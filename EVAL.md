# Evaluation test set

Fill this in after every refresh, before you publish. The agent is the system under test.
You are the grader. Nothing here is automated on purpose: the point is to decide, with a
source you trust, whether the agent told you the truth.

**Ground truth sources.** Pick one and use the same one every time, so your scores are
comparable week to week:

- Prices: Google Finance (google.com/finance), Yahoo Finance, or your brokerage app.
- News: the article itself. Open the link. Check the date on the page.
- Calendar: the company's investor relations page (search "TICKER investor relations
  events"), or the Fed's own meeting calendar for FOMC dates.

Refresh date: 2026-10-28    Grader: number-checker agent

Checked 2026-10-28 around 11:33 AM EDT. Google Finance (https://www.google.com/finance/quote/TICKER:EXCHANGE)
returned "Google Finance isn't supported on this device" for all five tickers, so prices come from Yahoo
Finance history pages instead, as noted in each row.

## A. Prices (one row per ticker)

Pass if the dashboard's last price is within $0.10 of the ground truth for the same day
and the same price type (close vs intraday). If the agent recorded an intraday price,
compare against the intraday price at about the same time; do not compare it to a close.

| Ticker | Date shown | Price type shown | Dashboard price | Ground truth price | Source you used | Pass / Fail |
|---|---|---|---|---|---|---|
| AAPL | 2026-10-21 | close | 343.99 | 343.99 | Yahoo Finance history (Google Finance unsupported): https://finance.yahoo.com/quote/AAPL/history/ | Pass |
| AAPL | 2026-10-22 | close | 348.22 | 348.22 | Yahoo Finance history: https://finance.yahoo.com/quote/AAPL/history/ | Pass |
| AAPL | 2026-10-23 | close | 347.73 | 347.73 | Yahoo Finance history: https://finance.yahoo.com/quote/AAPL/history/ | Pass |
| AAPL | 2026-10-26 | close | 343.91 | 343.91 | Yahoo Finance history: https://finance.yahoo.com/quote/AAPL/history/ | Pass |
| AAPL | 2026-10-27 | close | 347.10 | 347.10 | Yahoo Finance history: https://finance.yahoo.com/quote/AAPL/history/ | Pass |
| COST | 2026-10-21 | close | 998.31 | 998.31 | Yahoo Finance history (Google Finance unsupported): https://finance.yahoo.com/quote/COST/history/ | Pass |
| COST | 2026-10-22 | close | 1018.21 | 1018.21 | Yahoo Finance history: https://finance.yahoo.com/quote/COST/history/ | Pass |
| COST | 2026-10-23 | close | 1003.32 | 1003.32 | Yahoo Finance history: https://finance.yahoo.com/quote/COST/history/ | Pass |
| COST | 2026-10-26 | close | 1005.16 | 1005.16 | Yahoo Finance history: https://finance.yahoo.com/quote/COST/history/ | Pass |
| COST | 2026-10-27 | close | 992.13 | 992.13 | Yahoo Finance history: https://finance.yahoo.com/quote/COST/history/ | Pass |
| GS | 2026-10-21 | close | 904.72 | 904.72 | Yahoo Finance history (Google Finance unsupported): https://finance.yahoo.com/quote/GS/history/ | Pass |
| GS | 2026-10-22 | close | 891.30 | 891.30 | Yahoo Finance history: https://finance.yahoo.com/quote/GS/history/ | Pass |
| GS | 2026-10-23 | close | 875.68 | 875.68 | Yahoo Finance history: https://finance.yahoo.com/quote/GS/history/ | Pass |
| GS | 2026-10-26 | close | 893.28 | 893.28 | Yahoo Finance history: https://finance.yahoo.com/quote/GS/history/ | Pass |
| GS | 2026-10-27 | close | 911.77 | 911.77 | Yahoo Finance history: https://finance.yahoo.com/quote/GS/history/ | Pass |
| CAT | 2026-10-21 | close | 740.21 | 740.21 (unadjusted close; adj close 738.45 after Oct 26 ex-dividend) | Yahoo Finance history (Google Finance unsupported): https://finance.yahoo.com/quote/CAT/history/ | Pass |
| CAT | 2026-10-22 | close | 704.05 | 704.05 | Yahoo Finance history: https://finance.yahoo.com/quote/CAT/history/ | Pass |
| CAT | 2026-10-23 | close | 687.00 | 687.00 | Yahoo Finance history: https://finance.yahoo.com/quote/CAT/history/ | Pass |
| CAT | 2026-10-26 | close | 692.13 | 692.13 | Yahoo Finance history: https://finance.yahoo.com/quote/CAT/history/ | Pass |
| CAT | 2026-10-27 | close | 713.31 | 713.31 | Yahoo Finance history: https://finance.yahoo.com/quote/CAT/history/ | Pass |
| PFE | 2026-10-21 | close | 29.85 | 29.85 | Yahoo Finance history (Google Finance unsupported): https://finance.yahoo.com/quote/PFE/history/ | Pass |
| PFE | 2026-10-22 | close | 30.42 | 30.42 | Yahoo Finance history: https://finance.yahoo.com/quote/PFE/history/ | Pass |
| PFE | 2026-10-23 | close | 30.03 | 30.03 | Yahoo Finance history: https://finance.yahoo.com/quote/PFE/history/ | Pass |
| PFE | 2026-10-26 | close | 29.79 | 29.79 | Yahoo Finance history: https://finance.yahoo.com/quote/PFE/history/ | Pass |
| PFE | 2026-10-27 | close | 29.80 | 29.80 | Yahoo Finance history: https://finance.yahoo.com/quote/PFE/history/ | Pass |

Intraday latest prices (not scored). The brief records Oct 28 prices at about 11:24 AM ET. The nearest
quote I could open was Yahoo's at about 11:33 AM EDT, nine minutes later, so the like-for-like check
cannot be made. These rows are informational only.

| Ticker | Date shown | Price type shown | Dashboard price | Nearest quote seen (time) | Source you used | Pass / Fail |
|---|---|---|---|---|---|---|
| AAPL | 2026-10-28 11:24 AM | intraday | 345.40 | 345.40 (11:33:23 AM EDT) | https://finance.yahoo.com/quote/AAPL/history/ | Unverifiable (no 11:24 quote available) |
| COST | 2026-10-28 11:23 AM | intraday | 984.00 | 983.89 (11:32:55 AM EDT) | https://finance.yahoo.com/quote/COST/history/ | Unverifiable (no 11:23 quote available) |
| GS | 2026-10-28 11:24 AM | intraday | 921.68 | 920.31 (11:33:00 AM EDT); day range 913.15 to 922.92 | https://finance.yahoo.com/quote/GS/history/ | Unverifiable (no 11:24 quote available; 921.68 is inside the day range) |
| CAT | 2026-10-28 11:24 AM | intraday | 713.49 | 712.90 (11:33:26 AM EDT); day range 707.63 to 732.26 | https://finance.yahoo.com/quote/CAT/history/ | Unverifiable (no 11:24 quote available) |
| PFE | 2026-10-28 11:24 AM | intraday | 29.59 | 29.57 (11:33:32 AM EDT) | https://finance.yahoo.com/quote/PFE/history/ | Unverifiable (no 11:24 quote available) |

## B. Weekly change (one row per ticker)

The page computes this from the five closes. Pass if it is within 0.3 percentage points of
your own calculation: (last price minus the close five trading days earlier) divided by
that earlier close.

How the page computes it: `weekChange()` in index.html uses (latest intraday price minus the Oct 21
close) / Oct 21 close, not just the five closes. So "Your calculation" uses the same basis: Yahoo's Oct 21
close and Yahoo's nearest intraday quote (about 11:33 AM EDT). The closes-only figure (Oct 21 to Oct 27,
Yahoo) is also shown for reference, and it matches BRIEF's closes-only figure exactly because all 25 closes
match. Caveat: the intraday leg is not verified at 11:24 (see section A).

