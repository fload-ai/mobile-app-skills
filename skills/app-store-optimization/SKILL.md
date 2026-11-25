---
name: app-store-optimization
description: Use when improving an app's App Store or Google Play listing, auditing a listing, choosing keywords, writing a title, subtitle, keyword field, short or full description, deciding whether to replace a keyword, localizing a listing or using a second locale for more keywords, planning screenshots, custom product pages or store listing tests, reading whether a listing change worked, or deciding whether to roll a change back after organic downloads or keyword ranks moved.
license: MIT
metadata:
  version: '2.0.0'
---

# App Store Optimization (ASO)

ASO is the work of getting an app found in store search and chosen once it is seen. It moves two things:

- **Visibility:** how often the listing is shown, which comes from the ranks it holds for the searches people make.
- **Conversion:** how often a view of the listing becomes a download.

Every change targets one of them. Say which one before you make it.

This skill is a full method for both stores. It covers how to:

- audit a listing;
- find and judge keywords;
- decide what to replace and what to protect;
- write the fields;
- test, read the result, and decide whether to keep or roll back.

It works by hand. The checklist for an audit is in [references/audit-checklist.md](references/audit-checklist.md).

## The ground rules

Six rules govern everything below:

1. **Keep platform, storefront and locale apart.** "Germany" is a storefront. "German" is a language. One App Store storefront can read more than one localization. Never guess one from the other: name all three for every recommendation.
2. **Never invent a number.** Do not make up a rank, search volume, difficulty, conversion rate, download count, competitor field or rollout status. If you do not have it:
   - write "unknown";
   - estimate from a real signal (ratings count, ranks you can see, download estimates) and label it an estimate;
   - or mark that one decision as waiting for data while the rest of the work goes on.

   Missing data never stops the whole analysis.
3. **Label your evidence**, strongest first:
   - the app's own console data;
   - what you see in the live store;
   - the platform's own documentation;
   - an outside estimate;
   - a calculation;
   - a rule of thumb;
   - your own inference.

   An idea you generated is an inference until something checks it.
4. **Hard gates beat good numbers.** A keyword that is not relevant fails, whatever its volume. So does a claim the app cannot back up, or a policy breach. Relevance means: would someone who searched this be happy after installing? Score it from 1 to 5. Below 3 it is off-category and is not used anywhere.
5. **Rules of thumb are not rules.** Search volume cutoffs, difficulty tiers, timing windows and "typical uplift" figures are starting points. Use them, say so, and let real data overrule them.
6. **A before and after is not proof.** If paid spend, featuring, price, seasonality, ratings or several assets changed in the same window, the change is at most associated with the result. Name what else moved.

## The decisions you can make

Give every object its own decision: each keyword, each page, each market, each action. A swap is never one verdict.

| Decision | When |
|---|---|
| **Proceed** | Evidence is enough and nothing blocks it. Do it, if you are allowed to. |
| **Protect** | The current element is proven to be worth something. Replacing it needs strong evidence of a net gain. |
| **Test** | It might help or hurt, the doubt is real, and a safe, reversible test can measure it. |
| **Hold** | Keep things as they are while evidence matures or a good trend continues. |
| **Needs data** | A required input is missing; do not decide yet. |
| **Review** | A person must decide: a policy question, contradictory high-value evidence, or a material downside. |
| **Reject** | It fails a hard gate, or its expected value is clearly negative. |

**Protect what is proven before you chase what is promising.** When a swap is roughly balanced, do not choose for the owner. Keep the current element and offer the swap as an optional, riskier choice.

## Step 1: Measure the baseline

Before any change, write down the following:

- **Organic downloads** per week, per storefront you will touch. Use at least 28 days of clean history: no launch spike, no featuring, no outage in it.
- **Product page conversion:** page views to downloads, on the store's own definition. Google Play changed how it reports acquisitions. Keep the old series and the new click-based series apart; never join them into one line.
- **Ranks** of every keyword the app ranks for in those storefronts, not only the ones you plan to change.
- **What else is going on:**
  - paid spend per day;
  - featuring;
  - price changes;
  - rating trend;
  - releases;
  - seasonal events in each market.

Judge confidence by volume. Under about 100 organic downloads in 30 days, a storefront's reads are low confidence. From about 1,000 they are high. When a market is small, widen the window to 90 days, then to 12 months.

## Step 2: Judge how strong the app is

How hard a keyword the app can win depends on its ranking power.

