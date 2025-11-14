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


## Tech
Power BI · DAX · CSV (sample data) · Git LFS for large assets


