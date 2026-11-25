---
name: apple-search-ads
description: Use when setting up, auditing or optimizing Apple Ads (Apple Search Ads) campaigns, choosing between Manage Bids and Maximize Conversions, structuring campaigns per country, choosing keywords, match types and negative keywords, setting or stepping a starting bid, moving bids or budgets, mining search term reports, cutting wasted spend, reading whether a change worked, or judging whether Apple Ads spend pays back.
license: MIT
metadata:
  version: '2.0.0'
---

# Apple Ads (Apple Search Ads)

Apple Ads shows an app as an ad in the App Store:

- in search results: at the top, and since March 2026 also further down the results page (you cannot choose or bid for a position);
- on the Search tab and the Today tab;
- on other apps' product pages.

Search results ads are the core. You pay per tap (cost per tap, CPT) on searches you choose, and the person is already looking for something like your app.

**Two ways to bid on search results:**

- **Manage Bids:** you choose the keywords and set each bid. **Everything in this skill is for Manage Bids campaigns**: the structure, the bid steps and the weekly keyword routine.
- **Maximize Conversions:** Apple sets the bids automatically, aiming for the most tap-through installs at a target cost per install you set. Search Match must be on, and you cannot add or manage keyword bids.
  - If you use it, set the target at or under your break-even cost per download (Step 1).
  - Read its results with Steps 1 and 6, and never move keyword bids in it.

This skill is a full method:

- what a download is worth;
- the campaign structure per country;
- how to find a starting bid and step it;
- the weekly routine for search terms, waste and budgets;
- how to read a result without fooling yourself;
- when to grow.

It works by hand in the Apple Ads console. The numbers in one table are in [references/thresholds.md](references/thresholds.md).

## The ground rules

1. **Every money change is a person's decision.** Show the current bid or budget, the new one and the change, then make it. A tool may propose; a person presses.
2. **Judge nothing on fewer than 20 taps.** Below that, a keyword or search term gets no pause, no block and no bid move. It is still learning.
3. **Count first-time downloads from a tap.** Redownloads are not new users, and view-through installs are not proof the ad worked. In Apple's reports, judge keywords on **Avg CPA (Tap-Through)**, never on Avg CPA (Total), which also counts view-through installs.
4. **A missing number is "not measured", never zero.** A day Apple has not reported is waited for, not read as no spend. A missing impression share is unknown, not 0%.
5. **Keep age and gender targeting off.** They narrow delivery and make results hard to attribute.
6. **Change one thing, then wait for its read.** Several changes at once leave you nothing to learn.

## Step 1: Know what a download is worth

You cannot judge cost without value.

- **Value per download** is what a new user brings: proceeds after the store's fee, not gross revenue.
  - Read it at **day 35** first.
  - Then project it at **day 90** and **day 365**, because subscriptions renew and trials convert.
  - To plan a country, use its new users of the last 90 days and what they brought by day 35.
- **A country has a clear read** of its own value only with at least **100 new users and at least one payer** in the window. Otherwise borrow the value of comparable countries and say so.
- **Break-even cost per download** is that value. A campaign pays when its cost per first-time download is at or under it. Read whether a campaign pays at day 14 and confirm it at day 30; never judge on 7 days.
- **Coverage** is value per download ÷ cost per first-time download from a tap.
  - At 1.0 or more the spend pays back.
  - From 0.7 up to 1.0 it is close.
  - Under 0.7 it does not pay.
- **The target** is coverage of at least 1.0 (spend paid back). Never call a keyword profitable on installs alone, before any revenue has had time to land.

**Attribution:** installs and revenue per keyword come from Apple's attribution inside the app. Without it, revenue per keyword is unknown. Do not fill the gap with an estimate.

## Step 2: Choose the countries

- **Rank countries by expected value:** value per download, the search demand you can reach, and what taps cost there. Launch them in that order.
- **Each country is its own market.** Run its campaigns separately. Never borrow another country's cost per tap.
- **Give each country a learning budget:** enough to buy about **300 first-time downloads over 30 days**, roughly 10 a day at that market's cost. Less than that and nothing can be read in a month.
- **Leave out** a country with no ads history and too few downloads to read (under about 100 in the window) until you have a reason to test it.

