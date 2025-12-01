# COMPAS Dataset Data Dictionary

## Overview
The COMPAS (Correctional Offender Management Profiling for Alternative Sanctions) dataset contains information used to assess the risk of recidivism (re-offending) for defendants in Broward County, Florida.

## Core Variables

### Demographic Information
- `id`: Unique identifier for each defendant
- `name`: Defendant's name (anonymized)
- `age`: Defendant's age at time of screening
- `age_cat`: Age category ('Less than 25', '25 - 45', 'Greater than 45')
- `race`: Self-reported race
- `sex`: Biological sex
- `dob`: Date of birth

### Case Information
- `c_case_number`: County case number
- `c_charge_degree`: Charge degree (Felony 'F' or Misdemeanor 'M')
- `c_charge_desc`: Description of the charge

### Time Information
- `c_jail_in`: Date defendant entered jail
- `c_jail_out`: Date defendant exited jail
- `days_b_screening_arrest`: Days between arrest and COMPAS screening

### COMPAS Scores
- `decile_score`: COMPAS risk score (1-10, higher = higher risk)
- `score_text`: Risk category ('Low', 'Medium', 'High')
- `priors_count`: Number of prior arrests
- `v_decile_score`: Violent recidivism risk score

### Outcome Variables
- `two_year_recid`: Recidivism within two years (1 = yes, 0 = no)
- `is_recid`: Recidivism flag (-1 = not applicable, 0 = no, 1 = yes)
- `is_violent_recid`: Violent recidivism flag

### Risk Assessment Factors
- `priors_count`: Number of prior charges
- `juv_fel_count`: Juvenile felony charges
- `juv_misd_count`: Juvenile misdemeanor charges
- `juv_other_count`: Other juvenile charges

## Preprocessing Notes
Variables used in our analysis:
- `risk_binary`: Derived from `score_text` (1 = High/Medium, 0 = Low)
- `recidivism_binary`: Derived from `two_year_recid`
- `privileged_group`: Binary indicator (1 = Caucasian, 0 = African-American)

## Source
ProPublica COMPAS Analysis: https://github.com/propublica/compas-analysis