---
title: "Node.js 24 is now the default for Builds and Functions on new sites"
url: "https://www.netlify.com/changelog/2026-07-07-nodejs-24-default-new-sites/"
date: "2026-07-07"
feed_url: "https://www.netlify.com/changelog/feed.xml"
---
New sites created on Netlify now use Node.js 24 by default for both builds and Netlify Functions. Existing sites aren’t affected — they keep using whatever Node.js version they’re currently pinned to, whether that’s set via a NODE_VERSION environment variable, an .nvmrc/.node-version file, or the engines.node field in package.json. If you want to move an existing site to Node.js 24, follow the Node.js version configuration guide for builds, and the functions runtime version guide for Netlify Functions.
