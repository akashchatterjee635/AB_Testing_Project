<h1>A/B Testing for Conversion Optimization</h1>
This project applies statistical analysis to evaluate whether a new landing page improves user conversion on an e-commerce platform. It simulates a common business scenario where a product or growth team wants to validate design changes with data before rolling out to all users.

<h3>Dataset</h3>
The dataset (ab_data.csv) contains:
user_id: Unique visitor identifier
timestamp: Visit time
group: A/B test assignment (control or treatment)
landing_page: Page seen by the user (old_page or new_page)
converted: Binary flag (1 if user converted, 0 otherwise)

<h3>Objectives</h3>
Validate integrity of A/B assignment (control vs treatment).
Filter out mismatches (e.g., control group seeing new page).
Calculate overall conversion rates for both groups.

<h3>Perform hypothesis testing:</h3>
Two-proportion z-test
Logistic regression with statsmodels
Analyze statistical significance at 95% confidence level (p < 0.05).

<h3>Methods Used</h3>
Data cleaning and integrity checks
Conversion rate calculations
Two-proportion z-test using scipy
Logistic regression via statsmodels.Logit
Power analysis and p-value interpretation
Optional: Visualizations using matplotlib and seaborn

<h3>Tools & Libraries</h3>
pandas
numpy
matplotlib, seaborn
scipy.stats
statsmodels

<h3>Key Results</h3>
The difference in conversion rates between the control and treatment groups was analyzed and found to be statistically insignificant at the 95% confidence level.
Logistic regression further confirmed that the new page did not significantly impact conversion probability.
Business recommendation: Do not roll out the new landing page without further redesign or additional experimentation.

<h3>File Structure</h3>
bash
Copy
Edit
AB_Testing.ipynb     # Main analysis notebook
ab_data.csv          # Source dataset
README.md            # Project documentation

<h3>Future Work</h3>
Segment analysis (device, region, traffic source)
Time-based effects (day-of-week, recency)
A/B/C multi-variant testing
Use uplift modeling or Bayesian testing for more nuanced evaluation
