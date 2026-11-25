---
name: build-an-app
description: Use when turning an app idea into an iPhone or Android app, checking whether an app idea has demand and room on the App Store or Google Play, writing an app plan or screen list, choosing an app's name, prices and look, building an app screen by screen with a coding agent, testing it with TestFlight or a Google Play test, or making a new app ready for App Review and the stores.
license: MIT
metadata:
  version: '2.0.0'
---

# Build an App

The job is to take an idea to a built app that people can find, that passes review, and that someone would pay for or come back to. An app that ships is small, does one job well, aims at a gap the apps people use today leave open, and is built store-ready from the first screen.

The numbers this job moves: whether people search for what the app does, how its rivals are rated, and, once it's live, its first downloads, its conversion and its first ratings. Building the wrong app well moves none of them, so the method starts with the idea, not the code.

## The loop

1. **Check the idea** against the store: demand, rivals, their complaints, a verdict, the gap.
2. **Write a one-page plan** aimed at the gap.
3. **Check the name** and make the icon your own.
4. **Choose how to build** it.
5. **Build screen by screen**, judging each screen in light and dark before the next.
6. **Build store-ready** as you go, not at the end.
7. **Test it on phones** with real testers.
8. **Hand it to a launch** (the `launch-an-app` skill).

If a step fails its check (how to judge, below), go back one step, not forward.

## 1. Check the idea before you plan it

Spend an hour on this first. It decides what the plan aims at.

1. **Write the searches people would type** to find an app like it: 3 to 8 short searches, two to four words each, in lower case, the words real people type, most likely first. No app or brand names. Mark the one to three broadest.
2. **Check demand for each search.** The Apple Ads console shows a popularity tier for a search term, from 1 (low) to 5 (high). Apple also gives a 1 to 100 score and an in-genre score, with weekly and monthly history, through its Ads insights and its platform API. Each is Apple's relative score for how often it is searched, not a search volume. Write it down per search. A search with no score has not been measured: write "not measured", never 0. With a score that has history, compare the last three months with the same three months a year before; as a rule of thumb, a change within about 15% is flat.
3. **Look at the apps people find now.** Search the broadest terms on the store and take the first five apps. For each, note its stars, its number of ratings and its exact price.
4. **Read their 1 to 3 star reviews.** Write one sentence per app on what its users complain about most. If its reviews say nothing clear, write nothing.
5. **Give one verdict:**
   - **Strong**: people search for this (as a rule of thumb, tiers of 3 or more on several searches), and the apps they find leave room (few ratings, low stars, or a common complaint).
   - **Crowded**: big apps (as a rule of thumb, many thousands of ratings and high stars) already own these searches.
   - **Thin demand**: the searches sit at tier 1.
   - **Unclear**: the searches aren't measured, or the facts are too thin to tell.
6. **Name the gap**: what this app could do that the apps found now don't, taken from what their users complain about.
7. **If the verdict is not strong, write a sharper angle**: the same idea, aimed at the gap, in one sentence. Then plan the angle, not the first idea.

Use only numbers you actually found. Don't estimate, round or add them up, and remember a popularity tier is not a count of searches or people.

Keep the searches: the best ones feed the app's name, subtitle and keywords later (see the `app-store-optimization` skill).

## 2. Write the plan (one page)

- **Name**: short and friendly. Both stores allow 30 characters for the title, and on the App Store emoji and flags can count as more than one character. Keep emoji out of the name.
- **Subtitle** (App Store): up to 30, counted the same way. Use one of your best searches in it.
- **Promise**: one sentence on what the app does for the person, at most about 160 characters. "It reminds me to water each plant on the day it needs it."
- **Audience**: who it is for, in one short phrase.
- **What it keeps**: one plain sentence. The simplest first app keeps everything on the phone, with no account and no sign-in. That also removes account deletion and sign-in rules from your review, and makes offline use easy.
- **The look**: an accent colour, a lighter version of it that reads well on a dark background, a display font and a style that suit the idea. Plan light and dark from the start.
- **Screens**: 3 to 6 for the first version, the main one first. For each: a title of one to three words, what the person sees there in one or two sentences, what they can tap or do there, and a short line shown when it's ready. Everything else waits for version 2.
- **Prices**: free, or one simple price to start. If you sell a subscription, at most one price per period (monthly, yearly, lifetime) and a clear free trial if you offer one. Use the rivals' prices as a guide, not a copy. Both stores take a commission on digital sales. Apple's Small Business Program charges 15% on up to $1M. Google Play, since 30 June 2026 in the EEA, the UK and the US, charges 10% plus a 5% billing fee on the first $1M (15% in total with Play Billing). Plan the price with it.

