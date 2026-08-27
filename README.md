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
_(to be filled in as analysis progresses)_

## How to Reproduce
1. Clone this repo
2. `python3 -m venv venv && source venv/bin/activate`
3. `pip install -r requirements.txt`
4. Download the dataset and place in `data/`
5. Run notebooks in `notebooks/`