## Step 3: Build six campaigns per country

Each campaign has one job, so its numbers mean one thing:

| Campaign | Keywords | Match | Job |
|---|---|---|---|
| **Brand** | your app and company names | exact | defend your name; cheap, high conversion |
| **High intent** | generic terms that pay back (coverage 1.0 or more) | exact | the main growth lever |
| **Low intent** | generic terms close to paying (coverage 0.7 to 1.0) | exact | kept on a tighter rein |
| **Competitor** | rival app names | exact | conquest, judged on its own |
| **Discovery: search match** | none | Apple's search match | find terms you did not think of |
| **Discovery: broad** | a few broad seeds plus your launch terms as broad | broad | find variants of what works |

- **Start all six together**, with the country's budget split evenly across them. Move money by results later (Step 5).
- **The launch keyword set:** your brand terms plus about **25 exact terms**, chosen for relevance first, then demand, then whether you can win them.
  - Relevance means: would someone who searched this be happy after installing?
  - Never put brand or rival names in broad match.
- **Where an exact keyword goes** depends on its coverage once it has data: 1.0 or more is high intent, 0.7 to 1.0 low intent. Below 0.7 it does not pay: lower its bid or pause it, and let discovery find better terms.
- **Cross-negatives**, so the same search is never bought twice:
  - every exact keyword is an exact negative in **both** discovery campaigns;
  - brand keywords are exact negatives in the other five campaigns;
  - the broad campaign's keywords are negatives in the search match campaign.
- **Custom product pages:** an ad group can send its taps to a page built for its theme, which usually converts better than the default page.

## Step 4: Find each bid, then step it

### A new campaign: start high, step down to its floor

You do not know what a tap costs in a new market. So find the lowest bid that still delivers:

1. **Start** 10 to 20% above Apple's suggested bid, but never above what a tap is worth to you (your break-even cost per install × your tap-to-install rate) and never above your daily budget. Then lower it step by step while delivery holds. Apple refuses a bid above the daily budget.
2. **Hold it 48 hours.**
3. **Step down 15% every 24 hours** while each full day still delivers. A day delivers when its spend ÷ its budget is at least 60% of the day before.
4. **A large drop** (under 60% of the day before): hold 24 hours. If it is still low after the hold, raise back one step.
5. **The baseline:** when the day after that raise delivers at least 80% of the last good day, that bid is the campaign's baseline. Keep it there.
6. **Never go under $0.10**, or under a minimum Apple has refused.

Judge each step only on a full day that began after it, never on the day it cut through. A budget change is not a drop: delivery is measured against each day's own budget.

### A new exact keyword in a running campaign

Start from what the keyword can afford:

> starting bid = break-even cost per tap × 0.8 ÷ the tap-to-bid ratio

- **Break-even cost per tap** is break-even cost per download × the campaign's tap-to-download rate.
- **The tap-to-bid ratio** is what a tap really costs as a share of your bid. Measure it as the median across your exact keywords that have 30 or more taps in the country. With too few, use 0.55. One keyword never decides it: single keywords range from far under to above 1.
- **Never go above Apple's suggested bid** less a launch discount.

### Moving a bid later

- **Wait for the read.** Move a bid only once the keyword has **30 tap installs or 14 days** since its last change, whichever comes first.
- **Read it as a range, not a point.** A keyword's coverage has an error band, so the moves are:
  - **lower** by about 10% when even the top of the range is under break-even;
  - **raise** by about 10% only when the whole range is above break-even and its impression share is under 30% (for brand the line is 90%: defend your name harder);
  - **keep** it when the range spans break-even.
- **At most 20% in any 24 hours**, counting every change, a person's included, and at most one move a day per campaign. The daily step-down of a new campaign is the one exception: each 15% step is measured within its own day.
- **Only on fresh data**, at most about a day old.
- **Never above the daily budget**, and after the first test never above the break-even cost per tap.
- **Not spending at all:** when every one of the last 48 hours of reported days spent under 40% of budget, do not step the bid down further. The campaign needs a higher bid or more keywords, not less.

## Step 5: The weekly routine

