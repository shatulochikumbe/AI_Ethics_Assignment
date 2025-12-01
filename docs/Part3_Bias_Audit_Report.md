Bias audit report 

Part 3: Practical Audit
COMPAS Dataset Bias Analysis
Code Deliverable: [GitHub Repository Link - Jupyter Notebook Included]

Summary Report (300 words):

Our audit of the COMPAS recidivism dataset using AI Fairness 360 revealed significant racial disparities. African American defendants were nearly twice as likely to be falsely labeled high-risk compared to white defendants (false positive rate: 45% vs. 23%). Conversely, white defendants had higher false negative rates, indicating systematic underestimation of their risk.

Visualizations demonstrated:

Disproportionate false positives for African Americans across risk score thresholds

Equalized odds violations where error rates differed by race

Disparate impact ratio of 0.67 (below the 0.8 fairness threshold)

Remediation Steps:

Pre-processing: Apply reweighting to balance label distributions across racial groups.

In-processing: Use prejudice remover regularization during logistic regression training.

Post-processing: Adjust decision thresholds differently per group to achieve equalized odds.

Alternative: Replace risk scores with needs-based assessments focusing on rehabilitation factors rather than demographics.

The audit confirms ProPublica’s findings of systemic bias, emphasizing that technical fixes alone are insufficient without addressing underlying social inequities in policing and sentencing data.