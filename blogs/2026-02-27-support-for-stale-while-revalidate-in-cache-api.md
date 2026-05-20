---
title: "Support for stale-while-revalidate in Cache API"
url: "https://www.netlify.com/changelog/cache-api-stale-while-revalidate/"
date: "Fri, 27 Feb 2026 00:00:00 GMT"
author: ""
feed_url: "https://www.netlify.com/changelog/feed.xml"
---
The Netlify Cache API now has full support for stale-while-revalidate (SWR). This was a previous limitation of the Cache API that has now been lifted, thanks to a request from a customer. When using fetchWithCache with the swr option, background revalidation is handled automatically.
