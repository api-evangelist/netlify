---
title: "Netlify Database is now generally available"
url: "https://www.netlify.com/changelog/2026-04-28-netlify-database/"
date: "Tue, 28 Apr 2026 00:00:00 GMT"
author: ""
feed_url: "https://www.netlify.com/changelog/feed.xml"
---
Netlify Database is launching today as a serverless Postgres database that's deeply integrated into the Netlify workflow and upgraded from the beta experience to a full Netlify primitive.

Netlify Database is designed to provide strong guardrails out-of-the-box when collaborating with team members and AI agents. For example, a marketing team member can start an agent run to suggest a feature that requires database changes, and then test the changes in a preview environment. A developer then reviews and publishes the change, and only then is the production database changed.

When you create or update a project on Netlify using Agent Runners, your AI agent will automatically detect whether your app needs a database and set it up for you as needed. If you're working locally, a database is provisioned automatically when you install @netlify/database and deploy to Netlify.

Learn more about why we built Netlify Database and how it works in our official blog post.

What's new

Netlify Database replaces the beta Netlify DB experience that required an extension for the initial setup. The new experience is a native Netlify primitive, which means you can customize your database setup, choose your own ORM, and more.

Pricing and availability

Netlify Database is available for Credit-based plans only. When a database is active, it consumes credits for the compute and bandwidth used. However, database storage space (i.e., the size of data stored) is free until July 1, 2026.

Different limits apply to your database depending on your plan type. Learn more in the Plan limits docs.

Usage meter updates

To help you better understand how database usage works alongside other meters, we're adding more context to how your usage is calculated and applied.

We're breaking down the Bandwidth and Compute meters to show you more granular usage for your team's databases:

Before launch: Bandwidth
After launch: Bandwidth is now broken down into Database Bandwidth and Web Bandwidth

Before launch: Compute
After launch: Compute is now broken down into Database Compute and Functions & Agent Compute

Learn more about how usage meters work in our Database usage meters docs.

Switching from the Netlify DB Beta experience

If you set up a database using the Netlify DB Beta experience, which required the Neon extension, you can continue using it — Netlify will continue to support these databases. If you have a Credit-based plan, you have the option to switch to the new experience.

Get started

Get started with Netlify Database from your Agent Runners dashboard, favorite local AI agent, or CLI.

Here are some quick docs links to get you started:

<ul>
<li>Netlify Database docs

</li>
<li>API docs

</li>
<li>CLI reference

</li>
<li>Switch to Netlify Database

</li>
</ul>
