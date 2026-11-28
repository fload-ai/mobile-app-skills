# Apple Ads thresholds

Every number the method in [../SKILL.md](../SKILL.md) uses, in one place. The bid and keyword rows are for Manage Bids campaigns; Maximize Conversions sets its own bids. They are starting points for a careful account: a team with its own measured reasons can tune them, and should write down why.

## What a download is worth

| Number | Rule |
|---|---|
| Day 35 | Value per download is first read at day 35, from proceeds (after the store's fee), not gross revenue. |
| Days 90 and 365 | Value is then projected at day 90 and day 365. |
| 90 days | To plan a country, use its downloads of the last 90 days. |
| 100 downloads and 1 payer | The least a country needs for a clear read of its own value. With less, borrow comparable countries' value. |
| Coverage 1.0 | Value per download ÷ cost per paid download: a download from a tap, first-time or redownload. At 1.0 or more the spend pays back. |
| Coverage 0.7 | From 0.7 up to 1.0 is close to paying; under 0.7 it does not pay. |
| Day 14, then day 30 | Read whether a campaign pays at day 14 and confirm it at day 30; never judge on 7 days. |

## Countries and budgets

| Number | Rule |
|---|---|
| 300 paid downloads over 30 days | A country's learning budget: about 10 paid downloads a day at its own cost. |
| about 100 downloads | Leave out a country with no ads history and fewer downloads than this in the window. |
| Six campaigns, an even split | Every country starts with all six, with its budget split evenly. |
| 20% a week | Weekly budget move from the lowest-coverage campaign to the highest. |
| 30 paid downloads | Each campaign needs this before the weekly move. |
| Brand's launch share | Brand never drops below it. |
| 30.4 days | A month's budget ÷ 30.4 is the daily pace; never more than what is left ÷ the days left. |
| +30%, paying 1.0× | The first growth step is a test of +30% of today's spend, and growth continues only if that step paid back at least 1.0×. |

## Keywords and search terms

| Number | Rule |
|---|---|
| About 25 exact terms | The launch set, plus your brand terms. |
| 20 taps | Below this, nothing is judged: no pause, no block, no bid move. |
| 5 installs over 7 days | Promote a discovery search term to exact once it has this many tap installs over at least 7 days of its own delivery, at or under break-even. Negate it in both discovery campaigns the same day. |
| 0 installs, 20 taps, 3 × break-even | Block a search term that has all three. Without a break-even, use 3 × the campaign's cost per tap install. |

## Bids

| Number | Rule |
|---|---|
| 10 to 20% above Apple's suggested bid | A new campaign's starting bid, but never above what a tap is worth to you (your break-even cost per install × your tap-to-install rate) and never above your daily budget. Apple refuses a bid above the daily budget. |
| 48 hours | Hold the starting bid this long. |
| 15% a day | Step the bid down this much every 24 hours while delivery holds. |
| 60% | A day delivers when its spend ÷ budget is at least 60% of the day before's. Under that: hold 24 hours, then raise back one step if it is still low. |
| 80% | After a raise, a day at 80% or more of the last good day makes that bid the baseline. |
| $0.10 | The lowest bid. Never go under a minimum Apple refused either. |
| 40% for 48 hours | If every reported day of the last 48 hours spent under 40% of budget, do not step down further. |
| × 0.8 ÷ 0.55 | A new exact keyword's starting bid = break-even cost per tap × 0.8 ÷ the tap-to-bid ratio (0.55 until you can measure your own). |
| 30 taps, 3 keywords | Measure your own tap-to-bid ratio as the median over exact keywords with at least 30 taps, from at least 3 of them. |
| 30 installs or 14 days | Wait this long since a bid's last change before you judge it. |
| 30% impression share (90% for brand) | Raise a paying bid only under this share. |
| 20% in 24 hours | The most any bid moves in any 24 hours, counting every change, a person's included. |
| One move a day | At most one bid move per campaign every 24 hours, on data at most about a day old. |

## Reading results

| Number | Rule |
|---|---|
| 95% | A change counts as a clear win or loss only beyond the central 95% of the account's normal week-to-week swings. |
| 100 quiet-week pairs | The least history for the account's own noise band. With fewer, borrow from comparable keywords and widen the band. |
| 5 installs a week | Under this, a cost or installs change cannot be read. |
| 30 days | Revenue in a read less than 30 days past its window is provisional. |
| 1 to 5 (console); 1 to 100 and in-genre (Ads insights, platform API) | Apple's search popularity per term: relative demand, not a search count. The finer scores come with weekly and monthly history. |
| Tap-through CPA | Judge keywords on Avg CPA (Tap-Through); Avg CPA (Total) also counts view-through installs. |