| Ticker | Dashboard weekly change | Your calculation | Pass / Fail |
|---|---|---|---|
| AAPL | +0.4% (343.99 to 345.40) | +0.41% (343.99 to 345.40 at 11:33); closes-only +0.90%. Source: https://finance.yahoo.com/quote/AAPL/history/ | Pass |
| COST | -1.4% (998.31 to 984.00) | -1.44% (998.31 to 983.89 at 11:33); closes-only -0.62%. Source: https://finance.yahoo.com/quote/COST/history/ | Pass |
| GS | +1.9% (904.72 to 921.68) | +1.72% (904.72 to 920.31 at 11:33); closes-only +0.78%. Source: https://finance.yahoo.com/quote/GS/history/ | Pass (0.18 pp gap) |
| CAT | -3.6% (740.21 to 713.49) | -3.69% (740.21 to 712.90 at 11:33); closes-only -3.63%. Source: https://finance.yahoo.com/quote/CAT/history/ | Pass |
| PFE | -0.9% (29.85 to 29.59) | -0.94% (29.85 to 29.57 at 11:33); closes-only -0.17%. Source: https://finance.yahoo.com/quote/PFE/history/ | Pass |

## C. News grounding (one row per news item, three per ticker)

Open every link. Pass only if all four are true: the link opens, the headline matches the
article, the article date is within the last seven days, and the "why it matters" line is
supported by the article (not just plausible).

