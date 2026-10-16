---
title: "Know who is visiting your protected site, right from your functions"
url: "https://www.netlify.com/changelog/2026-10-07-context-user-in-functions/"
date: "2026-10-07"
feed_url: "https://www.netlify.com/changelog/feed.xml"
---
On private projects and sites protected with Netlify team login, your Netlify Functions and Edge Functions can now see who is making the request. The signed-in Netlify user is available as context.user, with their user ID, email address, and when their access expires. This function returns the signed-in user's ID, email address, and access expiry as JSON at /whoami, and responds with a 401 when context.user isn't set: // netlify/functions/whoami.ts import type { Config, Context } from '@netlify/functions' export default async (req: Request, context: Context) => { if (!context.user) { return ne
