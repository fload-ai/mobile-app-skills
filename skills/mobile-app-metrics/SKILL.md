---
name: mobile-app-metrics
description: Use when reading or reporting a mobile app's downloads, organic downloads, revenue, proceeds, subscriptions, trials, retention, conversion, ad spend or ratings on the App Store or Google Play, building an app dashboard or weekly report, judging whether a drop is real, explaining why a metric moved, or adding app metrics up over days, countries, sources or apps.
license: MIT
metadata:
  version: '2.0.0'
---

# Mobile App Metrics

The job is to say how an app is doing in numbers that are right: downloads, organic downloads, conversion, proceeds, subscriptions and ratings, rolled up the right way, compared fairly, and with every gap said out loud. Most wrong answers about an app come from five mistakes: adding up a number that must not be added, averaging a ratio, putting the wrong number on top of a ratio, calling a missing number zero, and trusting the newest days before they are in.

This is the method we use for every app's numbers, on both stores, with ad networks and subscription data alongside.

## The loop

Run it every week, and again whenever someone asks "why did this move?".

1. **Pull** each metric as a daily series, per source (each store, each ad network, the subscription data), never already rolled up.
2. **Label each metric's kind** (step 1 below) before you touch it.
3. **Cut the unfinished days**: stop each series at its last complete day (step 3).
4. **Roll up** by kind, and **recompute ratios** from their parts (step 2).
5. **Compare** with the periods that are fair to compare (step 6).
6. **Judge** whether a move is real before you explain it (how to judge, below).
7. **Explain** what is real by splitting it and lining it up with events.
8. **Report** with each number's kind, its days covered, and what is unknown.

**What to pull, per source:**

| Source | Pull | Kinds |
|---|---|---|
| App Store Connect | impressions, product page views, product page downloads, downloads by source type and country, redownloads, sales, proceeds, crashes | unique, flow |
| Google Play Console | installs, store listing visitors, store listing acquisitions, revenue, crashes and ANRs, active devices | flow, unique |
| Each ad network | spend, impressions, taps, installs, first-time downloads after a tap, by campaign and country | flow |
| Subscription data | active subscriptions, active trials, new trials, MRR, trial conversion, churn, refunds | level, flow, rate |
| The store's ratings | average rating and number of ratings, per country | level, cumulative |

## 1. Know each metric's kind before you total it

Every daily number is one of five kinds, and each kind has one correct way to roll up over a week, a month or a year.