- **Ranking power** comes from recent downloads from every source, over the last 30 and 90 days. Brand searches and paid downloads count. Ratings and reviews support the reading. Lifetime totals count for little: an app is judged on recent traction.
- **Technical health and conversion can cap it.** An app with a serious crash or "app not responding" problem should not plan as a strong app until that is fixed.
- **Keep ranking power apart from how well the app uses it.** A strong app with few generic keyword ranks is not a weak app. It is an app under-using its ASO, and that is an opportunity.

## Step 3: Find and judge keywords

**Start from the app's job**, in the words a person would type: "budget planner", not "financial wellness platform".

**Where to look:**

- the store's search suggestions as you type;
- competitors' titles and subtitles (or short descriptions);
- the search terms the stores report for your own app, including Google Play's search terms and Apple Ads search term reports;
- your reviews, for how users describe the app;
- native speakers' searches in each market.

**Research each market locally.** Never translate keywords one to one. People in Germany search "abnehmen", not the literal translation of "weight loss". Chinese, Japanese and Korean listings need native writing and a native review, not translation.

**Other brands' names and words never to suggest:**

- When you judge how relevant a keyword is, judge another brand's name by fit, like any word. A closely related brand can count as relevant. The app's own brand always counts.
- Competitor names stay out of the name, subtitle, promotional text and description. In the keyword field they are allowed, with a note (Step 5).
- Never suggest an Apple trademark, or a celebrity's or other protected name. Step 5 says what to do when the app owner adds one.
- Never suggest or show slurs, profanity, sexual terms, or terms for illegal or harmful acts, whatever the keyword data says.

**Judge each candidate on four things together:**

1. **Difficulty**, as a first filter only. Difficulty scores are imperfect, and tiers like 40, 60 and 80 are examples, not rules. You can measure a ceiling for this app instead:
   - take the generic (non-brand) keywords it has held in the top 10 for at least 3 weeks;
   - drop clear outliers;
   - average the 5 hardest.

   With fewer than 5 such keywords there is no measured ceiling. Treat any tier as provisional and let the next three checks decide.
2. **Ranking power against the competitors who rank for it.** A keyword is realistic when apps of similar strength rank for it. Drop it in priority when every app ranking for it is clearly stronger.
3. **Placement**, yours and the competitors'. A word in the title has a better chance than the same word lower down, even at higher difficulty.
4. **Current rank**, yours and the competitors'.

**Search volume is demand, not downloads.** A store's popularity score is relative, so never turn it into an install forecast.

- Below a popularity of about 10, a keyword offers limited value. For a large app the line is about 30.
- The exception is a new app with no meaningful ranks yet: low-volume, relevant terms are its way in.
- Track every keyword the app ranks for, low ones included.

**Group keywords by intent, not volume.** Combine keywords that one page promise can satisfy. Split them when they need different messages or creative. A group is your unit for custom pages later.

## Step 4: Decide what to replace and what to protect

Listing space is scarce. Every new word usually pushes an old one out, so the real question is the **net gain**: what the new word adds minus what the removed word was bringing.

**Before you remove or change any existing word**, check what it does today:

- its rank and the traffic it brings;
- its brand value;
- the phrases it helps form with other words;
- the characters it costs;
- the risk if you need to undo the change.

**A word has traction** when it, or a phrase it completes, ranks in the top 30. For a large app, use the top 15.

**Before removing a weak word**, check:

- **Can it move up instead?** A word ranking within the top 50 in a lower field may do better moved into the title or subtitle.
- **Was it given a real chance?** Removal needs at least 6 weeks of observations showing it never broke into a realistic band while the top 10 stayed out of reach. One snapshot is not enough.
- **Is it protected?** Momentum, a seasonal or strategic role, a unique place in a phrase (even at zero measured volume), or working performance all stop a removal.
- **Is there an easier word with the same intent?** Write down why you are swapping.

**When the gain is not clearly established, protect the current word.**

## Step 5: Write the fields

### App Store

| Field | Limit | Indexed for search |
|---|---|---|
| App name (title) | 30 | yes, strongest |
| Subtitle | 30 | yes |
| Keyword field | 100, hidden | yes |
| Promotional text | 170, change any time | no |
| Description | 4,000 | no |

