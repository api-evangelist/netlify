---
title: "Netlify Identity package update: CSRF protection with new `verifyRequestOrigin` helper"
url: "https://www.netlify.com/changelog/2026-05-02-netlify-identity-verify-request-origin/"
date: "2026-05-02"
feed_url: "https://www.netlify.com/changelog/feed.xml"
---
@netlify/identity 1.1.0 introduces a new verifyRequestOrigin helper to make it easier for developers and AI agents to add CSRF (Cross-Site Request Forgery) protection when running authentication on the server. You can call login(), signup(), or logout() from a Netlify Function or Edge Function to handle authentication entirely on the server. The library reads and writes the nf_jwt and nf_refresh cookies through the Netlify runtime, so the user’s browser receives the session via the response.
