---
name: launch-an-app
description: Use when publishing a new app or a major update to the App Store or Google Play, preparing App Store Connect or Play Console for a first release, filling in App Privacy, the age rating or Data safety, getting through App Review, answering a rejection, or planning what to do in the first weeks after launch.
license: MIT
metadata:
  version: '2.0.1'
---

# Launch an App

The job is to take a built app to the stores: every form true, every store step done in order, through review on the first or second try, and set up to grow from its first week. The numbers it moves: the days from "built" to "live", the number of review rounds, and the first weeks' downloads and ratings.

This skill is the method we use: walk the store's steps in a fixed order, know for every step who acts next, write each answer from what the app really does, check Apple's common rejections before you submit, and answer every point App Review raises.

## The loop

1. **Write down what the app does, once** (below).
2. **Walk the steps in order** for each store, and keep a state on each.
3. **Every day**, push the first step that isn't done.
4. **Before submitting**, run the check against Apple's common rejections and fix every failure.
5. **When review answers**, release, or answer every point and go round again.
6. **After launch**, switch to growing: reviews, search, ads, measurement.

## How to run a launch

Treat the launch as a list of steps in order. At any moment each step is in one of these states:

- **Done.**
- **To do**, and you know who acts next: you, the store, or whoever is helping you.
- **Working**: someone is on it (a build processing, a review under way).
- **Blocked**: an earlier step comes first.
- **Stopped**: the store sent it back, or it failed.
- **Unknown**: not checked yet, or the store gives no way to check it.

**Keep a status board**, one row per step, and update it every day:

| Step | State | Who acts next | Note |
|---|---|---|---|
| Team | done | | |
| App record | done | | name reserved |
| Listing | to do | you | German description needs the Terms of Use link |
| Screenshots | working | you | 6.9-inch set in progress |
| Build | working | Apple | processing since 10:00 |
| App Review | blocked | | waits on the build |

The first row that isn't done is the one to push today. A "working" row that hasn't moved in a day becomes "to do" for you: find out why.

**Plan the calendar backwards from the launch day:**

- An organization's Apple Developer Program enrollment can take days to weeks; a person's is usually quicker.
- A Google Play personal account created after 13 November 2023 needs a closed test of at least 14 days.
- App Review usually answers within a day or two, but plan for one round of feedback.
- A Google Play review of a new app can take several days.
- Leave two or three days between approval and the launch day, so a late fix doesn't move the date.

**Write down what the app does, once,** in a few plain sentences: what it does, who it's for, what it keeps and what leaves the phone, how it makes money. The listing, the privacy answers, the age rating and the keyword research all start from it, so they agree with each other and with the app.

## The store's field limits

Count the App Store's limits as App Store Connect shows them: emoji and flags can count as more than one character.

| Field | App Store | Google Play |
|---|---|---|
| Name (title) | 30 | 30 |
| Subtitle | 30 | none |
| Short description | none | 80 |
| Keywords | 100 (comma separated) | none |
| Promotional text | 170 | none |
| Description | 4,000 | 4,000 (full description) |

## App Store: the steps, in order

1. **Team.** An Apple Developer Program membership, on your own account. An organization account needs the company's legal registration details and takes longer to approve, so start early. Accept the agreements in App Store Connect. If the app sells anything, the paid apps agreement also needs its **tax forms and bank account** filled in, or nothing can go on sale.
2. **The app's record in App Store Connect**: a bundle ID, the app's name (unique on the store), primary language and SKU. Creating it early also reserves the name.
3. **What the app does**: the few sentences above.
4. **The listing**: name, subtitle, keywords, description and promotional text, researched for search (see the `app-store-optimization` skill), within the limits above.
5. **Screenshots** for the required sizes (the largest iPhone size, and iPad if the app runs on iPad), from the real app.
6. **In-app purchases and subscriptions**: each product with its price, its display name and a review screenshot. The review screenshot is a .png or .jpeg with no transparency, at one of the iPhone or iPad screenshot sizes.
7. **The details**:
   - **App Privacy.** These answers are a statement you make, so never answer blind. Go type by type and write down why each one is a yes or a no. Only data that leaves the phone counts; what stays on the device is not declared. Start from what every SDK in the app sends (its own privacy documentation says), then add what the app itself sends. Never declare less than the SDKs send. Say whether each type is linked to the person and whether it is used for tracking.
   - **Age rating.** Answer each question from what the app does, with your reason, never by guessing. Apple's ratings are now 4+, 9+, 13+, 16+ and 18+ (12+ and 17+ were removed), with new questions: answer the current set.
   - **Kids.** Only choose the Kids category if the app is made for children; it brings stricter rules on ads, data and links out of the app.
   - **Regulated medical device status.** Apple asks apps in the EU and EEA, the UK and the US, in particular any app in Health & Fitness or Medical or with frequent medical information in its age rating. Most apps answer No; a Yes needs regulatory details for each region.
   - **EU trader status.** To be on the App Store in the EU, say whether you are a trader under the Digital Services Act. A trader's address, phone and email are shown on the listing there.
   - **Category, pricing and availability, content rights, export compliance** (encryption).
   - **A privacy policy URL and a support URL** (both required), on a real page that names the app.
   - **App Review information**: a contact, and a working demo account if the app needs a sign-in. Notes for anything the reviewer can't see on their own.