- **Count characters the way the store does.** Emoji and flags can count as more than one character.
- **App name:** the brand plus the single most valuable keyword phrase, if it reads naturally. Put the most valuable generic word early. Never stuff.
- **Subtitle:** a benefit carrying one or two more keywords, from local research. Do not waste it on a generic tagline or on words already in the title.
- **Keyword field:**
  - single words separated by commas, with no spaces after the commas;
  - never repeat a word already in the name or subtitle (a word is indexed once);
  - use the singular only where you have checked that the store matches plurals in that language;
  - use digits instead of spelled-out numbers;
  - drop filler words where existing ranks allow;
  - break target phrases into their words and spread them across the three fields of the same locale; the store combines them.
- **Fill the space.** An empty character in the three indexed fields is lost reach. Check again after every removal.
- **Do not duplicate across fields** unless the duplicate is needed to assign that keyword to a custom product page.
- **Competitor names:** keep them out of the name, subtitle, promotional text and description. In the keyword field they are a common tactic and allowed, with a note that Apple can reject an app for using another company's trademark (guideline 5.2.5).
- **Apple's trademarks and protected names:** never suggest Apple's own trademarks, or a celebrity's or other protected name, for any field, unless the app owns or licenses it. Apple rejects apps under guideline 5.2.5 for this; for example, "iMessage" in a name or subtitle. If the app owner adds one themselves, allow it with a warning that Apple can reject the app for it. Your own brand is fine. Bidding on competitor names in Apple Ads is a different matter, and is allowed.
- **Keywords for custom product pages:** you can assign keywords from the app's latest approved version to a custom product page (up to 70 pages per app). Searches for those keywords then show that page instead of the default one.
- **App tags** on the App Store are generated by Apple from your listing and cannot be set. Clear, accurate metadata is the only lever.

**Second locales (cross-localization):**

- Many App Store storefronts read more than one localization. For example, the US storefront also reads Spanish (Mexico). The extra locale's name, subtitle and keyword field are extra keyword space.
- Use it only where you have checked that the storefront really indexes it. The words are still seen by the people who use that locale, so weigh what that market could lose against what the target market gains.
- Keyword sets overlap across languages. Decide on the combined opportunity: overlapping terms can move into the second locale, freeing the main one, while terms that matter locally stay protected.
- Repurposing a locale is a test, never a plain switch.
- Make the app's primary language an English locale, preferably English (US), so English (UK) stays free to serve as a second locale.
- Remove a duplicate across overlapping locales only when it is truly redundant. Keep the most important coverage in the primary listing.

### Google Play

| Field | Limit | Indexed for search |
|---|---|---|
| App name (title) | 30 | yes, strongest |
| Short description | 80 | yes |
| Full description | 4,000 | yes |

- **Repeat the main keywords** across the title, the short description and the full description.
- **Full description:**
  - weave the core keywords in naturally, high in the text;
  - about 2 to 5 mentions of a core keyword is a reference, not a target;
  - around 30 repetitions or about 5% density is only a stuffing alarm.
- **Short description:** a ranking signal and the first sell line, with keywords from local research.
- **Policy:** Google's metadata policy bans rank claims ("#1"), price promotions, and emoji or capitals used for attention in the title.
- **Tags:** choose accurate, relevant tags in the console. Unlike the App Store, Google Play lets you set them.
- **Category:** check the category fits the product truthfully, for browse and charts. On the App Store, check the secondary category too.

Limits change: check the current limits in App Store Connect and Google Play Console before you publish.

## Step 6: Conversion (icon, screenshots, video, pages)

- **The first three screenshots carry most of the decision**, because most people never scroll. Build them as a hook, a value and a result, each with a short caption that reads at thumbnail size. Show the real app.
- **Screenshot caption text is a possible but unconfirmed ranking signal.** Some say it counts since mid-2025, others find no conclusive proof, and Apple has not confirmed it. Matching the strongest search intent on the default page does lift conversion on that keyword, so featuring a keyword in the screenshots is a fair test. Measure the page's conversion, never a claimed rank shift.
- **Video:** the first frame and first seconds must say the value without sound.
- **Localize** screenshots in your main markets, and keep one formal or informal form of address per market across text and screenshots.
- **Custom product pages** (App Store) and **custom store listings** (Google Play) are a low-risk, high-return tactic. Build one for each important intent group or campaign theme.
  - On the App Store you can also assign keywords to a custom product page (Step 5), so organic searches for them land on it.
  - A custom page gets no ranking boost of its own.
  - Before launch, define the baseline, the success metric, the window, the minimum traffic and what would make you remove it.
  - A win is confirmed against the default page after launch, not by relevance alone.
- **A group becomes a custom page test** only when all five of these pass:
  - one coherent intent;
  - real demand or value;
  - the app can rank or is visible for it;
  - the market is ready;
  - the creative can be clearly different.

  Otherwise merge it into an existing page or fix the ranking first.
