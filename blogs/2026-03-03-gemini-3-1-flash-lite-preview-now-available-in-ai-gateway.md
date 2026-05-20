---
title: "Gemini 3.1 Flash-Lite Preview now available in AI Gateway"
url: "https://www.netlify.com/changelog/gemini-3-1-flash-lite-preview-ai-gateway/"
date: "Tue, 03 Mar 2026 00:00:00 GMT"
author: ""
feed_url: "https://www.netlify.com/changelog/feed.xml"
---
Google’s Gemini 3.1 Flash-Lite Preview is now available through AI Gateway. You can call this model from Netlify Functions without configuring API keys; the AI Gateway provides the connection to Google for you. Example usage in a Function: import { GoogleGenAI } from '@google/genai'; export default async () => { const ai = new GoogleGenAI({}); const response = await ai.models.generateContent({ model: 'gemini-3.1-flash-lite-preview', contents: 'How can AI improve my coding?' }); return Response.json(response); }; This model works across any function type and is compatible with other Netlify…