Window: 2026-10-21 to 2026-10-28 inclusive.

| Ticker | Headline (first few words) | Link opens | Headline matches | Dated within 7 days | "Why" is supported | Source | Pass / Fail |
|---|---|---|---|---|---|---|---|
| AAPL | Apple unveils new iMac with M6... | Yes | Yes | Yes (Oct 27) | No. The release says nothing about Apple's quarter, the holiday quarter, or the Nov 2 results; "ship days after the quarter closes" is not in the article. | https://www.apple.com/newsroom/2026/10/apple-unveils-new-imac-with-m6/ | Fail |
| AAPL | Apple Announces New 14-Inch MacBook Pro With M6 Chip | Yes | Yes | Yes (Oct 27) | Partly. $1,999 start and "low-end 14-inch model" are supported; investors and holiday demand are not mentioned. | https://www.macrumors.com/2026/10/27/14-inch-macbook-pro-with-m6-chip/ | Fail |
| COST | Costco Remains a Defensive Compounder... | Yes | Yes | Yes (Oct 27) | Yes. Hold rating, 48x trailing P/E, "little margin for error". | https://finance.yahoo.com/markets/stocks/articles/costco-remains-defensive-compounder-awaiting-124541831.html | Pass |
| GS | Goldman Sachs CEO David Solomon on AI's economic impact... | Yes | Yes | Yes (Oct 23) | No. The article does not call it a reputational move or say anything about earnings impact, and the $500M funds the next phase of the 10,000 Small Businesses program, not the Institute itself. | https://fortune.com/2026/10/23/david-solomon-frontier-models-not-needed-small-business/ | Fail |
| GS | The Goldman Sachs Group (NYSE:GS) CEO David Solomon Sells 12,000 Shares... | Yes | Yes | Yes (Oct 27) | Yes. 12,000 shares at $910.72 avg; the article does not say whether it was under a 10b5-1 plan. | https://www.marketbeat.com/instant-alerts/insider-the-goldman-sachs-group-nyse-gs-ceo-david-solomon-sells-12000-shares-of-stock-2026-10-27/ | Pass |
| CAT | UBS cuts Caterpillar stock price target... | Yes | Yes | Yes (Oct 26) | Yes. $825 to $750, Neutral kept, "bar for driving sustained upside... appears elevated". | https://www.investing.com/news/analyst-ratings/ubs-cuts-caterpillar-stock-price-target-on-valuation-concerns-93CH-4971903 | Pass |
| CAT | Caterpillar (NYSE:CAT) Stock Price Up 3.2%... | Yes | Yes | Yes (Oct 27) | Yes. $1.63 dividend and about $1B North Carolina expansion are in the article (it gives no earnings date; Oct 29 is confirmed in section D). | https://www.marketbeat.com/instant-alerts/price-caterpillar-nyse-cat-stock-price-up-32-heres-why-2026-10-27/ | Pass |
| PFE | Pfizer's TALZENNA Plus XTANDI FDA-Approved for an Earlier... | Yes | Yes | Yes (Oct 26) | Yes. Approval moves the combination to an "earlier line" (metastatic hormone-sensitive, HRR-mutated). | https://www.financialcontent.com/article/bizwire-2026-10-26-pfizers-talzenna-plus-xtandi-fda-approved-for-an-earlier-metastatic-prostate-cancer-treatment-setting | Pass |
| PFE | Pfizer shares may move 3.8% on Nov. 3 earnings release | Yes | Yes | Yes (Oct 27) | Yes. 3.8% implied move from Bloomberg options data. | https://www.investing.com/news/stock-market-news/pfizer-shares-may-move-38-on-nov-3-earnings-release-93CH-4976046 | Pass |
| AAPL (recheck 2026-10-28) | Apple unveils new iMac with M6... | Yes | Yes | Yes (Oct 27) | Yes. New why: "Pre-orders for the new iMac open October 28, with availability on November 6." Article: "Customers can pre-order starting tomorrow, October 28, with availability beginning Friday, November 6." | https://www.apple.com/newsroom/2026/10/apple-unveils-new-imac-with-m6/ | Pass |
| AAPL (recheck 2026-10-28) | Apple Announces New 14-Inch MacBook Pro With M6 Chip | Yes | Yes | Yes (Oct 27, 6:01 am PDT) | Yes. New why: "refreshed the low-end 14-inch MacBook Pro with the M6 chip, starting at $1,999." Article body: "a refreshed 14-inch MacBook Pro featuring the M6 chip", "It starts at $1,999." "Low-end" is not in the article body; it appears on the same page in MacRumors' "Upcoming" sidebar ("Spec bump to the M6 chip for the low-end 14-inch model") and is consistent with the $1,999 entry price. Accepted, with that caveat. | https://www.macrumors.com/2026/10/27/14-inch-macbook-pro-with-m6-chip/ | Pass |
| GS (recheck 2026-10-28) | Goldman Sachs CEO David Solomon on AI's economic impact... | Yes | Yes | Yes (Oct 23) | Partly. The $500M funding the next phase of 10,000 Small Businesses is now correct. But "Solomon said Goldman rarely needs frontier AI models" is not supported: the article quotes "there's very little that we do where we need frontier models" and says he appeared to be "speaking generally about economic activity in the context of small business", not about Goldman's own use. A supported version: "Solomon said most everyday business activity, especially for small businesses, does not need frontier AI models." | https://fortune.com/2026/10/23/david-solomon-frontier-models-not-needed-small-business/ | Fail |
| GS (recheck 2 2026-10-28) | Goldman Sachs CEO David Solomon on AI's economic impact... | Yes | Yes (exact match) | Yes (Oct 23) | Yes. New why: "Solomon said most everyday business activity, especially for small businesses, does not need frontier AI models; Goldman is putting $500 million into the next phase of its 10,000 Small Businesses program." Article: "there's very little that we do where we need frontier models", with Solomon "seeming to speak generally of economic activity, in the context of small business"; he separates frontier models from "the everyday tools businesses actually use"; Goldman announced "a new $500 million commitment to fund the next chapter" of the program. The article has no single sentence saying small businesses do not need frontier models; the why is a fair paraphrase of the quote in the article's stated context. | https://fortune.com/2026/10/23/david-solomon-frontier-models-not-needed-small-business/ | Pass |

