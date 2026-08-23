# Day 8 – Personal Environmental Health Analyzer

**Challenge:** Build an interactive dashboard analyzing AQI, PM2.5/PM10, and water quality across Indian cities, then upgrade it from demo data to real, cited data.

## What I Built

A single self-contained `index.html` — a dark-theme, premium SaaS-style dashboard covering 19 Indian cities, with:
- Working filters (city, AQI range, pollutant, health-risk level, date range, city-comparison mode)
- 5 interactive Chart.js visualizations (AQI, PM2.5, PM10, category distribution, environmental ranking)
- An animated SVG AQI gauge, city detail cards, and a personal environmental "report card" with computed scores and grades
- Auto-generated insights (cleanest/most polluted cities, anomalies) and personalized recommendations — all computed live from the dataset, not hardcoded
- Real AQI data (CPCB National AQI Bulletin + aqi.in) and real water-quality data (BIS 2019 national tap-water study), fully cited inside the dashboard itself

## Key Learnings

**1. "Real data" means methodology, not just new numbers.**
The hard part of swapping demo values for real ones wasn't finding numbers — it was being honest about *where each number actually came from*. Some AQI values are official CPCB readings; PM2.5/PM10 for most cities are *derived* from AQI using CPCB's own published breakpoint formula, because the public bulletin doesn't list raw concentrations. Some water-quality scores are direct BIS test results; five cities without direct data use a clearly labeled state-capital proxy. Disclosing the difference between "measured" and "estimated" turned out to matter more than the precision of any single figure.

**2. One unguarded dependency can silently break a whole page.**
The dashboard loaded its charting library from an external CDN with no fallback check. When that CDN didn't load, the very first chart call threw an error — and because nothing downstream had error handling, *every section after it* (insights, city detail, recommendations, even sections that had nothing to do with charts) quietly stayed blank. Nothing crashed visibly; it just... didn't finish. That's a scarier failure mode than a visible crash, because it looks like missing data instead of broken code.

**3. "Self-contained" has to be taken literally.**
The brief asked for a single self-contained HTML file, but depending on an external CDN for a core feature quietly broke that promise. The real fix wasn't wrapping the failure in a try/catch — it was removing the external dependency entirely by embedding the charting library's source directly in the file. Sometimes the right fix isn't handling a failure gracefully; it's making the failure impossible.

**4. Test the fix — don't just assert it.**
Rather than declaring "this should work now," the fix was verified by actually reproducing the failure (stripping network access in a headless browser test) and confirming every section still populated. Then, after embedding the library, the same test was re-run with *zero* network access to confirm the charts rendered from nothing but the file itself. A good habit to carry forward: reproduce the bug before claiming it's fixed.

## Stack & Sources
`HTML / CSS / vanilla JS` · `Chart.js 4.4.4 (embedded, no external calls)` · Data: CPCB National AQI Bulletin, aqi.in, BIS 2019 Tap Water Quality Study

---
#60DayClaudeChallenge · Day 8/60
