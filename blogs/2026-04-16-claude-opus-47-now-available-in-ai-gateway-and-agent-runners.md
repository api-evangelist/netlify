---
title: "Claude Opus 4.7 now available in AI Gateway and Agent Runners"
url: "https://www.netlify.com/changelog/claude-opus-4-7-ai-gateway-agent-runners/"
date: "Thu, 16 Apr 2026 00:00:00 GMT"
author: ""
feed_url: "https://www.netlify.com/changelog/feed.xml"
---
Anthropic's Claude Opus 4.7 model is now available through Netlify's AI Gateway and Agent Runners with zero configuration required.

Use the Anthropic SDK directly in your Netlify Functions without managing API keys or authentication. The AI Gateway handles everything automatically. Here's an example using the Claude Opus 4.7 model:

import Anthropic from '@anthropic-ai/sdk';

export default async () =&gt; {
    const anthropic = new Anthropic();

    const response = await anthropic.messages.create({
        model: 'claude-opus-4-7',
        max_tokens: 4096,
        messages: [
            {
                role: 'user',
                content: 'How can AI improve my coding?'
            }
        ]
    });

    return new Response(JSON.stringify(response), {
        headers: { 'Content-Type': 'application/json' }
    });
};

Claude Opus 4.7 is available for all Function types and Agent Runners. You get automatic access to Netlify's caching, rate limiting, and authentication infrastructure.

Learn more in the AI Gateway documentation and Agent Runners documentation.
