# Predicting Injury Severity Following a Car Crash

**Tools Used:** R, Logistic Regression, Data Visualization

## Executive Summary
This repository analyzes traffic accident data from Montgomery County, Maryland, to determine which environmental, behavioral, and vehicular variables most significantly impact the severity of driver injuries following a collision. By developing a binary logistic regression model, this project provides data-driven insights into the primary risk factors associated with severe traffic injuries.

## Methodology & Data

*   **Dataset:** Data was sourced from the Automated Crash Reporting System (ACRS) via local Maryland police departments[cite: 1].
*   **Target Variable:** The analysis focused exclusively on cases where injuries occurred, restructuring the response variable into a binary outcome: *Suspected Serious/Fatal Injury* (1,755 cases) and *Suspected Minor Injury* (13,622 cases).
*   **Modeling:** A full binary logistic regression model was selected over a reduced model following a drop-in-deviance test and AIC/BIC evaluation.
*   **Thresholding:** A decision-making threshold of 0.1 was applied based on the ROC curve to minimize the false-negative rate, prioritizing the accurate classification of potentially fatal crashes.
*   **Predictors:** The final model integrated weather type, surface condition, driver distraction, collision type, driver substance abuse, vehicle body type, vehicle damage extent, and speed limit.

## Key Findings

*   **Model Performance:** The final logistic regression model achieved an Area Under the Curve (AUC) of 0.758, indicating fair predictive ability. 
*   **Vehicle Characteristics:** Vehicle body type and the extent of vehicle damage emerged as the strongest indicators of injury seriousness. Passenger cars and trucks are associated with significantly lower odds of severe injury compared to motorcycles.
*   **Substance Abuse:** Drivers with no detected substance abuse have significantly lower odds of being involved in a serious/fatal injury crash compared to drivers suspected of alcohol use.
*   **Limitations:** While the model correctly identified suspected minor injuries with approximately 94% accuracy, it only correctly predicted serious/fatal injuries ~23% of the time, indicating a need for future multinomial modeling.

---
*For the complete exploratory data analysis, visualizations, and statistical outputs, please view the [Full Project Report](written-report.pdf).*