- **Ratings are conversion.** A low rating is fixed in the product, support and review prompts before you scale acquisition. Use the stores' native review prompts at moments of real satisfaction, and answer negative reviews quickly in the user's language.
- **Google Play's technical health** shows in the store. Watch the crash rate and the "app not responding" rate against Google's bad-behavior thresholds, and fix them first when they are breached.

## Step 7: Ship one change, and lock what it touches

- **One material change at a time.** If several changes go live together, the result belongs to the bundle.
- **Running-test lock:** while a metadata test runs, propose no other change to the name, subtitle, keyword field or description in that localization. That includes any localization a storefront reads together with it. Promotional text may still change.
- **Native tests:** use product page optimization (App Store, up to three treatments against the original) and store listing experiments (Google Play) for creative and text. Run each until it reaches the confidence the console reports.
- **Seasonal moments** in each market are among the strongest levers, for example Ramadan, Golden Week and Singles' Day. Plan them per market, together with in-app events, promotional content and featuring nominations for real updates.

## Step 8: Read the result

**Decide the read before launch**: the metric, the guardrail, the window and the stop-loss.

| Change | Read | Guardrail | Window |
|---|---|---|---|
| Keywords or metadata | rank movement of the new and the removed keywords; conversion only for a title change | no material rank drop on protected words | first look at 14 to 21 days; verdict after one full 30-day cycle |
| Localization | the market's organic downloads and conversion | no damage to other locales; watch retention and ratings | 28 to 56 days |
| Creative or custom page | conversion against the default page | retention and refunds | the store test's own confidence, else 14 to 21 days |

- **A rank check is an observation**, not a fact. Results vary by device and context. Look for a trend over at least 2 to 3 consistent observations.
- **Paid and organic are kept apart.** Apple Ads data can suggest organic ideas, but it is never proof that paid spend moved an organic rank. If ad spend fell by 30% or more during the window, a rank drop is not a reason to roll back.
- **Report each change beside the other factors** for the same weeks (paid, featuring, seasonality, price, ratings, releases), each marked unchanged, up or down. A good result gets a short comment. A bad one gets a full review of the non-ASO factors.

## Step 9: Keep, or roll back

**Never roll back automatically.** A rollback is a recommendation that a person decides, on the value lost against the value gained. Work through these rules in order:

1. **An add-only change** fills empty space and removes nothing, so it is never rolled back. Still read its performance. If organic downloads fall more than 10% with no explanation, the read is inconclusive: hold, do not roll back.
2. **Too early:** with fewer than 28 days of clean organic history in the touched storefronts, the read needs more data. Report the keyword moves as information and read again later.
3. **Keyword ranks come first.** Read the whole update, never one keyword: every tracked keyword and phrase in the touched storefronts, not only the changed ones.
   - Turn each rank into an estimate of daily downloads, from its search volume and the share of searchers who download at that rank.
   - Weigh gains and losses one to one.
   - If there is no real net loss, there is no rollback, whatever downloads did.
4. **Organic downloads are the supporting check.** Downloads alone never trigger a rollback. Offer a rollback with high importance only when:
   - there is a net, volume-weighted loss of keyword ranks, **and**
   - organic downloads in the touched storefronts are more than 10% below the level expected for those weeks, with seasonality accounted for, **and**
   - outside causes are removed first (featuring, a spike in paid spend, a release).

   Small storefronts (under about 100 organic downloads a month) are left out of this read.
5. **When the removed keyword fell and the new one did not improve**, the new keyword's rank decides:

   | New keyword's rank | What to do |
   |---|---|
   | 1 to 5 | likely keep (still review the trade-off) |
   | 6 to 10 | consider a rollback if the removed keyword was top 5 |
   | 11 to 30 | look at what the removed keyword brought (popularity above 5? ranked better than 10?); consider a rollback |
   | below 30 | consider a rollback; keep watching for upward movement |

6. **The only gain is on a competitor's name in the keyword field (App Store only):** the change counts as kept, with the note from Step 5. If the other new keywords still do not rank after two test cycles (60 days), swap them in a new update. That is a swap, not a rollback.
7. **Google Play:** where keyword-level rank impact cannot be measured reliably, do not use rank loss to recommend a rollback. Instead:
   - with no fall beyond 10% in organic downloads, keep the change;
   - with a verified fall of more than 10% after seasonality and outside events are removed, send it to a person for review;
   - when the cause cannot be separated, hold it as inconclusive.

   On Google Play an add-only change is an addition to the full description that leaves the title, short description and the rest of the description unchanged.

