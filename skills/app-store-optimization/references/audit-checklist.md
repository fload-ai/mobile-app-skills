# ASO audit checklist

Work through every row for each localization and storefront you touch. The **Store** column says where a check applies:

- **Both:** App Store and Google Play.
- **App Store** or **Google Play:** that store only.

A row that fails becomes a recommendation, with its decision (proceed, test, hold, needs data, review, reject) and its evidence. The method behind each row is in [../SKILL.md](../SKILL.md).

## Metadata and keywords

| Check | Store | What to do |
|---|---|---|
| Character space not fully used | Both | Fill every indexed field in every localization, and check again after any removal. |
| Subtitle (App Store) or short description (Google Play) wasted on a generic tagline or on title words | Both | Write a keyword-bearing line per locale from local keyword research, never a translation. |
| Duplicates across fields | App Store | Remove repeats across the name, subtitle and keyword field. Keep one only when a custom product page keyword assignment needs it. |
| Spaces after commas in the keyword field | App Store | Separate with commas only, and spend the freed characters on validated words. |
| Singular and plural both in the keyword field | App Store | Keep the singular where the store's matching of plurals in that language is checked. |
| Filler words using scarce characters | Both | Remove them where store behavior and existing ranks allow. |
| Numbers spelled out | Both | Use digits where they read naturally. |
| Whole phrases repeated instead of split into words | App Store | Break target phrases into their words and spread them across the three indexed fields of one locale. |
| The most valuable generic keyword buried late in the name or subtitle | Both | Test placing it earlier where brand and conversion allow. |
| Google Play full description not keyword-optimized | Google Play | Rewrite naturally around the core keywords, repeated with care and never stuffed. |
| Main keywords not repeated across title, short description and full description | Google Play | Repeat them in all three. In the full description about 2 to 5 mentions is a reference, never a target. |
| The same keyword in overlapping localizations of one storefront | App Store | Remove only true redundancy, and keep the main coverage in the primary listing. |
| Keywords translated one to one | Both | Research each market in its own language. |
| Chinese, Japanese or Korean listings translated literally | Both | Rewrite natively, with a native speaker's review. |
| No second locale used for extra keywords | App Store | Map which storefronts read which localizations, then use a second locale's space for words that do not fit the primary one. |
| A competitor's name in the app name, subtitle, promotional text or description | Both | Move it out. In the App Store keyword field it is allowed, with a note that Apple can reject an app for using another company's trademark (guideline 5.2.5). |
| Apple's own trademarks (such as "iMessage") or celebrities' or other protected names in any metadata field | Both | Warn the app owner that it can get the app rejected (guideline 5.2.5 on the App Store), unless the app owns or licenses it. Keeping it is the owner's call. |
| Google Play tags missing or weak | Google Play | Choose only accurate, relevant tags. |
| Primary or secondary category a poor fit | Both | Check truthful fit, browse relevance and chart eligibility. The secondary category exists on the App Store only. |

## Localization

| Check | Store | What to do |
|---|---|---|
| Metadata localized but the app is not | Both | At minimum localize onboarding. Weigh how much the app depends on language (see the skill, Step 5). |
| In-app purchase names left in English | Both | Localize the names people see, and keep them truthful. |
| Promotional text not localized | App Store | Localize timely messages for each relevant market. |
| Formal and informal address mixed | Both | Pick one form per market and use it across metadata and screenshots. |
| Markets with no localized listing | Both | Weigh the expected download and revenue gain against other tasks. |
| Screenshots not localized | Both | Localize them in the main markets. |
| No rank tracking per locale after localizing | Both | Track before and after, per market. |

## Conversion

| Check | Store | What to do |
|---|---|---|
| Icon not tested in a long time | Both | Run an icon test with a clear hypothesis when traffic allows. |
| Screenshots do not say the value clearly | Both | Rework the order, the message, readability and intent match as testable concepts. |
| The first 3 screenshots do not say the main value fast | Both | Rebuild them as hook, value and result, with short captions. |
| No regular native listing tests | Both | Run product page optimization (App Store) and store listing experiments (Google Play), each with a hypothesis. |
| Video relies on sound or has a weak first frame | Both | Make the first frame and first seconds work without sound. |
| No look at competitors' creative | Both | Review their themes, formats and messages to find test ideas. |
| No custom pages, or only in English | Both | Build and localize custom product pages (App Store) or custom store listings (Google Play) for each intent group with real traffic. |
| All campaigns land on the same default page | Both | Map the main paid, social and email themes to their own custom pages when traffic justifies it. |
| Keyword assignment to custom product pages not used | App Store | Assign keywords from the latest approved version to the most relevant custom product page for high-value searches (up to 70 pages per app). |

## Events, featuring and ratings

| Check | Store | What to do |
|---|---|---|
| Local seasonal moments ignored | Both | Keep an event calendar per market (Ramadan, Golden Week, Singles' Day and the like). |
| No regular featuring nominations | Both | Nominate real, high-quality updates, events and seasonal moments. |
| No in-app events or promotional content | Both | Keep a real event and content calendar: in-app events (App Store) and promotional content (Google Play). |
| No local review strategy | Both | Localize review prompts and support flows, and answer negative reviews quickly in the user's language. |
| A low rating not treated as a conversion problem | Both | Find the causes, then fix the product, support and prompts before scaling acquisition. |
| Review prompts at bad moments, or not the store's own | Both | Use the stores' native review prompts at moments of real satisfaction, within their limits. |
| Negative reviews unanswered, recurring issues not passed on | Both | Answer them, and pass recurring problems to the product and support teams. |
| High crash or "app not responding" rates | Google Play | Check the console's technical health against Google's bad-behavior thresholds, and fix it first when they are breached. |

## Measurement

| Check | Store | What to do |
|---|---|---|
| Changes launch with no baseline, success metric or rollback trigger | Both | Define all of them before launch (Step 8 of the skill). |
| Benchmarks copied from stores, markets or categories that are not alike | Both | Use like-for-like benchmarks, or lower your confidence. |

## Hand over to paid acquisition or product

These rows are for the ads or product owner. ASO can supply the evidence for them.

| Check | Store | What to do |
|---|---|---|
| A high-value market with no paid test | Both | Check the market's value and unit economics, then test paid acquisition where it pays. |
| Brand-defense ad spend never tested for its real gain | Both | Measure how many brand downloads the ads add rather than take from organic. Set spend from the cost of each extra download, not a fixed percentage. |
| Winning ad creative not localized | Both | Adapt proven concepts for the main locales and test them at small scale. |
| Apple Ads search terms not fed back into ASO | App Store | Use converting search terms as evidence for metadata, keyword and custom page ideas. |
| Relevant keywords ranked around 5 to 15 with no paid support test | App Store | For valuable, winnable words, test whether ads support lifts the organic rank enough to pay for itself. |
| Country prices not localized or tested | Both | Test prices where buying power or competitors' prices differ a lot. |

## Never recommend

- Incentivized installs to push a keyword, fake or paid reviews, review attacks or bot engagement.
- Bursts of bought installs to fake ranking speed.

You may detect and report a competitor doing these.
