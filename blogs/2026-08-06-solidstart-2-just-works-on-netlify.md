---
title: "SolidStart 2 just works on Netlify"
url: "https://www.netlify.com/changelog/2026-08-06-solidstart-2-on-netlify/"
date: "2026-08-06"
feed_url: "https://www.netlify.com/changelog/feed.xml"
---
SolidStart 2 is out, and it deploys to Netlify with no framework-specific adapter to install, a first for full-stack frameworks on Netlify. While SolidStart 1 deployed to Netlify through Nitro under the hood, SolidStart 2 no longer includes Nitro, building directly on Vite’s Environment API instead. The Netlify Vite plugin can now take the server build Vite produces and prepare it for deployment on its own, with no SolidStart-specific Netlify adapter needed in between.
