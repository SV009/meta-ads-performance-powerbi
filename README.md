# meta-ads-performance-powerbi
A data-driven overview of paid ad performance on Facebook and instagram. Track reach, engagement, conversions, and budget to understand what's working and where to optimize

# Meta Ads Performance Analytics Dashboard (Power BI)

A Power BI dashboard analyzing paid social performance across Facebook and Instagram. It brings together campaign, ad, and event-level data to surface high-ROI segments, compare formats, and guide budget/creative optimization.

**Live Demo:** [Power BI (read-only)](https://app.powerbi.com/view?r=eyJrIjoiYjRlZDZjMWEtOWU3ZS00ZDkxLWE5M2MtMmUwNDQyMTI5MTc3IiwidCI6IjM0MDJlZWMzLWYyZDgtNDFmMy1iNjk4LWJlNzRkMDEwMGQ3NyIsImMiOjJ9&pageName=9480e9604ea2c8501466)

## Project Highlights
- Introduction + Insights pages for executive storytelling.
- Slicers for platform, audience, ad type/format, geography, and time.
- Core performance metrics with clear definitions and consistent DAX.
- Campaign calendar vs. observed event window handled via in-period logic (budget proration, overlap checks).

## Data Timeframe
- **Observed events:** May 7, 2025 – Aug 6, 2025 (UTC).
- **Campaign calendar:** Jan 4, 2025 – Dec 10, 2025 (UTC).
- Metrics in visuals reflect the **observed event window**; budgets are **prorated** to the overlap days where noted.

## Data Model (tables)
- `campaigns` — id, name, start_date, end_date, duration_days, total_budget  
- `ads` — id, campaign_id, platform, ad_type, target_gender, target_age_group, target_interests  
- `ad_events` — event_id, ad_id, user_id, timestamp (UTC), day_of_week, time_of_day, event_type  
- `users` — id, age, gender, country (aggregated for audience slices; no PII)

> **Privacy note:** This repo includes only anonymized samples for demonstration.

## Key Metrics
- **Click-through rate (CTR)** = Clicks ÷ Impressions  
- **Engagement rate** = (Clicks + Shares + Comments) ÷ Impressions  
- **Conversion rate** = Purchases ÷ Clicks  
- **Purchase rate** = Purchases ÷ Impressions  
- **Cost per acquisition (CPA)** = Ad Spend ÷ Conversions  
- **Return on ad spend (ROAS)** = Revenue ÷ Ad Spend

## Executive Summary — Meta Ads Performance

### Headlines:
ads are very good at attracting attention and interaction, but fewer people finish the purchase than expected. Total activity in the sample shows 216K impressions, 25.4K clicks, 29K engagements, and 1.3K purchases with CTR 11.76% and Engagement Rate 13.56%—strong signs that creative and targeting are resonating—while Purchase Rate is 0.61% and Conversion Rate is 5.21%, indicating room to improve the post-click experience.

### Where we’re strong:

- Creative and targeting are working: high CTR and engagement show people notice and interact with the ads. 
- By format, Video performs best on click-through, conversion, and engagement, with Stories also strong; Image/Carousel are solid but slightly weaker on purchases. Focus investment on Video and Stories. 

### What’s holding results back:

- Despite strong attention and interactions, only 0.61% of views become purchases (1.3K out of 216K). This points to issues after the click—page load speed, message/offer strength, or checkout friction.

### Who to prioritize:

- Engagement is higher among females (43%) and concentrates in the 20–30 age band; performance drops after 35+. Tailor creative and offers to this core group.
- Markets: India & US drive scale; Germany/UK likely deliver higher value per purchase. Plan “scale” vs “premium” messaging and bids accordingly.

### When to show up:

- Activity is steady across weeks, with late-afternoon to evening (~15–20h) peaks. Calendar spikes around the 19–21 and 25–27 dates suggest promotions or launches move the needle. Weight delivery to these hours and replicate event-driven bursts.

### 30-day action plan:

- Shift more budget to Video and Stories; trim lower-yield formats. 
- Improve what happens after the click: faster pages, clearer value, simpler checkout; add retargeting for interested visitors who didn’t buy. 
- Prioritize females 18–30 with tailored creative and offers. 
- Schedule and bid more aggressively in afternoons/evenings and around promo/event days where engagement historically spikes.

## Tech
Power BI · DAX · CSV (sample data) · Git LFS for large assets