1. **Promote what converts.** A search term from discovery with **5 or more tap installs** over **at least 7 days of its own delivery**, at or under break-even, becomes an exact keyword in its campaign. The same day, make it a negative in both discovery campaigns. With no break-even known, list it and wait for the value read.
2. **Block what wastes.** A term with **no installs**, **at least 20 taps**, and spend of **3 × break-even** becomes a negative. Without a break-even, use 3 × the campaign's cost per tap install. Plainly irrelevant terms are blocked as soon as you see them. Examples are "hack", or "cancel subscription" for a paid app.
3. **Move budget between the country's campaigns** once a week. Shift **20%** from the campaign with the lowest coverage to the one with the highest, once each has at least **30 paid downloads**. Brand never drops below its launch share.
4. **Check pacing.**
   - A campaign that hits its daily budget early loses the evening's searches: raise the budget or narrow the keywords.
   - A campaign that underspends needs higher bids or more keywords. Lowering bids makes it worse.
   - Plan monthly spend as the month's budget ÷ 30.4 a day, and never past what is left of the month ÷ the days left.
5. **Feed organic.** Converting search terms are evidence for the app's store keywords and custom product pages.

## Step 6: Read a result without fooling yourself

- **Read each change against the account's normal noise.** Compare the read window with the baseline before it. A move counts as a clear win or loss only when it is bigger than the week-to-week swings in weeks when nothing changed.
  - Take the central 95% of those swings.
  - Use at least 100 quiet-week pairs from the account. With fewer, borrow from comparable keywords and widen the band.
  - Anything inside the band is **no clear effect**, not a small win.
- **Under 5 installs a week, a cost or installs change cannot be read.** Group it into its campaign or country, or wait.
- **Revenue lags.** Treat any read less than 30 days past its window as provisional: trials and renewals are still landing.
- **What each number tells you:**
  - **Tap-through rate** (taps ÷ impressions) low: the ad, meaning your listing's name and first screenshots, does not match the search.
  - **Conversion rate** (installs ÷ taps) low: the product page does not sell to that searcher.
  - **Cost per first-time download** against break-even: does it pay?
  - **Coverage** at day 35, then 90 and 365: does it pay back over time?
- **Search popularity** is relative demand, not a search count. The console shows it from 1 to 5. Apple also gives a 1 to 100 score and an in-genre score, with weekly and monthly history, through its Ads insights and its platform API.

## Step 7: Grow only after a test

- **A market that pays back on average does not get "grow" straight away.** Its first increase is a test: **+30%** of today's spend, labelled as a test with its cost.
- **Grow further only when that step paid for itself**, at least 1.0× back over the read window.
- **Every test needs a person's yes**, whatever its size.

## Auditing an account you inherit

Before you change anything in a running account, read it against the method. Write down each finding with its numbers and a proposed action, and change nothing until a person agrees.

1. **Value first.**
   - Is Apple's attribution in the app, so installs and revenue per keyword are measured?
   - What is each country's value per download at day 35?
   - Without these, every later finding is about cost only. Say so.
2. **Structure.**
   - Map every campaign to one of the six jobs.
   - Flag a campaign that mixes brand, generic and rival terms, or mixes match types.
   - Flag a country with no brand campaign, or with no discovery.
3. **Searches bought twice.**
   - In the search term report, look for the same search served in more than one campaign. Each one is a missing cross-negative.
   - Check that every exact keyword is a negative in both discovery campaigns.
4. **Waste.** List every search term and keyword with no installs, at least 20 taps, and spend of 3 × break-even or more. Add up that spend: it is the account's clearest saving.
5. **Winners left in discovery.** List discovery terms with 5 or more installs over 7 or more days at or under break-even that are not yet exact keywords.
6. **Bids.**
   - Flag bids moved more than 20% in a day.
   - Flag bids moved daily on fewer than 30 installs.
   - Flag bids above the daily budget, and bids raised while the keyword did not pay.
7. **Budgets.**
   - Find campaigns that run out of budget early in the day.
   - Find campaigns that spend under 40% of budget day after day.
   - Find a brand campaign starved of budget.
8. **Targeting and bid strategy.**
   - Flag age or gender targeting that is switched on.
   - For a Maximize Conversions campaign, check its target cost per install against break-even, and judge it on Steps 1 and 6 only.