**Watch for alarms between changes**, on the app's organic downloads across all storefronts combined. A single storefront swings too much to alarm on.

1. A week well below the weeks before it is only a flag.
2. An alarm needs the last 30 days to be at least 10% below the 30 days before.
3. Then compare the same 30 days against last year, when you have 12 months of history:
   - only the first comparison down, and last year's same weeks also down: it is likely seasonal, so say so;
   - both down: look for the cause (a rank loss, a rating drop, an outage, a release, ad spend, featuring, a competitor move or a market-wide shift) before you change anything.

Skip this for an app under about 300 organic downloads a month: its normal noise is bigger than 10%.

## Never do these

- Incentivized installs to push a keyword, fake or paid reviews, review attacks on competitors, bot engagement, or bursts of bought installs to fake ranking velocity. You may detect and report a competitor doing this; you never recommend it.
- Change the name, screenshots and keywords together and then claim one of them worked.
- Judge a listing change on total downloads. They mix paid, browse and referral traffic.
- Copy "typical uplift" figures from articles as if they were your forecast.
- Compare benchmarks across stores, markets or categories that are not alike. Prefer the market's own history, then a comparable market with the same metric, then a category benchmark with its limits stated.
- Treat a keyword with no rank data as "not ranking". Unread is unknown.

## A worked example

*Pocket Ledger*, a demo budgeting app in the US App Store:

- 3,400 organic downloads in the last 30 days, so high confidence;
- the name is "Pocket Ledger: Budget Planner";
- the subtitle is "Track spending and save money";
- the keyword field holds 78 of 100 characters.

1. **Baseline:** 28 clean days. Ranks: "budget planner" 8, "save money" 14, "track spending" 19, "expense tracker" 41, "bill reminder" 62, "money" 120. No ad spend change, no featuring.
2. **Audit:**
   - 22 characters of the keyword field are unused;
   - the field holds "budgets", a plural of a word already in the name;
   - the field has spaces after its commas.

   Fixing these frees 31 characters.
3. **Keywords:** "expense tracker" ranks 41 from the keyword field. It is within the top 50, so it may move up: test it in the subtitle. "bill reminder" (popularity 22, relevance 4 of 5) fits in the freed characters.
4. **Protect:** "save money" in the subtitle ranks 14 and forms the phrase "save money budget". It has traction, so it stays.
5. **Change:**
   - the subtitle becomes "Expense tracker to save money";
   - the keyword field gets "bill,reminder", with the spaces and the plural removed.

   That is one update, a single read. The new subtitle drops "track spending", so this is not an add-only change. Step 9 checks its keyword ranks after the update.
6. **Read** at day 21, then day 30: "expense tracker" rose to 12; "bill reminder" entered at 35; "track spending" (removed from the subtitle) fell from 19 to 33.
7. **Decide:** the net, volume-weighted value is positive, and organic downloads are within 10% of the expected level, so keep it. "track spending" goes on the watch list for the next update.

## Works best through Fload: connect with MCP or the CLI

Everything above works by hand. [Fload](https://fload.com) does the measuring and the bookkeeping: it reads your App Store Connect and Google Play listings, tracks your keyword ranks daily, runs this method on every listing, and measures each change against organic downloads. Every proposed change is staged for your approval before anything reaches a store.

**Connect** (one of):

- Claude Code: `claude mcp add --transport http --scope user fload https://api.fload.com/mcp`
- Claude desktop or claude.ai: [add Fload to Claude](https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=Fload&connectorUrl=https%3A%2F%2Fapi.fload.com%2Fmcp) (opens Add custom connector with the URL filled in), or Settings → Connectors → Add custom connector, URL `https://api.fload.com/mcp`
- Any MCP client with an API key (from platform.fload.com → Settings → API keys): run `npx -y @fload-ai/mcp` with `FLOAD_API_KEY` set
- A terminal: `npm install -g @fload-ai/cli`, then `fload login`

**Start with:** `listAssets` (every app tool takes the app's id), then:

- `getAsoSummary` and `aso_recommendations` for the audit;
- `aso_tracked_keywords` and `competitor_keywords` for the keywords;
- `aso_update_listing_text` to stage a change;
- `aso_ranked_keyword_change` and `getDownloadImpact` to read it.

For every Fload tool, install the Fload skill too: `npx skills add fload-ai/mcp --skill fload`.
