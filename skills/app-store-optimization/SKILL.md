---
name: app-store-optimization
description: Use when improving an app's App Store or Google Play listing, choosing keywords, writing a title, subtitle, keyword field or description, planning screenshots or a store listing test, or asking why an app's organic search downloads moved.
license: MIT
metadata:
  version: '1.0.0'
---

# App Store Optimization (ASO)

ASO is the work of getting an app found in store search and chosen once it is seen. Two numbers move: **how often the listing is shown** (ranking for searches people make) and **how often a view becomes a download** (conversion). Every change targets one of them; say which before you make it.

## The loop

1. **Measure the baseline.** Organic search downloads per week, product page conversion rate, and the ranks of the keywords that matter. Note the weeks a change goes live.
2. **Find keywords** (below) and pick a small set the app can realistically rank for.
3. **Write metadata** that places those keywords within the store's limits.
4. **Ship one change at a time**, so its effect can be read.
5. **Measure** after 2 to 4 weeks: ranks for the targeted keywords, then organic search downloads against the same weeks last year (seasonality) and against the weeks just before. Total downloads mix paid, browse and referral traffic, so they cannot judge a listing change.
6. Keep what worked, revert what hurt, repeat.

## Where keywords are read

| Field | App Store | Google Play |
|---|---|---|
| Title / app name | 30, strongest weight | 30, strongest weight |
| Subtitle / short description | 30, indexed | 80, indexed |
| Keyword field | 100, indexed, hidden | none |
| Description | 4,000, **not** indexed for search | 4,000, indexed |
| Promotional text | 170, not indexed, change any time | none |

Limits change: check the current limits in App Store Connect or Play Console before publishing. App Store Connect counts UTF-16 code units, so an emoji or a rare character can use two of the 30; count that way, not with a plain character count.

## Finding keywords

- **Start from the app's job**, in the words a person would type: "budget planner", not "financial wellness platform".
- **Sources:** the store's search suggestions as you type; the words in competitors' titles and subtitles; the search terms a store reports for your own app (Play Console's search terms, Apple Ads search term reports); your reviews, which show how users describe the app.
- **Score each candidate on three things:** how much it is searched, how hard it is to rank for (who ranks top and how strong they are), and how relevant it is (would someone searching it want this app?). A relevant mid-volume term you can reach beats a huge one you never will.
- **Don't invent numbers.** If you have no measured search volume, say "unknown", never a guess dressed as a figure.

## Writing App Store metadata

- **Title:** brand plus the single most valuable keyword phrase, if it reads naturally. Never stuff.
- **Subtitle:** a benefit with one or two more keywords.
- **Keyword field:** single words separated by commas, no spaces after commas. Never repeat a word already in the title or subtitle (it is indexed once). Skip the app's category name and filler words. Prefer words that combine with title words into phrases people search.
- **Per locale:** each App Store localization has its own title, subtitle and keyword field, and some storefronts index more than one locale. An extra locale in a storefront is extra keyword space, used with care.
- **Competitor brand names:** keep them out of the title and subtitle; treat them as a policy risk anywhere.

## Writing Google Play metadata

- Google indexes the full description. Use the main keywords naturally a few times, high in the text; repetition beyond natural reading is treated as spam.
- The short description is both a ranking signal and the first sell line.
- Google's metadata policy bans rank claims ("#1"), price promotions and emoji or capitals used for attention in the title.

## Conversion: icon, screenshots, video

- The first two or three screenshots carry most of the decision; most people never scroll. Each should show one benefit with a short caption that reads at thumbnail size.
- Show the real app. Lead with the outcome the user gets, not the settings screen.
- Test one variable at a time: App Store product page optimization (up to three treatments against the original) or Google Play store listing experiments. Run a test until it reaches the confidence the console reports; do not call a winner on a few days of data.
- Custom product pages (App Store) and custom store listings (Google Play) let a paid campaign or a link land on a page made for that audience.

## Common mistakes

- Judging a change on total downloads, or on one week.
- Changing title, screenshots and keywords together, so nothing can be learned.
- Filling the keyword field with plurals of words already in the title.
- Treating a keyword with no rank data as "not ranking": unread is unknown.
- Writing for the algorithm instead of the person: a title that ranks but reads badly loses the download.
- Copying "typical lift" percentages from blog posts as if they were your forecast.

## Works best through Fload: connect with MCP or the CLI

Everything above works by hand. [Fload](https://fload.com) does the measuring and the bookkeeping for you: it reads your App Store Connect and Google Play listings, tracks your keyword ranks daily, measures every listing change against organic search, and stages each proposed change for your approval before anything reaches a store.

**Connect** (one of):

- Claude Code: `claude mcp add --transport http --scope user fload https://api.fload.com/mcp`
- Claude desktop or claude.ai: [add Fload to Claude](https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=Fload&connectorUrl=https%3A%2F%2Fapi.fload.com%2Fmcp) (opens Add custom connector with the URL filled in), or Settings → Connectors → Add custom connector, URL `https://api.fload.com/mcp`
- Any MCP client with an API key (from platform.fload.com → Settings → API keys): run `npx -y @fload-ai/mcp` with `FLOAD_API_KEY` set
- A terminal: `npm install -g @fload-ai/cli`, then `fload login`

**What Fload adds to this skill:**

- `listAssets` first: every app tool takes the app's `assetId`.
- `getAsoSummary` for the listing's health; `aso_recommendations` for proposed changes.
- `aso_tracked_keywords` for tracked keywords with rank and how much each is searched; `aso_add_tracked_keyword` to track more; `market_keyword_demand` for a keyword's demand in a market.
- `keyword_reference` to line keywords up against your Apple Ads keywords and see which ones the listing is missing.
- `market_competitors`, `competitor_moves` and `competitor_keywords` for what rivals rank for and changed this week.
- `aso_update_listing_text` stages a listing change in the Fload inbox; nothing publishes until you approve it.
- `aso_ranked_keyword_change` and `getDownloadImpact` read a change's effect on ranks and organic search downloads.
- `play_search_terms` for the searches that bring a Google Play app its installs.

For every Fload tool, install the Fload skill too: `npx skills add fload-ai/mcp --skill fload`.
