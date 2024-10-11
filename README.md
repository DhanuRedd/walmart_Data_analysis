# Walmart Business case study : Confidence Interval and CLT

## About Netflix

Walmart is an American multinational retail corporation that operates a chain of supercenters, discount departmental stores, and grocery stores from the United States. Walmart has more than 100 million customers worldwide.

🎯 Objective

The Management team at Walmart Inc. wants to analyze the customer purchase behavior (specifically, purchase amount) against the customer’s gender and the various other factors to help the business make better decisions. They want to understand if the spending habits differ between male and female customers: Do women spend more on Black Friday than men? (Assume 50 million customers are male and 50 million are female).

## Dataset

| Feature                  | Description                                 |
|:-------------------------|:--------------------------------------------|
| User_ID                  | User ID                                     |
| Product_ID               | Product ID                                  |
| Gender                   | Sex of User                                 |
| Age                      | Age in bins                                 |
| Occupation               | Occupation (Masked)                         |
| City_Category            | Category of the City (A, B, C)              |
| StayInCurrentCityYears   | Number of years stay in current city        |
| Marital_Status           | Marital Status                              |
| ProductCategory          | Product Category (Masked)                   |
| Purchase                 | Purchase Amount                             |

# steps performed

1. **Detection of Null Values & Outliers**:
   - Null values in the dataset were detected using the `isnull()` method.
   - Outliers were identified using a boxplot visualization.
   - The `describe()` method was employed to examine the spread of data, with particular attention to the difference between the mean and median to identify outliers.

2. **Data Exploration**:
   - The total amount spent per transaction by all 50 million female and male customers was tracked.
   - The average spending for both female and male customers was calculated, and the results were compared.

3. **Confidence Interval Calculation**:
   - The sample average for female and male customers was used to calculate a confidence interval within which the average spending of 50 million customers may lie.
   - The **Central Limit Theorem** was applied to observe how varying the sample size affected the distribution of average expenses for both male and female customers.
   - Confidence intervals with different widths (e.g., 90%, 95%, and 99%) were calculated and analyzed.

4. **Conclusion on Confidence Intervals**:
   - The overlap or non-overlap of confidence intervals for male and female spending was examined.
   - Based on this, recommendations were made for Walmart on potential changes or improvements.

5. **Married vs Unmarried Customer Analysis**:
   - The same analysis was conducted for married and unmarried customers, comparing their average spending and confidence intervals.

6. **Age Group Analysis**:
   - Customers were divided into life stage categories
   - An analysis of average expenses and confidence intervals was performed for each age group.

# Business Recommendations/Insights

1. Target product categories (1, 5, 8) across all age groups to boost demand and business performance.
2. Focus on the 26-35 age group and non-married individuals under 45 for targeted products to maintain demand and increase turnover.
3. Prioritize males in categories (1, 5, 8) to boost sales, then expand efforts to females. Avoid low-performing product categories below 9000 in sales.
4. City Category B, particularly for both males and females in categories (1, 5, 8), offers high business potential.
5. Occupations (0, 1, 4, 7, 14, 20) across genders contribute significantly to purchases, suggesting they are key targets.
6. No overlap in male and female purchase behaviors, indicating distinct spending patterns.
7. Overlap in male and female purchases at smaller sample sizes diminishes with larger samples, confirming significant behavior differences.
8. Married and non-married purchase behaviors show no significant difference based on overlapping confidence intervals.
9. Across sample sizes (300, 3000, 30000), no significant difference in married vs. non-married purchase behaviors was observed.
10. Overlap in purchases between age groups (18-25 and 45-50, 25-35 and 45-50/55) shows no significant behavioral differences.
11. Certain overlaps in purchase behavior between age bins (35-45 and 55) suggest less differentiation among these groups.
