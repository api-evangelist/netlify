---
title: "New `netlify logs` CLI command"
url: "https://www.netlify.com/changelog/2026-05-01-netlify-logs-cli-command/"
date: "Fri, 01 May 2026 00:00:00 GMT"
author: ""
feed_url: "https://www.netlify.com/changelog/feed.xml"
---
The Netlify CLI now includes a netlify logs command, giving you a powerful and flexible way to access logs for your projects whether you're a developer debugging locally or an AI agent processing structured output.

Filter by source

Use --source to pull logs from functions, edge functions, deploys, or any combination of them together. Color-coded output makes it easy to tell sources apart at a glance when you're tailing multiple at once.

netlify logs CLI showing colour-coded output from functions and edge functions

Need to narrow it down further? The --function and --edge-function flags let you filter to a specific function by name, and --url lets you target the exact deploy you want logs from.

Historical and real-time views

The --since and --until flags let you query logs over any specific time window — useful for tracking down what happened during a past deploy or incident. When you want to watch logs as they come in, --follow streams them in real time.

JSON Lines support

Pass --json to get structured output in JSON Lines format. This works in both historical and real-time modes, making netlify logs easy to pipe into your own tooling or integrate into automated workflows.

netlify logs CLI with --json flag showing JSON Lines output

Update to the latest Netlify CLI to start using it:

npm install -g netlify-cli@latest

Then run netlify logs --help to see all available options.