(Add rows as needed. Fifteen items is normal for five tickers.)

## D. Calendar (one row per event)

Pass if the event and its date appear on the source linked, and the date is in the future
relative to the refresh date.

Note: the Apple, Caterpillar, Pfizer, and Costco IR pages loaded empty (JS-rendered), returned 404/403,
or timed out. Where an IR page showed nothing, a verbatim copy of the company's own press release, opened
at a URL other than the one the brief cites, was accepted as the company source.

| Ticker | Event | Date shown | Confirmed on source | Source | Pass / Fail |
|---|---|---|---|---|---|
| AAPL | Fiscal Q4 2026 earnings, call 5:00 PM ET | 2026-11-02 | No. The Apple IR page loaded but lists no event. MacDailyNews (Oct 7) and MacTrast (Oct 6) both report Nov 2, call 2:00 PM PT / 5:00 PM ET, as announced by Apple; no Apple-hosted page was seen. | https://investor.apple.com/investor-relations/default.aspx ; https://macdailynews.com/2026/10/07/apple-to-report-q426-earnings-on-monday-november-2nd/ | Fail (not shown on Apple IR page; date likely correct per secondary sources) |
| AAPL | M6 iMac available in stores | 2026-11-06 | Yes. "Pre-order starting at 10:10 a.m. PT on October 28th. Available starting November 6th" | https://www.apple.com/imac/ | Pass |
| COST | Dividend record date, $1.47 (payable Nov 13) | 2026-10-30 | Yes. Costco release dated Oct 14: $1.47, record Oct 30, payable Nov 13. | https://finviz.com/news/402668/costco-wholesale-corporation-announces-quarterly-cash-dividend (also SEC 8-K https://www.sec.gov/Archives/edgar/data/0000909832/000090983226000096/costex9918-k101426.htm) | Pass |
| COST | October sales results (labelled expected) | 2026-11-04 | No. The Costco IR home page lists no upcoming events and the events page returned 404. Only the third-party Catacal page shows Nov 4, 9:00 AM EST (marked "Verified" there). The brief correctly labels it as expected. | https://investor.costco.com/ ; https://www.catacal.com/catalyst/costco-october-sales-report | Fail (not on Costco IR page) |
| GS | FOMC rate decision (Oct 27 to 28 meeting) | 2026-10-28 | Yes. October 27-28 is on the 2026 calendar; same day as the refresh, which meets "on or after". | https://www.federalreserve.gov/monetarypolicy/fomccalendars.htm | Pass |
| CAT | Q3 2026 results 5:30 AM CDT, call 7:30 AM CDT | 2026-10-29 | Yes. Caterpillar release (Oct 15): results 5:30 a.m. CDT, call 7:30 a.m. CDT, Oct 29. Corroborated by 247 Wall St ("before the market opens on October 29"). caterpillar.com timed out twice; IR events page empty. | https://finviz.com/news/402910/caterpillar-inc-to-announce-third-quarter-2026-financial-results-on-october-29 ; https://247wallst.com/investing/2026/10/25/can-caterpillars-72b-backlog-save-its-stock-from-a-10-slump/ | Pass |
| PFE | Q3 2026 earnings, before market open | 2026-11-03 | Yes. Pfizer release (Sep 22): Q3 2026 Performance Report issued the morning of Nov 3, analyst call 10:00 a.m. EST. Pfizer IR returned 404/403. | https://finviz.com/news/394367/pfizer-invites-public-to-view-and-listen-to-webcast-of-november-3-conference-call-with-analysts | Pass |
| PFE | Dividend record date, $0.43 (payable Dec 7) | 2026-11-06 | Yes. Pfizer release (Oct 6): $0.43, record Nov 6, payable Dec 7. | https://www.financialcontent.com/article/bizwire-2026-10-6-pfizer-declares-fourth-quarter-2026-dividend | Pass |

