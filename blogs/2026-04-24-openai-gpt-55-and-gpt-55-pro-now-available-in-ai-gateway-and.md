---
title: "OpenAI GPT-5.5 and GPT-5.5 Pro now available in AI Gateway and Agent Runners"
url: "https://www.netlify.com/changelog/gpt-5-5-ai-gateway-agent-runners/"
date: "Fri, 24 Apr 2026 00:00:00 GMT"
author: ""
feed_url: "https://www.netlify.com/changelog/feed.xml"
---
OpenAI’s GPT-5.5 and GPT-5.5 Pro models are now available through Netlify’s AI Gateway and Agent Runners with zero configuration required.

Use the OpenAI SDK directly in your Netlify Functions without managing API keys or authentication. The AI Gateway handles everything automatically. Here’s an example using the GPT-5.5 model:

import OpenAI from 'openai';

export default async () =&gt; {
    const openai = new OpenAI();

    const response = await openai.responses.create({
        model: 'gpt-5.5',
        input: 'Give a concise explanation of how AI works.',
    });

    return Response.json(response);
};

GPT-5.5 and GPT-5.5 Pro are available for all Function types and Agent Runners. You get automatic access to Netlify’s caching, rate limiting, and authentication infrastructure.

Learn more in the AI Gateway documentation and Agent Runners documentation.
