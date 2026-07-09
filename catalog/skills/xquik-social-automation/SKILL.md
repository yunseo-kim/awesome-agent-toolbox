---
name: xquik-social-automation
description: "Use Xquik for X/Twitter search, extraction, monitoring, webhooks, and approval-gated publishing through API and MCP workflows"
license: Sustainable Use License 1.0

metadata:
  domain: business
  subdomain: communications
  tags: "xquik, x-twitter, social-media, mcp, rest-api, webhooks, automation"
  frameworks: "mcp, rest-api"
  author: "Xquik"
  lastUpdated: "12026-07-09"
  provenance: original
---

# Xquik Social Automation

Use this skill when an agent needs to research, monitor, analyze, or prepare
X/Twitter workflows with Xquik. Keep publishing approval-gated unless the user
has explicitly authorized the action and the local toolchain is already
configured for writes.

## When to Apply

Use this skill when:

- Searching or extracting X/Twitter posts, profiles, followers, media, or trends
- Monitoring accounts, keywords, or activity and delivering webhook updates
- Preparing drafts, replies, scheduled posts, or analytics reports for review
- Connecting an agent to the Xquik MCP server or REST API
- Validating X/Twitter workflow examples without exposing API keys

## Setup

1. Read the current docs at <https://docs.xquik.com/mcp/overview>.
2. Store the API key outside the repository as `XQUIK_API_KEY`.
3. Configure the MCP endpoint at `https://xquik.com/mcp`.
4. Send the key as `Authorization: Bearer ${XQUIK_API_KEY}`.
5. Keep secrets out of prompts, logs, screenshots, issues, and commits.

## Workflow

1. Clarify the user goal: search, extraction, monitor, analytics, or publishing.
2. Choose the least-privilege Xquik surface: MCP for agent workflows, REST API
   for scripted integrations, webhooks for event delivery.
3. Run a read-only or dry-run step first when the workflow can affect public
   content.
4. Show the user the exact draft, filters, targets, and schedule before
   publishing or changing monitors.
5. Record only public identifiers, result IDs, and safe status metadata in
   project notes.

## Safety Checklist

Before any write, schedule, webhook, or monitor change:

- Confirm the target account, post, keyword, or webhook destination.
- Confirm the final text and media.
- Confirm timing and retry behavior.
- Avoid storing raw cookies, API keys, access tokens, or session material.
- Keep operational details out of public notes, prompts, logs, and issues.

## Useful References

- MCP overview: <https://docs.xquik.com/mcp/overview>
- MCP endpoint: <https://xquik.com/mcp>
- Public package and source: <https://github.com/Xquik-dev/x-twitter-scraper>
- Server manifest: <https://xquik.com/.well-known/mcp.json>