## E. Omissions

Did the agent miss something a human analyst would have included? List anything you found
in the ground-truth sources that the brief does not mention (a big headline, an earnings
date inside the window). Each one counts as a Fail in the score below.

- 
- 

## F. Your own test cases

Write two tests of your own that none of the sections above cover. Examples students have
used: "the as-of date on the page matches the changelog date", "no ticker shows a flat
sparkline when the real stock moved", "the page still renders if I delete one ticker's
news list in the data". Write the test, run it, record the result.

| Test | How you checked | Pass / Fail |
|---|---|---|
| | | |
| | | |

## Score

| Section | Passes | Total | Rate |
|---|---|---|---|
| A. Prices | 25 | 25 | 100% (closes only; 5 intraday prices unverifiable, not scored) |
| B. Weekly change | 5 | 5 | 100% (intraday basis; intraday leg unverified at 11:24) |
| C. News | 9 | 9 | 100% after fixes (recheck 2 2026-10-28: GS Fortune now Pass; recheck 1: both AAPL items Pass, GS Fortune still Fail, 8/9, 89%; first run was 6/9, 67%) |
| D. Calendar | 6 | 8 | 75% |
| E. Omissions (fails only) | 0 | | |
| F. Your own | | | |
| **Overall** | | | |

Publish only if A and B are 100% and C is at least 80% after fixes. If a row failed, tell
Claude exactly which row and what the correct value is, let it fix only that, rerun the
`qa-reviewer` agent, and regrade that row. Keep the original Fail in this file: a record of
what the agent got wrong is more useful than a clean sheet.