If you checked the idea, write the promise, audience, screens and prices from the research: aim at the gap and make the app different from what people find now. Note which finding shaped which part.

**Keep every promise honest**: only what a small app on one phone can do. No personal financial, medical or legal advice.

**The plan as a file** (put it in the repository; the coding agent builds from it):

```markdown
# <Name> (<n> of 30)
Subtitle: <subtitle> (<n> of 30)
Promise: <one sentence>
Audience: <one phrase>
Keeps: <what, and where: on the phone, or an account>
Look: accent #RRGGBB, dark accent #RRGGBB, display font, style

## Screens (in build order)
1. <Title>: <what you see>. Actions: <what you can do>. Ready line: "<line>"
2. ...

## Prices
- <period>: <price>, trial <days or none>

## The idea check
Verdict: <strong | crowded | thin demand | unclear>. Gap: <gap>. Angle: <angle or none>
Searches: <search> (tier <n>), ...

## Version 2 (not now)
- <everything that didn't make the first version>
```

The "Version 2" list matters: writing an idea down there is how you keep it out of version 1 without losing it.

**Pricing, in more detail**

- **Free first** when the app's value shows only after a few days of use (a habit, a reminder). Charge for more, not for starting.
- **A subscription** suits an app that keeps giving (new content, syncing, ongoing reminders). A **one-time price** suits a tool that does one thing forever.
- **A trial** should be long enough to reach the moment the promise comes true. A weekly habit needs a week; a daily one can show it in three days.
- **The paywall** names the price, the period, what the trial turns into and when, and links the Terms of Use and privacy policy. Nothing on it should surprise the person on their first bill.
- **Price per country** later, from real conversion. Start with the store's own price points.

## 3. Check the name and the icon

- **Search the name on both stores.** If a store can't be searched, the answer is "unknown", never "free".
- **A store search only sees live apps.** It misses names already reserved in App Store Connect and registered trademarks. Search a trademark register for the name in your main countries too.
- **Reserve the name early** by creating the app's record in App Store Connect as soon as the name is settled. Google Play doesn't hold a name for you: other apps can use the same one, so there the trademark check is what protects it.
- **Make the icon your own.** An icon that looks like another app's (the same shape and layout, recoloured) invites a rejection and confuses buyers. Compare it with the icons of the apps you found in step 1.

## 4. Choose how to build it

| Choice | Good when |
|---|---|
| Apple's native tools (SwiftUI) for iPhone, Google's (Jetpack Compose) for Android | one platform first, the best feel, deep system features |
| A cross-platform framework | both platforms from one codebase, a small team |

Pick one and stay with it for the first version. Building the iPhone app first from the plan, then Android from the same plan, works well.

Decide these early too, because they shape the code:

- **Payments**: Apple's in-app purchase on iPhone and Google Play Billing on Android. For subscriptions you need a way to check purchases and keep each person's status: either your own server checking receipts with each store, or a subscription service. Restore purchases must work.
- **Notifications**, if the promise depends on them (a reminder app does): ask permission at the moment it makes sense, not on first launch.
- **Offline use**: what happens with no connection. On-phone data makes this simple.
- **Languages**: write every word through a string file from screen one, so translating later is a copy job, not a rewrite.
- **Android**: build for the target API level Google currently requires, and know what every SDK collects for the Data safety form.

**What changes between iPhone and Android, from the same plan:**

| | iPhone | Android |
|---|---|---|
| Payments | Apple's in-app purchase | Google Play Billing |
| Privacy form | App Privacy in App Store Connect | Data safety in Play Console |
| Testing | TestFlight | internal, closed and open tests |
| Back navigation | in the screen (a back button, a swipe) | the system back gesture must work on every screen |
| Sign-in | with another company's sign-in, also an equivalent login option (guideline 4.8) | no equivalent rule |
| Reminders | ask permission when it's needed | Android 13 and later also asks permission for notifications |

