# Final project guide — Swan



Develop P1 (app use and spending) and P2 (coupon assignment and visits, spending, renewal, and business viability). The monthly-revenue extension is optional. Submit one notebook based on template.ipynb with relative paths to dados/. The instructor sets the deadline. Restart Kernel and Run All before submission. The guide organizes questions without prescribing a model or answer.



## 1. Understanding the data



### Guidance



Understand what each row and column represents before fitting a model.



### Hint



What is the observation unit and period? Which variables describe registration, choices, assignment, or outcomes?



### Caution



Choice, randomization, and recording determine what data can answer.



## 2. Data quality



### Guidance



Investigate missing values, zeros, extremes, and consistency.



### Hint



Do customers reporting income resemble those not reporting it? What does zero recorded visits mean? Which extreme observations are plausible under the dictionary?



### Caution



Do not delete or impute without investigation and a record of consequences.



## 3. Questions and outcomes



### Guidance



Define each outcome, its type, and the scale relevant to the decision.



### Hint



Is it continuous, a count, or binary? Is it skewed? Are zeros meaningful? Should results be in dollars, percentages, or percentage points?



### Caution



Zeros cannot enter logarithms without an explicit decision and recognition of its consequences.



## 4. P1: specification and estimation



### Guidance



Choose a reference specification and justify inference.



### Hint



How do users differ from nonusers? Which characteristics also relate to spending? What functional forms and standard errors are defensible?



### Caution



Controlling a consequence of the variable of interest changes the question.



## 5. P1: diagnostics and robustness



### Guidance



Examine residuals and influential cases; compare defensible alternatives.



### Hint



What changes with functional form, sample, missingness treatment, or extreme observations? Identify the sample and interpretation of every alternative.



### Caution



Robustness is not searching for the preferred p-value.



## 6. P2: randomization



### Guidance



Examine pre-pilot comparability and explain what assignment identifies.



### Hint



Can randomized groups differ by chance? Do balance p-values certify or invalidate the protocol? What interference or recording problems would matter?



### Caution



The design concerns coupon assignment, not automatically app use or coupon redemption.



## 7. P2: visits, spending, and renewal



### Guidance



Estimate each outcome using an appropriate specification and inference.



### Hint



Which scale serves each question? What does dispersion imply? Do controls change the sample, estimate, or precision?



### Caution



Nonlinear-model coefficients are not directly probabilities or outcome units.



## 8. P2: heterogeneity and business decision



### Guidance



Investigate group differences and translate evidence into a recommendation.



### Hint



Does incremental contribution cover cost under the stated accounting convention? What uncertainty remains? Is future renewal value observed or assumed? Which operating information is missing?



### Caution



Statistical significance does not establish economic value; overlapping intervals do not test equality.



## 9. Optional revenue extension



### Guidance



Characterize trend, persistence, and growth.



### Hint



Which deterministic terms match the question? Record the test protocol and distinguish exact growth from log changes.



### Caution



Nonrejection does not prove a unit root; rejection does not guarantee future stability or recovery.



## 10. Conclusions, recommendations, and limitations



### Guidance



Answer management in decision language.



### Hint



Separate evidence, assumptions, proposed action, missing information, and reassessment conditions. State limitations from design, synthetic data, coverage, and period.



### Caution



An association does not establish causality; a recommendation without evidence is not an analytical conclusion.



## Business convention



The 20% margin and USD 120 annual incremental cost per assignment are brief assumptions. Cost has not already been deducted from the calculation margin. Separate current net contribution from future-renewal scenarios and avoid counting discounts twice. Record inventory, capacity, and service gaps; do not estimate hiring without hours, productivity, and wages.



## Submission check



Confirm unit and variable origins; documented quality choices; justified outcome scales and specifications; appropriate inference; interpreted diagnostics and alternatives; economic and causal limits; clear recommendations; and successful clean execution.