8. **The build**: upload it, wait for it to process, test it in TestFlight, then attach it to the version.
9. **Check Apple's common rejections before you submit** (below). Fix every failure first.
10. **Submit for review**, and choose the release: automatic on approval, manual, or on a date. For updates, a phased release rolls out over 7 days and can be paused for up to 30 days in total.

### The check before you submit

| Guideline | What to check |
|---|---|
| 3.1.2 Subscriptions | An app with auto-renewing subscriptions links its Terms of Use (EULA) in the description **of every language** the listing has, or sets a custom EULA in App Store Connect. Inside the app, the paywall shows the price, the period, and links to the Terms of Use and the privacy policy. A missing link in one language is enough for a rejection. The detailed list comes from Schedule 2 of the developer agreement, which 3.1.2(c) points to. |
| 2.1 App completeness | No crashes, no broken links, no placeholder content; the demo account works and won't expire during review. |
| 2.3 Accurate metadata | Screenshots and text match the app as it is. |
| 3.1.1 In-app purchase | Digital content and features are sold only through Apple's in-app purchase, with Restore purchases. |
| 4.2 Minimum functionality | The app does enough on its own; it isn't a thin wrapper of a website. |
| 4.3 Spam | The app is clearly its own app, not a near-copy of another or of a template. |
| 5.1.1 Data collection | It asks only for data it needs; an app with accounts lets people delete them in the app. |

Apple says over 40% of unresolved issues fall under 2.1, so it is the most common; the others are frequent, in no particular order.

A finding is either passed, worth a look, or a failure. Don't submit with a failure.

### When App Review sends it back