## 5. Build screen by screen

- Put the one-page plan in the repository as a file, and have the coding agent build **one screen at a time**, in the plan's order.
- After each screen: run it, take a screenshot in **light and in dark**, check it against the plan, fix, then move on. A screen isn't done until both screenshots look right.
- Keep shared pieces (colours, type, buttons) in one place from screen one, so later screens stay consistent.
- Commit after every working screen. If a build run stops, the finished screens stay; carry on from the next one.
- Test on a real phone before calling a screen done: speed, keyboard, notch and safe areas.

## 6. Build store-ready from the start

These are cheaper to build in than to add after a rejection:

- **Real content, no placeholders.** Every button works; empty, loading and error states exist.
- **In-app purchase** through the store for digital content and features, with a **Restore purchases** button and clear prices and trial terms on the paywall.
- **Terms of Use and privacy policy** linked from the paywall if the app sells auto-renewing subscriptions, and the price, the period and what the trial turns into shown before the person pays.
- **Permissions** asked only when needed, with a line that says why.
- **Privacy**: know what every SDK in the app sends off the phone. You'll declare all of it at launch.
- **Account deletion** inside the app, if the app has accounts at all.
- **An equivalent login option** (guideline 4.8) on iPhone, if the app offers another company's sign-in: one that limits the data to name and email, lets people hide their email, and doesn't track them for ads without consent. Sign in with Apple meets it but isn't required. There are exceptions: an app with only its own sign-in, education or enterprise accounts, sign-in with a government ID, and an app for a third-party service's clients.
- **Accessibility**: text that scales, labels for screen readers, enough contrast, in light and dark.
- **Analytics and crash reporting** from the first build: a short list of events tied to the promise (opened, did the core action, paid).
- **Originality.** An app built from a template must be clearly its own app: its own name, icon, look and purpose. Near-duplicates are rejected as spam.

## 7. Test it on phones

- **iPhone, TestFlight.** Up to 100 people on your own App Store Connect team can test a build with no review. For testers outside your team, invited by email or a public link, the first build gets a full Beta App Review, which can take a day or more; later builds of the same version might not need one.
- **Android, Google Play testing.** An internal test reaches up to 100 testers you name, within minutes. **Closed test:** personal developer accounts created after 13 November 2023 need 12 testers opted in for 14 days in a row before production. Start it here, as soon as you have a build, so the two weeks run while you finish.
- Use it yourself for a few days and fix every crash. Then hand it to a launch (see the `launch-an-app` skill), on your own Apple and Google developer accounts.

## How to judge a result

**The idea** passes when the verdict is strong, or when the sharper angle aims at a gap at least two rivals' users complain about.

**The plan** passes when:

