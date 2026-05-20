---
title: "Gemini 3.1 Flash Image Preview now available in AI Gateway"
url: "https://www.netlify.com/changelog/gemini-3-1-flash-image-preview-ai-gateway/"
date: "Thu, 26 Feb 2026 00:00:00 GMT"
author: ""
feed_url: "https://www.netlify.com/changelog/feed.xml"
---
Google's Gemini 3.1 Flash Image Preview, also known as Nano Banana 2, is now available through AI Gateway. You can call this image generation model from Netlify Functions without configuring API keys; the AI Gateway provides the connection to Google for you. Example usage in a Function: import { GoogleGenAI } from '@google/genai'; export default async (request: Request) => { const url = new URL(request.url); const prompt = url.searchParams.get('prompt') || 'two happy bananas'; const ai = new GoogleGenAI({}); try { const response = await ai.models.generateContent({ model:…