| Kind | One day's number is | Over a period | Examples |
|---|---|---|---|
| **Flow** | that day's count or amount | **add the days up** | downloads, redownloads, proceeds, sales, refunds, new trials, crashes, ad spend, ad impressions, ad taps, ad installs |
| **Level** | a snapshot at that moment | **take the last value** of the period | active subscriptions, active trials, MRR, ARR, rating average |
| **Cumulative** | a running total to date | **take the last value**; subtract the start for the period's own change | total ratings count, subscriptions churned to date |
| **Rate** | a ratio between 0 and 100% | **recompute** from its parts (step 2); with only the daily rates, average them (weighted by each day's size if you can) and say so | conversion rate, trial conversion, churn, retention, tap-through rate |
| **Unique** | distinct people or devices that day | **neither add nor take the last** (below) | daily active users, active devices, paying users, store impressions, product page views, store listing visitors |

**Unique numbers are the trap.** A person active on 20 days of the month appears in 20 daily counts, so adding the days counts them 20 times (a month of added daily actives overstates about 30 times). A true monthly unique can't be rebuilt from daily uniques at all. So:

- For a stand-alone figure ("how many active devices this month?"), report the **average daily** count, and call it that.
- As the bottom of a ratio (crashes per active device, downloads per page view), **add the days up**: the ratio is then "per device-day" or "per page-view day".
- If you need true monthly uniques, they must come from the source as a monthly number.

Store impressions and product page views are counted as unique devices per day, which is why they sit in Unique. Ad impressions are a count of ads shown, so they are a flow.

## 2. Ratios: a ratio of totals, with the right top

A period's ratio is the period's total on top divided by the period's total on the bottom, never the average of the daily ratios.

**Put the right number on top.** On the App Store:

- **Product page conversion** = product page downloads ÷ product page views. Not all downloads ÷ page views: many downloads come straight from search results without a page view, so all downloads on top makes conversion look far too high.
- **Impression conversion** = downloads ÷ impressions. App Store Connect's own conversion rate is total downloads (first-time downloads plus redownloads, plus pre-orders) ÷ unique device impressions, not all impressions. Say which one you report.
- **Cost per install** = ad spend ÷ ad installs for the same network and days.

**Days where the bottom is zero** need a decision, and it depends on the ratio:

- **Cost ratios count every day.** Spend on a day with no installs is real money spent, so it stays in. Skipping those days makes cost per install look much cheaper than it was.
- **Ratios where the top implies the bottom leave such days out.** A crash happens on an active device, a product page download follows a page view. A day with the top and no bottom is a gap in the data, not a real ratio.

**Never mix sources inside one ratio.** One ad network's spend must never be divided by another network's installs, and one source's payer count must never divide another source's proceeds. Compute each source's ratio from its own numbers, count a source only over the days it reports both parts, then combine totals, not ratios.

**Stop at the last day that has both parts.** App Store page views arrive about a day after product page downloads, and on Google Play listing visitors arrive about a week after installs. So the newest days have downloads but no page views yet. Counting them makes conversion read too high. Stop the ratio at the last day with both.

## 3. Unknown is not zero, and the newest days aren't in

- A day with no data is **unknown**. A metric the source never reported is unknown. Say so: "no data for 3 to 5 March", never "0 downloads". Zero is a measured value.
- **The stores report 0 for days they haven't finished.** A 0 for a recent day is not final. As a rule of thumb, trust a 0 only once its day is about a week old.
- **Store reports usually arrive a day or two late; don't judge the last 2 days.** Some sources run longer:

| Source | How far behind it usually runs |
|---|---|
| App Store figures by country | up to 4 days |
| App Store product page views | about a day after product page downloads |
| Google Play installs and active devices | 2 to 3 days |
| Google Play store listing visitors | 6 to 10 days |
| Google Play per-listing report (listing acquisitions and visitors) | about 7 days |
| Google Play revenue | up to 4 days |

- **Trial conversion is dated by the day the trial started**, so a day only settles once its trials have ended: about 5 days later for 3-day trials, 9 days for 7-day trials, longer for longer trials. Its first value is often a misleading 100% from one early buyer. Don't read the newest ten days or so of trial conversion, or of lifetime value, as a trend.
- **Compare only complete periods.** A week or month still running is left out of a comparison, not compared as if it were whole.

## 4. The store numbers, defined

**App Store**

- **Impressions → product page views → product page downloads** is the funnel on the store's own pages. Impressions and page views are unique devices per day.
- **Downloads** (first-time) and **redownloads** are separate counts; a "total downloads" figure may hold both.
- **Sales, proceeds, refunds, in-app purchases** are flows; **active subscriptions** and **active trials** are levels.
- **Crashes** are a count. A crash rate needs a bottom from the same days (crashes per active-device day).

**Google Play**

- **Store listing visitors**: people who visited the listing without already having the app, per day. Daily uniques.
- **Store listing acquisitions**: people who installed from the listing who didn't have the app on any device. Smaller than all store acquisitions, which also count installs that never opened the listing.
- **Listing conversion** = store listing acquisitions ÷ store listing visitors, over the days both are reported.
- **ANRs** (app not responding): a count, which you add up. Google's ANR rate is a different number, the share of daily users who hit one; don't divide a count by active devices and call it Google's rate.

## 5. Downloads: organic, paid and new

- **First-time downloads vs redownloads.** Only first-time downloads are new users.
- **Source types** on the App Store: App Store search, App Store browse, web referrer, app referrer and others. Each is a slice of the total, so the slices add up to it. Some exports give one split at a time (by source or by country, not both); check what yours allows before you build a table across both.
- **Organic search downloads** = App Store search downloads minus Apple Ads installs from search results ads, per day, floored at 0, then added up over the period. This is the number to watch for store optimization: browse and referrer downloads are not organic search.
- **All organic downloads** = first-time downloads minus all ad installs, per day, floored at 0. A secondary number; it can be split by country.
- **Ad installs include redownloads and view-through installs** (people who saw an ad, didn't tap, and installed later). New users from ads are the **first-time downloads after a tap**. Never add those two numbers together: one contains the other.
- If no ad network is connected, paid is 0. If the store side is missing, organic is unknown, not 0.

## 6. Money, subscriptions and ratings

**Money**

- **Sales vs proceeds.** Sales is what customers paid; proceeds is what the developer receives after the store's commission and taxes. They are the same purchases in two numbers: report one and say which. Never add both.
- **Convert currencies before adding.** Bring every amount to one currency at the day's rate, then add.
- **Refunds are negative.** Subtract them in the period they happen.

**Subscriptions**

- **MRR**: every active subscription normalised to a month (an annual plan counts 1/12). A level: "MRR for the year" is the MRR at the end of the year, not twelve readings added up, which reports 12 times the real figure.
- **Trial conversion**: trials that became paid ÷ trials that ended, dated by trial start (step 3).
- **Churn**: subscriptions that ended ÷ active at the start of the period.
- **Retention** is per cohort: of the people who started on day 0, the share still active on day 1, 7 and 30.
- **Lifetime value** is an estimate until cohorts are old enough. Say how it was estimated.

**Ratings**

- An average rating across countries or stores is **weighted by each one's number of ratings**. Never add ratings, and never take the plain mean of the country averages.

## 7. Comparing periods

- **Like with like**: the same weekdays, and the same weeks last year for seasonal apps. Week on week alone misleads around holidays.
- **Same days on both sides** of a ratio and of a comparison.
- **Matching the consoles.** Your numbers won't always match what a store console shows, for known reasons:
  - Google Play's store listing pages switched to click-based measures in June and July 2026, so the console's click-through rate is not listing acquisitions ÷ listing visitors. Don't compare the two.
  - Apple's usage numbers (sessions, active devices, retention) only count people who agreed to share data with developers, so they undercount real use.
  - App Store Connect's own conversion rate is total downloads (first-time plus redownloads, plus pre-orders) ÷ unique device impressions; say which conversion you mean.

## 8. Explaining a change

Only once the change is judged real (below):

1. **Split it** by source type, country, store, platform and app version. A drop that sits in one country or one source has one cause; a drop spread evenly across all of them usually has an outside cause (a season, a store-wide change).
2. **Split organic from paid.** A fall in all downloads with organic search steady is an ads story; the reverse is a search story.
3. **Line it up with events**: releases, listing changes (name, subtitle, keywords, screenshots), ad changes, price changes, featuring, outages, a competitor's launch.
4. **Check the funnel stage.** Fewer impressions means people saw the app less (search rank, ads). The same impressions with lower conversion means the listing or the price persuaded fewer of them.
5. **Say what is not known**, and what would settle it (another week of data, a test).

## How to judge a result

**Is a drop real?** Before explaining a fall in organic downloads, run these in order:

1. **Enough volume?** Skip apps under about 300 organic downloads in 30 days (10 a day): below that, day-to-day noise moves a week by more than 10%.
2. **Flag:** the last 7 days against the 28 before, as a daily pace. A fall of 10% or more is a flag: look, don't alarm.
3. **Alarm:** the last 30 days are at least 10% below the 30 before **and** at least 10% below the same 30 days a year earlier. Both, so a normal seasonal dip doesn't alarm.
4. Leave out known spikes and event days (a featuring, an outage) before comparing.

**For ads**, a week with fewer than 5 installs can't be read: a change in cost or installs that small is noise.

**Before a number leaves your hands**, check:

- A rate over 100% means the wrong top (usually all downloads over page views).
- A monthly active figure far above the daily figures means uniques were added up.
- A yearly MRR far above monthly MRR means a level was added up.
- A recent 0 means an unfinished day.
- A ratio's two parts cover the same days.

## Hard gates

Stop and fix before reporting if any of these is true:

- Daily uniques added into a stand-alone period total.
- A level (MRR, active subscriptions) added up over days.
- Daily ratios averaged when their parts were available.
- One source's numbers divided by another source's.
- An unread or unfinished day reported as 0.
- Sales and proceeds added together, or currencies added before converting.
- Ratings added, or country averages averaged without weights.
- A running week or month compared as if it were complete.

## Common mistakes

- Adding daily active users into "monthly users".
- Adding twelve months of MRR.
- Averaging daily conversion rates.
- Conversion with all downloads on top.
- Counting the newest days of downloads against page views that haven't arrived.
- Adding ad installs and first-time ad downloads together.
- Calling the newest, half-reported day a drop.
- Reading last week's trial conversion as final.
- Treating the console's numbers and your own as the same measure.

## Worked example: a weekly report

Quillnook, a demo journaling app on both stores. The report is written on Thursday 26 November for the week Monday 16 to Sunday 22, so every day of that week is at least 4 days old. The numbers below are the App Store side, plus what Google Play hasn't sent yet.

**Downloads (flow, added up).** First-time downloads 1,400 this week, 1,520 last week: down 7.9%.

**Organic search (flow, computed per day).** App Store search downloads 900, Apple Ads search results installs 260, so organic search is 640 (no day went below 0). Last week 980 and 240, so 740: down 13.5%.

**Is it real?**

- Volume: 3,040 organic search downloads in the last 30 days, well over 300.
- Flag: the 28 days before this week averaged 730 a week (2,920 ÷ 4). 640 against 730 is down 12.3%: a flag.
- Alarm: the last 30 days (3,040) against the 30 before (3,250) is down only 6.5%. Not an alarm.
- So: worth a look, not a crisis. Splitting by country shows the fall is all in the US, and the subtitle changed on Tuesday. That is a lead, not a proven cause.

**Product page conversion (rate, recomputed).** Page views arrive about a day after downloads, and Sunday is 4 days old, so both weeks are whole. Product page downloads 700 ÷ product page views 5,830 = 12.0%. Last week: 650 ÷ 5,120 = 12.7%.

**Active devices (unique).** Average 4,300 a day. Adding the seven days would say 30,100, which is wrong.

**Subscriptions (level, last value).** Active subscriptions on Sunday: 2,140. MRR on Sunday: 9,850 in the report's currency.

**Proceeds (flow).** 6,200 after converting every currency at the day's rate, with 90 of refunds subtracted.

**Trial conversion.** Trials started in the last 10 days are still settling. The latest settled week, trials started 9 to 15 November (the app's trial is 7 days), converted at 41% of 220 trials that ended.

**Ratings (weighted).** US 4.7 from 1,200 ratings, UK 4.2 from 300. Weighted: (4.7 × 1,200 + 4.2 × 300) ÷ 1,500 = 4.6. The plain mean of the two, 4.45, would be wrong.

**Ads.** Spend 780 ÷ installs 260 = 3.00 per install. Of those installs, 190 were first-time downloads after a tap: the new users ads brought, at 780 ÷ 190 = 4.11 per new user.

**Unknown this week:** Google Play listing visitors after the 17th (not published yet).

**The report as sent:**

> **Quillnook, week of Mon 16 to Sun 22 Nov**
> - Downloads 1,400 (last week 1,520, down 7.9%).
> - Organic search downloads 640 (down 13.5%). Flagged: 12.3% below the 4 weeks before. Not an alarm: the last 30 days are only 6.5% below the 30 before. The fall is in the US; the subtitle changed on Tuesday. Watching another week.
> - Product page conversion 12.0% (last week 12.7%).
> - Active subscriptions 2,140 and MRR 9,850, both on Sunday.
> - Proceeds 6,200, refunds subtracted.
> - Trials started 9 to 15 Nov converted at 41%. Newer trials are still settling.
> - Rating 4.6 (weighted across the US and the UK).
> - Ads: 3.00 per install; 190 new users from ads, 4.11 each.
> - Not known yet: Google Play listing visitors after the 17th.

Each line was rolled up by its kind (added up, last value, recomputed or weighted) or marked unknown.

## Works best through Fload: connect with MCP or the CLI

All of this can be done with exported reports. [Fload](https://fload.com) brings App Store Connect, Google Play, ad networks, subscription revenue and product analytics into one place. It rolls flows, levels and ratios up by their kind, recomputes ratios from their parts per source, computes organic downloads, and leaves unread days unknown in its daily series; check a ratio's newest days yourself. For daily uniques over weeks or months, apply the unique rule above.

**Connect** (one of):

- Claude Code: `claude mcp add --transport http --scope user fload https://api.fload.com/mcp`
- Claude desktop or claude.ai: [add Fload to Claude](https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=Fload&connectorUrl=https%3A%2F%2Fapi.fload.com%2Fmcp) (opens Add custom connector with the URL filled in), or Settings → Connectors → Add custom connector, URL `https://api.fload.com/mcp`
- Any MCP client with an API key (from platform.fload.com → Settings → API keys): run `npx -y @fload-ai/mcp` with `FLOAD_API_KEY` set
- A terminal: `npm install -g @fload-ai/cli`, then `fload login`

**Tools:** `listAssets` first (every app tool takes the app's `assetId`); `discoverMetrics` and `getMetricGuidance` for what exists; `getMetrics` for a daily series and its total; `getComputedMetrics` for ratios from their parts; `getDownloadImpact` for a listing change against the same weeks last year; `getDashboardOverview` for the portfolio. For every Fload tool: `npx skills add fload-ai/mcp --skill fload`.
