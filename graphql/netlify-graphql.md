# Netlify GraphQL API

Netlify offered a GraphQL API through its Netlify Graph developer preview (built on the OneGraph platform, which Netlify acquired in 2021). The API was accessible at `https://graph.netlify.com/graphql?app_id={NETLIFY_SITE_ID}` and exposed a unified `oneGraph` root query field that provided introspection and management of connected third-party service schemas, CLI session coordination, and persisted query management. The API supported OAuth 2.0 authentication via Bearer tokens and was scoped per Netlify site, with the site ID supplied as a query parameter on each request.

The Netlify Graph API enabled developers to compose GraphQL schemas from multiple third-party OAuth services (GitHub, Slack, Salesforce, Stripe, and others) into a single federated endpoint tied to their Netlify site. Authentication was handled via Netlify-issued access tokens or OneGraph API tokens, with webhook support for subscriptions secured by an HMAC-SHA256 webhook secret (`NETLIFY_GRAPH_WEBHOOK_SECRET`). The CLI integration used session-based coordination types to synchronize schema state between the local development environment and the cloud.

Netlify Graph was available as a developer preview and has since been deprecated; the `graph.netlify.com` host is no longer resolvable. Netlify's current API surface is a REST API at `https://api.netlify.com/api/v1/` documented via OpenAPI. The types, queries, and mutations documented here are drawn from the `netlify-onegraph-internal` npm package (v0.10.1) and represent the confirmed schema surface used by the Netlify CLI during the lifetime of the Graph developer preview.

**Endpoint:** https://graph.netlify.com/graphql?app_id={NETLIFY_SITE_ID}

**Documentation:** https://docs.netlify.com/graph/get-started/

**References:**
- Documentation: https://docs.netlify.com/graph/get-started/
- GettingStarted: https://docs.netlify.com/api-and-cli-guides/api-guides/get-started-with-api/