- the promise fits in one sentence and every screen serves it;
- the name and subtitle fit and the name is free (or you know it's unknown and why);
- the price is decided, and the screens assume it (a paywall screen exists if anything is sold);
- someone who isn't you can read it and say what the app does.

**A screen** passes when, on a real phone:

- it shows what the plan says it shows, and nothing the plan doesn't;
- every action the plan lists works, and nothing on it is dead;
- its empty, loading and error states exist and read well;
- both screenshots (light and dark) look right, with readable contrast;
- text at the largest size still fits, and a screen reader names every control;
- it uses the shared colours, type and buttons, not one-off copies.

**The build** passes when a test round with real people produced no crash you haven't fixed, every purchase and Restore works on the store's test accounts, and the store-ready list in step 6 is all true.

## Hard gates

Don't move on if any of these is true:

- The verdict is crowded or thin and you're still planning the first idea, not an angle.
- The name is taken on either store, or clashes with a registered trademark.
- A screen has placeholder text, a dead button or a missing state.
- Digital content is sold any way other than the store's in-app purchase.
- Restore purchases is missing.
- The app has accounts but no way to delete one in the app.
- You don't know what each SDK sends off the phone.
- The app gives personal financial, medical or legal advice, or promises what it can't do.
- The app looks like a copy of another app or of its template.

## Common mistakes

- Planning before checking whether anyone searches for it.
- Copying the market leader instead of aiming at its users' complaints.
- Reading a popularity tier as a number of searches.
- Twelve screens in version 1.
- Adding payments last, after the screens assume something else.
- A name that's taken on one store, found after the icon and listing are done.
- Hard-coded words that make translation a rewrite.
- Starting the Google Play closed test the week the launch is due.
- Judging screens only in light mode.

## Worked example

**The idea:** "an app that reminds me to water my plants".

**Searches:** "plant watering reminder", "water plants app", "plant care", "watering schedule", "plant tracker". Broadest: "plant care", "water plants app".

**Demand (Apple Ads popularity tiers):** plant care 4, water plants app 3, plant watering reminder 3, watering schedule 2, plant tracker 2.

**Rivals for "plant care"** (first five): two with tens of thousands of ratings at 4.7 and 4.8 stars, priced as a yearly subscription; three with a few hundred ratings around 4.2 to 4.4.

**Complaints:** the big two "push a subscription before you can add a plant" and "reminders ignore the season"; the small three "too many ads".

**Verdict: crowded.** Big apps own "plant care".
**Gap:** reminders that follow the season, with no paywall before the first plant.
**Angle:** "a watering reminder that shifts each plant's schedule with the season, free for your first five plants."

**The plan:**

- Name: Wrenleaf: Watering Reminder (27). Subtitle: Plant care by the season (24).
- Promise: It reminds me to water each plant on the day it needs it, all year.
- Audience: people with a few houseplants who forget to water them.
- What it keeps: your plants and their schedules, on your phone only. No account.
- Screens, in build order:
  1. **Today**: the plants to water today, each with its photo and how much water. Actions: tap a plant to mark it watered; snooze one to tomorrow. Ready line: "Here's today's watering."
  2. **My plants**: every plant, with the next day it needs water. Actions: add a plant (name, photo, how often), open one. Ready line: "Your plants, all in one place."
  3. **Plant**: one plant's schedule and the last ten waterings. Actions: change how often, delete the plant. Ready line: "Everything about this plant."
  4. **Seasons**: how each schedule shifts from summer to winter. Actions: turn the shift on or off per plant. Ready line: "Schedules that follow the year."
  5. **Settings**: reminder time, the yearly price, Restore purchases, Terms of Use and privacy policy. Actions: change the reminder time, restore purchases, open either link. Ready line: "Set it up your way."
- Price: free for five plants; one yearly price to unlock more, with a 7-day free trial. The paywall shows the price, the period, what the trial turns into, and both links.
- Version 2: sharing a plant with someone else, a plant identification camera, widgets.

**Name check** (in this example): no live app with the name on either store and nothing in the trademark search, so the App Store Connect record was created the same day to hold it.

**Build:** Today first, then My plants, Plant, Seasons, Settings, each shot in light and dark. The empty state of Today ("Nothing to water today") was missing on the first pass and added before moving on.

**Test:** TestFlight with 6 people from the team, then a public link after Beta App Review; a Google Play closed test with 14 testers started the same week. One crash (opening Seasons before any plant was added), fixed in build 4. Then on to the launch.

## Works best through Fload: connect with MCP or the CLI

The app builder is coming to [Fload](https://fload.com): it opens to organizations in stages, so it may not be open to you yet. Once it is, Fload builds the app with you by this method: it checks your idea against the US App Store (verdict, gap and a sharper angle), drafts the plan, checks the name, and builds the app screen by screen in light and dark. A built app then moves into a launch on your own Apple account; launches open in stages too.

**Connect** (one of):

- Claude Code: `claude mcp add --transport http --scope user fload https://api.fload.com/mcp`
- Claude desktop or claude.ai: [add Fload to Claude](https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=Fload&connectorUrl=https%3A%2F%2Fapi.fload.com%2Fmcp) (opens Add custom connector with the URL filled in), or Settings → Connectors → Add custom connector, URL `https://api.fload.com/mcp`
- Any MCP client with an API key (from platform.fload.com → Settings → API keys): run `npx -y @fload-ai/mcp` with `FLOAD_API_KEY` set
- A terminal: `npm install -g @fload-ai/cli`, then `fload login`

Install the Fload skill too: `npx skills add fload-ai/mcp --skill fload`.
