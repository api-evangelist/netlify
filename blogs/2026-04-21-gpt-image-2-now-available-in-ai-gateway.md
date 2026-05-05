---
title: "GPT Image 2 now available in AI Gateway"
url: "https://www.netlify.com/changelog/gpt-image-2-ai-gateway/"
date: "Tue, 21 Apr 2026 00:00:00 GMT"
author: ""
feed_url: "https://www.netlify.com/changelog/feed.xml"
---
OpenAI’s GPT Image 2 is now available through AI Gateway. You can call this model from Netlify Functions without configuring API keys; the AI Gateway provides the connection to OpenAI for you.

Example usage in a Function:

import OpenAI from 'openai';
const ai = new OpenAI();

export default async (req, context) =&gt; {
    const response = await ai.images.generate({
        model: 'gpt-image-2',
        prompt: 'Generate a realistic image of a golden retriever working at a tech startup',
        n: 1,
        size: '1024x1024',
        quality: 'low',
        output_format: 'jpeg',
        output_compression: 80
    });

    const imageBase64 = response.data[0].b64_json;
    const imageBuffer = Uint8Array.from(atob(imageBase64), (c) =&gt; c.charCodeAt(0));

    return new Response(imageBuffer, {
        status: 200,
        headers: {
            'content-type': 'image/jpeg',
            'cache-control': 'no-store'
        }
    });
};

This model works across any function type and is compatible with other Netlify primitives such as caching and rate limiting, giving you control over request behavior across your site.

See the AI Gateway documentation for details.
