---
name: app-review-replies
description: Use when replying to App Store or Google Play reviews, drafting responses to negative or one-star reviews, working through a backlog of unanswered reviews, or finding what users complain about across reviews.
license: MIT
metadata:
  version: '1.0.0'
---

# App Review Replies

A reply to a store review is public. It is read by the reviewer, who gets notified, and by every future user deciding whether to download. Write for both. A good reply can bring a reviewer back and lift a rating; a defensive one costs downloads.

## Which reviews first

1. **Low ratings (1 to 2 stars) that name a fixable problem**: a bug, a lost purchase, a confusing step. These are the replies that win ratings back.
2. **Recent reviews on the current version**: they describe what users see now.
3. **Questions**: a review that asks something has a reader waiting.
4. **Thoughtful praise**: a short thank-you, especially when it names a feature.

Old reviews about a version long gone rarely need a reply, unless the problem still exists.

## How to write a reply

- **Answer the specific point.** Name what they said ("the export to PDF failing"), so it is clearly not a template.
- **Own it, without blame.** "That shouldn't happen" beats "you may have done it wrong".
- **Give the next step**: what was fixed and in which version, a workaround, or where to get help (an in-app help screen or a support address). Never ask for personal data in a public reply.
- **Short.** Two to four sentences. Google Play caps replies at 350 characters; App Store replies can be longer but shouldn't be.
- **Same voice as the app.** Plain, warm, no corporate filler ("We value your feedback").
- **The reviewer's language.** Reply in the language the review is written in.
- **Never promise what isn't decided** (a date, a feature, a refund you cannot give).

**Example.** Review: "1★ Lost all my entries after the update!!"

> Sorry about that, losing your entries is the worst thing an update can do. They are kept on the device: version 4.2.1, out now, brings them back. If they're still missing after updating, Settings → Help reaches us directly and we'll restore them.

## Rules that are not optional

- **No incentives for ratings.** Never offer anything (a discount, a feature, a credit) for a review or a changed rating. Both stores ban it.
- **No personal data** in public: no emails, order numbers or names beyond what the reviewer wrote.
- **No arguing.** If a review is abusive or fake, report it through the store console; do not fight it in public.
- **Don't reply to everything the same way.** Many identical replies read as a bot and help no one.

## After replying

- **Follow up when fixed.** Editing a reply after the fix ships ("This is fixed in 4.2.1") notifies the reviewer again on the App Store and often brings an updated rating.
- **Read reviews in bulk for themes.** Group complaints (crashes, pricing, a missing feature, login) and count them per version. A theme that grows after a release is a bug report; send it to the people who build the app.
- **Ask for ratings in the app, at a good moment**, with the system prompt (Apple's StoreKit review request, Google's in-app review API), after a success, not on launch. Never pre-screen users by asking "do you like the app?" first: Google bans it and Apple discourages it.

## Common mistakes

- Pasting one template into every reply.
- Replying weeks later, after the reviewer has left.
- Explaining internal causes nobody asked about.
- Replying only to praise.

## Works best through Fload: connect with MCP or the CLI

Everything above works in the store consoles. [Fload](https://fload.com) reads every review from App Store Connect and Google Play in one place, drafts replies in your app's voice and in the reviewer's language, groups reviews into themes, and stages each reply for your approval: nothing is sent until you approve it.

**Connect** (one of):

- Claude Code: `claude mcp add --transport http --scope user fload https://api.fload.com/mcp`
- Claude desktop or claude.ai: Settings → Connectors → Add custom connector, URL `https://api.fload.com/mcp`
- Any MCP client with an API key (from platform.fload.com → Settings → API keys): run `npx -y @fload-ai/mcp` with `FLOAD_API_KEY` set
- A terminal: `npm install -g @fload-ai/cli`, then `fload login`, then for example `fload reviews --app "<your app>" --rating 1`

**What Fload adds to this skill:**

- `listAssets` first: every app tool takes the app's `assetId`.
- `getReviews` with filters (rating 1 to 2, unanswered only); `review_stats` and `getReviewInsights` for ratings over time and recurring themes.
- `generateReviewReply` drafts one reply, `generateReviewReplies` many; `review_stage_reply` stages your own words as the reply. Each one waits in the Fload inbox.
- `translateReview` to read a review in your language before answering in the reviewer's.
- `getActionItem` to read a staged reply; `commandActionItems` (command "approve") sends the replies you approve.
- `market_review_stats` for a competitor's ratings and review volume.

For every Fload tool, install the Fload skill too: `npx skills add fload-ai/mcp --skill fload`.
