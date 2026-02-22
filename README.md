Airbnb Price Transparency A/B Test

New Orleans Market Analysis

📌 Project Overview

This project evaluates whether increased price transparency improves booking conversion rates in the New Orleans Airbnb market.

Using real listing data from Kaggle, I simulated 50,000 randomized user sessions and conducted an A/B test to measure the impact of a transparency treatment on checkout completion and overall booking conversion.

The analysis was performed in R using statistical hypothesis testing and logistic regression.

🧪 Experimental Design

    Users were randomly assigned to either:

    • Variant A — Control
    • Variant B — Price Transparency Treatment

Checkout initiation probability was simulated based on listing characteristics including price, rating, superhost status, and instant booking availability.

The treatment group was simulated to have a +2 percentage point increase in booking completion probability.

Experiment integrity was validated through:

  • Sample ratio mismatch testing

  • Covariate balance checks

📊 Key Results

Primary Metric: Checkout Completion Rate

    • Control: 68.0%
    • Treatment: 70.8%
    • Lift: +2.0 percentage points
    • p-value: 0.0012

The difference is statistically significant at the 5% level.

Secondary Metric: Overall Booking Conversion

    • Control: 13.7%
    • Treatment: 14.5%
    • p-value: 0.0075

This result is also statistically significant.

📉 Logistic Regression (Controlled Analysis)

A logistic regression model was estimated to evaluate the treatment effect while controlling for listing characteristics.

    • Controls: price, rating, superhost status, instant booking
    • Treatment effect remains statistically significant (p = 0.002)
    
Because the effect remains significant after accounting for listing characteristics, the improvement in booking completion is unlikely to be driven by differences in price or host quality. This suggests the transparency treatment contributed to the observed lift.

💼 Business Recommendation

    Based on statistically significant improvements in checkout completion and overall booking conversion, 
    the price transparency treatment should be rolled out in the New Orleans market.

Further testing across additional markets is recommended before a broader deployment.

📊 Dataset

Source: Kaggle – New Orleans Airbnb Listings

Dataset not included due to licensing restrictions

To reproduce:

    • Download the dataset from Kaggle
    • Place the CSV file inside the data/ folder
    • Run scripts/ab_testing_analysis.R

🛠 Tools & Methods

    • R
    • A/B testing
    • Hypothesis testing (two-sample proportion tests)
    • Chi-squared test
    • Logistic regression (binomial)
    • Simulation modeling
    • Data manipulation (dplyr)
    • Data visualization (ggplot2)

👤 Author
    
    Isaiah Lacet
