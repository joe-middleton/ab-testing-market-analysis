# Marketing A/B Test Analysis

## Overview
Analysis of a marketing A/B test (588k users) comparing an ad campaign against a public service announcement (PSA), to determine whether the ads drove a statistically significant increase in conversions.

## Data
Source: [Kaggle - Marketing A/B Testing](https://www.kaggle.com/datasets/faviovaz/marketing-ab-testing)
Not included in this repo due to size — download from the link above and place in `data/`.

## Approach
- Exploratory data analysis
- Two-proportion hypothesis test on conversion rates
- Confidence interval on the lift
- Check for confounding variables (ad frequency, day/hour patterns)
- Power analysis given group imbalance

## Findings
- Users shown ads converted at 2.55% vs 1.79% for the PSA group — a 0.77 percentage point (43% relative) lift.
- This difference is highly statistically significant (two-proportion z-test, p < 0.001), with a 95% CI of (0.60, 0.94) percentage points for the absolute lift.
- The effect holds after controlling for total ad exposure and day of week using logistic regression (OR ≈ 1.47, p < 0.001), indicating the lift is attributable to ad content itself rather than confounding factors.
- Day of week significantly affects conversion independent of treatment — Monday and Tuesday show notably higher conversion than other days, a secondary insight worth further investigation.
- **Business takeaway:** the ad campaign meaningfully outperforms the PSA and the effect is robust — recommend continuing/scaling the ad campaign, with potential to further optimize by day-of-week targeting.

## How to Reproduce
1. Clone this repo
2. `python3 -m venv venv && source venv/bin/activate`
3. `pip install -r requirements.txt`
4. Download the dataset and place in `data/`
5. Run notebooks in `notebooks/`