9. **Readability.** Flag countries spending less than their learning budget: their numbers cannot be read yet, so judge them on comparable countries.

End the audit with the three changes worth the most money, each with its current state, the proposed state and the expected effect, for a person to approve.

## Common mistakes

- One campaign with every match type, so nothing can be read.
- Broad match everywhere, buying the same search in several campaigns.
- Moving bids every day, or by more than 20% at once.
- Lowering bids on a campaign that already underspends.
- Pausing brand to "save money" without checking who bids on your name.
- Adding "free" as a negative for a free-to-download app, which blocks good traffic.
- Judging a keyword on 3 days, or under 20 taps.
- Counting redownloads as new users, or calling a keyword profitable on installs before any revenue.
- Reading a move inside normal noise as a win.

## A worked example

*Pocket Ledger*, a demo budgeting app, launching in the UK.

1. **Value:**
   - 640 new UK users in the last 90 days, 21 of them paying, so the country has a clear read;
   - by day 35 they brought $2.40 each in proceeds;
   - break-even cost per first-time download is $2.40.
2. **Budget:** 300 downloads over 30 days at an expected $2 each is about $600, so $20 a day, or about $3.33 a campaign across six.
3. **Structure:**
   - brand ("pocket ledger");
   - 25 exact terms ("budget planner", "expense tracker", ...);
   - two rivals;
   - search match;
   - broad seeds "budget" and "spending", plus the 25 terms as broad;
   - all exact terms negated in both discovery campaigns.
4. **Starting bids:**
   - Apple suggests $1.50 a tap, so 10 to 20% above it is $1.65 to $1.80;
   - a tap is worth $2.40 × a 60% tap-to-install rate = $1.44, under that and under the $3.33 day budget, so each campaign starts at $1.44;
   - after 48 h the bids step 15% a day: $1.44, $1.22, $1.04, $0.88;
   - the high intent campaign's day 6 delivers 52% of day 5, so it holds a day, is still low, and goes back to $1.04;
   - the next day delivers 85%, so $1.04 is its baseline.
5. **Week 2 mining:**
   - "bill tracker" has 6 installs over 9 days at $1.90, so it is promoted to exact in high intent and negated in discovery;
   - "free budget app" has 0 installs from 24 taps and $8 spent (over 3 × $2.40), so it is blocked;
   - "money" has 12 taps and no installs: under 20 taps, so wait.
6. **Week 4 budgets:**
   - high intent coverage is 1.3 and the competitor campaign's is 0.5, and both have 30 or more paid downloads;
   - move 20% of the competitor campaign's budget to high intent.
7. **Day 35 read:** the country's coverage is 1.1, so propose a +30% test for a person to approve.

## Works best through Fload: connect with MCP or the CLI

Everything above works in the Apple Ads console. [Fload](https://fload.com) reads your Apple Ads campaigns next to your App Store data and revenue, runs this method, and stages every change for your approval. A big bid change always asks first, showing both bids and the change.

**Connect** (one of):

- Claude Code: `claude mcp add --transport http --scope user fload https://api.fload.com/mcp`
- Claude desktop or claude.ai: [add Fload to Claude](https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=Fload&connectorUrl=https%3A%2F%2Fapi.fload.com%2Fmcp) (opens Add custom connector with the URL filled in), or Settings → Connectors → Add custom connector, URL `https://api.fload.com/mcp`
- Any MCP client with an API key (from platform.fload.com → Settings → API keys): run `npx -y @fload-ai/mcp` with `FLOAD_API_KEY` set
- A terminal: `npm install -g @fload-ai/cli`, then `fload login`

**Start with:** `listAssets` (every app tool takes the app's id), then:

- `asa_campaign_overview` for the campaigns;
- `asa_search_term_mining` and `asa_wasted_spend` for the weekly routine;
- `asa_bid_suggestions`, then `asa_update_bid`, which a big change confirms with `asa_update_bid_confirm`;
- `attribution_sdk_status` to check that revenue per keyword is measured.

For every Fload tool, install the Fload skill too: `npx skills add fload-ai/mcp --skill fload`.