1. Read Apple's message in full, and list **every point it raises, in Apple's own words**, with the guideline it names. Never drop a point, even one that looks minor; a guideline named with no clear point still gets its own line.
2. For each point, decide: a change to the app, a change to the listing (kept within the field's limit), an answer to the reviewer, or something only you can decide.
3. Fix each one, then reply in App Store Connect saying what changed, point by point.
4. If you believe the reviewer is mistaken, explain calmly with specifics. An appeal to the App Review Board is the last step.

**A reply to App Review**, point by point:

> Thank you for the review. We've addressed each point:
> 1. Guideline 2.1 ("the app crashed when we tapped Add Plant without a photo"): fixed in build 1.0 (5). Adding a plant without a photo now uses a placeholder leaf.
> 2. Guideline 3.1.2 ("the Terms of Use link is missing from the description"): added to the description in every language.
> The new build is attached to the version.

Quote Apple's words for each point, say what changed and where, and don't add anything Apple didn't ask about.

### Major updates

An update goes through the same review, with fewer forms:

- Write the "What's New" text for the version: what changed for the person, in plain words.
- Review the listing and screenshots: do they still match the app as it is now?
- If the update changes what data leaves the phone (a new SDK, a sign-in), update App Privacy and Data safety **before** submitting.
- New in-app purchases go to review with the build that offers them.
- Release with a phased release on the App Store and a staged rollout on Google Play, and watch crashes before raising it.

## Google Play: the steps, in order

1. **Access**: your Play Console developer account, with identity verification. To sell anything, set up a **payments profile**. **Closed test:** personal developer accounts created after 13 November 2023 need 12 testers opted in for 14 days in a row before production. Plan those two weeks from the start.
2. **The app in Play Console**: created with its name and default language.
3. **What the app does**: the same few sentences as for the App Store.
4. **The store listing**: name (30), short description (80), full description (4,000).
5. **Graphics**: icon, feature graphic, phone screenshots, and tablet screenshots if it runs on tablets.
6. **Products**: in-app products and subscriptions, with prices.
7. **App content**:
   - privacy policy, app access (sign-in details for review), ads, content rating, target audience;
   - **Data safety**: what is collected and shared, including by every SDK (the same facts as your App Privacy answers). If the app has accounts, a **web link where people can ask to delete their account and data**;
   - the extra declarations that apply: financial features, health, government;
   - **Families policy** if children are in the target audience.
8. **The build**: an app bundle signed with Play App Signing, built for the target API level Google currently requires. Read the **pre-launch report** Play Console makes from it on its own (crashes and problems on real devices; it's optional, not a requirement) and fix what it finds.
9. **Release**, in this order: an internal test; then the closed test (for personal accounts created after 13 November 2023, the 14 days with 12 testers); then apply for production access; then production with a **staged rollout** (a share of users first, raised while crash rates stay normal).

Review of a new app can take several days. A policy rejection names the policy: fix it and resubmit.

**Before sending a Google Play release to review, check:**

| Area | What to check |
|---|---|
| Data safety | matches what the app and every SDK collect and share; the account deletion link works if the app has accounts |
| App access | the review sign-in works and won't expire |
| Target audience | if children are included, the Families policy rules are met (ads, data, content) |
| Declarations | every one that applies is filled in (ads, financial features, health, government) |
| Listing | text and screenshots show the real app; no claims the app can't back up |
| Payments | digital goods sold through Google Play Billing |
| Pre-launch report (optional) | no crash or blocking problem left unfixed |

## After launch: the first weeks

- **Reviews**: read and reply daily in launch week (see the `app-review-replies` skill).
- **Search**: audit the listing once real search data arrives (see the `app-store-optimization` skill).
- **Ads**: if you run Apple Ads, start with your brand terms plus up to 25 exact-match terms. Give each country a learning budget sized to buy about 300 paid downloads (downloads after an ad tap, first-time or redownload) over 30 days (about 10 a day): below that, results can't be read. Read what pays at day 14 and confirm it at day 30; never judge on 7 days. Then grow what pays (see the `apple-search-ads` skill).
- **Attribution**: know which downloads came from ads and which came from search.
- **A weekly report** of downloads, proceeds, trials and ratings, rolled up the right way (see the `mobile-app-metrics` skill).
- Keep the first version small and stable. A fast, fixed second update reads better than an ambitious first one.

## How to judge a result

- **Steps**: every step is done, or its blocker and who acts next are written down. A step marked "unknown" for more than a day gets checked.
- **The check before submit**: no failures, and each "worth a look" read by a person.
- **Review rounds**: one round is the goal; two is normal for a first app; a third on the same point means the fix didn't answer Apple's words.
- **Time to live**: from "built" to "live", count the days and where they went. The Google Play closed test alone is 14.
- **Staged rollout**: raise the share only while the crash rate on the new version stays at or below the last one's.
- **The first weeks**: downloads per day from launch, the crash rate on the staged rollout, the first ratings, and, with ads, cost per paid download against the learning budget.

## Hard gates

Don't submit or release if any of these is true:

- An App Privacy or Data safety answer was guessed, or declares less than the app's SDKs send.
- An age rating answer was guessed.
- A subscription app is missing its Terms of Use link in any language, or its paywall doesn't show price, period and both links.
- The demo account doesn't work, or will expire during review.
- Screenshots don't show the real app.
- A point App Review raised has no answer.
- The paid apps agreement's tax and bank forms aren't done, and the app sells something.
- On Google Play, a personal account created after 13 November 2023 hasn't finished its closed test.
- EU trader status isn't declared, and the app should be available in the EU.
- The Data safety form has no account deletion link, and the app has accounts.
- The Google Play pre-launch report, when it ran, shows a crash you haven't fixed.
- The privacy policy or support URL doesn't open, or doesn't name the app.

## Common mistakes

- Privacy answers that leave out what an SDK sends.
- Age rating answers given without reading the questions.
- A subscription app with the Terms of Use link in English only.
- A demo account that expires before review.
- Screenshots from a design tool instead of the real app.
- Answering only the first point of a rejection.
- Starting the Google Play closed test the week the launch is due.
- Forgetting EU trader status, then finding the app unavailable in the EU.
- Leaving the tax and bank forms for launch week, so nothing can go on sale.
- An update that adds an SDK without updating App Privacy and Data safety.
- Raising a staged rollout to 100% before reading its crash rate.

## Worked example

Wrenleaf, a demo plant watering app, free for five plants with one yearly subscription. It stores everything on the phone and uses one analytics SDK and one crash reporting SDK.

**What the app does:** "Wrenleaf reminds you to water each houseplant on the day it needs it, and shifts the schedule with the season. It's for people with a few plants who forget. Plants and schedules stay on your phone; anonymous usage and crash data go to two SDKs. Free for five plants; a yearly subscription unlocks more."

**App Privacy** from it: no account and no personal data leave the phone. The analytics SDK sends usage data and a device ID (neither linked to the person, neither used for tracking), and the crash SDK sends crash data. Each row carries its reason ("analytics SDK, see its privacy documentation").

**The check before submit** finds one failure: the description in German has no Terms of Use link (English and French do). Fixed before submitting.

**Review round 1** comes back with one point, quoted: "Guideline 2.1: the app crashed when we tapped Add Plant without a photo." The fix is a new build; the reply says what changed. **Round 2** is approved. Release: manual, on launch Tuesday (day 20).

**Google Play:** the closed test started during the build (14 testers, 14 days); production access applied for on day 15; staged rollout at 20%, then 100% after three days with a normal crash rate.

**The calendar, planned backwards from a Tuesday launch:**

| Day | What happens |
|---|---|
| Day 1 | App Store Connect record created (name reserved); Play Console app created; closed test started with the first build |
| Days 2 to 5 | Listing, screenshots, App Privacy, age rating, EU trader status, tax and bank forms |
| Day 6 | Check before submit: one failure (the German Terms of Use link), fixed; submitted |
| Day 7 | Review round 1: one point (the crash); new build and reply the same day |
| Day 8 | Approved; release set to manual |
| Day 15 | Closed test complete; Google Play production access applied for |
| Day 17 | Google Play approved; staged rollout at 20% |
| Day 20 | Launch Tuesday: App Store released; Google Play raised to 100% |

**First weeks:** reviews answered daily; brand plus 25 exact terms in Apple Ads in the US, with a learning budget for about 10 paid downloads a day; a weekly report from week one.

**Judged after two weeks:** 20 days from built to live, 14 of them the closed test; two App Store review rounds (one point, fixed the same day) and one on Google Play; no crash above the normal rate in the staged rollout; 31 ratings averaging 4.6; ads at about 10 paid downloads a day, so the learning budget is doing its job and the first read of what pays comes at day 14, confirmed at day 30.

## Works best through Fload: connect with MCP or the CLI

Launches are coming to [Fload](https://fload.com): they open to organizations in stages, so they may not be open to you yet. Once they are, Fload carries a launch by this method: each step on App Store Connect and Google Play with who acts next, the first listing from what the app does (for an app built with Fload, the App Privacy answers and age rating too, each with its reason), keyword research before launch, the subscription Terms of Use check before you submit, and App Review's message point by point. Every change waits for your approval.

**Connect** (one of):

- Claude Code: `claude mcp add --transport http --scope user fload https://api.fload.com/mcp`
- Claude desktop or claude.ai: [add Fload to Claude](https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=Fload&connectorUrl=https%3A%2F%2Fapi.fload.com%2Fmcp) (opens Add custom connector with the URL filled in), or Settings → Connectors → Add custom connector, URL `https://api.fload.com/mcp`
- Any MCP client with an API key (from platform.fload.com → Settings → API keys): run `npx -y @fload-ai/mcp` with `FLOAD_API_KEY` set
- A terminal: `npm install -g @fload-ai/cli`, then `fload login`

After launch, every other Fload tool applies. Install the Fload skill too: `npx skills add fload-ai/mcp --skill fload`.
