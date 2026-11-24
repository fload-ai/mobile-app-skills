---
name: launch-an-app
description: Use when publishing a new app or a major update to the App Store or Google Play, preparing App Store Connect or Play Console for a first release, filling in App Privacy or Data safety, getting through App Review, or answering a rejection.
license: MIT
metadata:
  version: '1.0.0'
---

# Launch an App

A first release fails on paperwork far more often than on code. Work through the store's list in order, keep every answer true to what the app actually does, and plan for one round of review feedback.

## App Store (iOS)

**Before the build**

1. **Apple Developer Program** membership. An organization account needs a D-U-N-S number and takes longer to approve; start early.
2. **Bundle ID** registered, and signing set up (a distribution certificate and provisioning profile, or automatic signing).
3. **App Store Connect record**: the app's name (must be unique on the store), primary language, bundle ID and an SKU.

**The listing and the forms**

4. **Name, subtitle, keywords, description, promotional text** (see the `app-store-optimization` skill).
5. **Screenshots** for the required device sizes (the largest iPhone size, and iPad if the app runs on iPad). Show the real app.
6. **Privacy policy URL** (required for every app) and a support URL.
7. **App Privacy** answers: every kind of data the app or its SDKs collect, whether it is linked to the person, and whether it is used for tracking. Include what third-party SDKs collect; check their documentation.
8. **Age rating** questionnaire, **category**, **pricing and availability**, **content rights**, **export compliance** (encryption).
9. **App Review information**: a contact, and a working demo account if the app needs a sign-in. Notes that explain anything the reviewer cannot see on their own (hardware, a region, a paid feature).

**Submit**

10. Upload the build (Xcode or a CI tool), test it in TestFlight, attach it to the version, submit for review.
11. **Release choice**: automatically when approved, manually, or on a date. For updates, a phased release rolls out over 7 days and can be paused.

**Why apps are rejected most often**

| Guideline | What triggers it |
|---|---|
| 2.1 App completeness | crashes, broken links, placeholder content, a demo account that doesn't work |
| 2.3 Accurate metadata | screenshots or text that don't match the app |
| 3.1.1 In-app purchase | selling digital content or features without Apple's in-app purchase |
| 4.2 Minimum functionality | a thin wrapper of a website, too little to do |
| 4.3 Spam | an app that duplicates another one, or a template with little changed |
| 5.1.1 Data collection | asking for data the app doesn't need; no way to delete an account the app lets you create |

**When rejected:** read Apple's message in full, fix each point it names, and reply in App Store Connect saying what changed. If you believe the reviewer is mistaken, explain calmly with specifics; an appeal to the App Review Board is the last step.

## Google Play (Android)

1. **Play Console developer account**, with identity verification.
2. **New personal accounts must run a closed test first**: at least 12 testers opted in for 14 days in a row before production access can be requested. Plan those two weeks.
3. **App bundle (AAB)** signed with Play App Signing, built against the target API level Google currently requires.
4. **App content** forms: privacy policy, app access (sign-in instructions for review), ads declaration, content rating questionnaire, target audience, **Data safety** (what is collected and shared, including by SDKs).
5. **Store listing**: name (30), short description (80), full description, icon, feature graphic, phone screenshots.
6. **Release** through a track: internal, closed, open, then production with a **staged rollout** (a percentage of users first, raised as crash rates stay normal).

Review of a new app can take several days. A policy rejection names the policy; fix it and resubmit.

## Launch week

- Watch crash reports and reviews daily; reply to early reviews (see the `app-review-replies` skill).
- Keep the first version small and stable. A fast, fixed second update reads better than an ambitious first one.
- Measure from day one (see the `mobile-app-metrics` skill).

## Common mistakes

- Privacy answers that leave out what an SDK collects.
- A demo account that expires before review.
- Screenshots from a design tool instead of the real app.
- Starting the Google Play closed test the week the launch is due.

## Works best through Fload: connect with MCP or the CLI

[Fload](https://fload.com) can carry a launch for you: it tracks each step on App Store Connect and Google Play, proposes the App Privacy answers and the first listing from what the app does, researches keywords before launch, reads App Review's feedback point by point, and stages every change for your approval. Launches are coming to Fload: they open to organizations in stages.

**Connect** (one of):

- Claude Code: `claude mcp add --transport http --scope user fload https://api.fload.com/mcp`
- Claude desktop or claude.ai: [add Fload to Claude](https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=Fload&connectorUrl=https%3A%2F%2Fapi.fload.com%2Fmcp) (opens Add custom connector with the URL filled in), or Settings → Connectors → Add custom connector, URL `https://api.fload.com/mcp`
- Any MCP client with an API key (from platform.fload.com → Settings → API keys): run `npx -y @fload-ai/mcp` with `FLOAD_API_KEY` set
- A terminal: `npm install -g @fload-ai/cli`, then `fload login`

**What Fload adds to this skill**, once launches are open to you:

- Start a launch on the App Store (on your own App Store Connect team) or Google Play, and see each step and who acts next.
- Say what the app does once: the first listing, the App Privacy proposal and the keyword research start from it.
- Approve what waits on you, in Fload or from your own login.
- When App Review sends a launch back: Apple's words, each point and where its fix stands.

After launch, every other Fload tool applies. Install the Fload skill too: `npx skills add fload-ai/mcp --skill fload`.
