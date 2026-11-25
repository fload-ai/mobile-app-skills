# Mobile app skills

Free agent skills for the jobs of running a mobile app: store optimization, review replies, Apple Ads, app metrics, building and launching.

## Install

**Claude Code**, everything in one plugin (the six skills, Fload's MCP server and three commands):

```
/plugin marketplace add fload-ai/mobile-app-skills
/plugin install fload@mobile-app-skills
```

The first time a command uses Fload, run `/mcp` and sign in to Fload.

**The skills only**, in any agent that reads skills, with no account:

```
npx skills add fload-ai/mobile-app-skills
```

## Upgrading from 1.x

The mobile-app skills are now one plugin, fload@mobile-app-skills, and the skills themselves are rewritten (2.0). If you installed 1.x, remove the old plugin first, then install the new one:

```
/plugin uninstall mobile-app-skills@mobile-app-skills
/plugin install fload@mobile-app-skills
```

## The skills

| Skill | What it teaches |
|---|---|
| [app-store-optimization](skills/app-store-optimization/SKILL.md) | Keywords, listings, screenshots and store tests on both stores |
| [app-review-replies](skills/app-review-replies/SKILL.md) | Which reviews to answer, replies in your voice and the reviewer's language, and how to measure coverage and time to reply |
| [apple-search-ads](skills/apple-search-ads/SKILL.md) | Campaigns, keywords, bids and budgets, and when a number can be trusted |
| [mobile-app-metrics](skills/mobile-app-metrics/SKILL.md) | Adding up each kind of number the right way, comparing periods, and telling a real drop from noise |
| [launch-an-app](skills/launch-an-app/SKILL.md) | Every App Store and Google Play step in order, the check before you submit, and answering App Review |
| [build-an-app](skills/build-an-app/SKILL.md) | Checking an idea's demand, a one-page plan, the name, and building and testing screen by screen |

Each skill teaches the job on its own, with its thresholds, the hard rules, common mistakes and a worked example. Each ends with how to do it through [Fload](https://fload.com), if you use it.

## Commands

The plugin adds three commands. Each one takes an app name, or uses your only app.

| Command | What it does |
|---|---|
| `/fload:morning` | What changed in your app since yesterday, the likely reason for each change, and the one thing to do today. |
| `/fload:reviews` | Your unanswered reviews, worst first, grouped by what people say, with a suggested reply for each one that needs it. |
| `/fload:keywords` | Where your app ranks, what moved this week and the likely reason, and the keywords your listing or Apple Ads are missing. |

All three only read. Anything that would change your app still asks you first.

## What needs a Fload account

- The six skills teach each job on their own. They need no account.
- The commands and the MCP server read your own app's numbers, reviews and keywords, so they need a Fload account with your app connected.
