# anaan_ml

## Organization   
Within the cleaning and combining datasets folder:    
- ANAANcombined_cec_2023-07-03.csv is a merged dataset using individual data I received from Yuchen in cardbox (R15 Sensor Preprocessing and Analysis > RAW ALL datasets deidentified). This csv combines the following datasets: DH3, PT open series, online IE, in vivo, PR, RPS, and CS
- AAN missingness measures.Rmd is where I clean baseline data (e.g., only keeping AN/AAN diagnoses, checking missingness, scoring measures, checking plausible values). the hmtl file is a knitted version of this markdown.

## Measures   
- **BDI**:    
  - non clinical (20 item): dh3, online ie, in vivo. rescored items 15 and 17.   
  - clinical (21 item): pt, r15, RPS, CS. item 7 was removed, so it will be NA for rows in these datasets. rescored items 16 and 18   
  - total score was calculated by summing all items except the suicidality item   
- **EDE-Q**:    
  - 4.0: dh3, online ie, in vivo    
  - 6.0: pt, r15, RPS, CS   
  - for easy edeq calculation, I've created redundant columns. They are: edeq_restraint, edeq_ec, edeq_sc, edeq_wc, edeq_global. Corresponding edeq4_restraint and edeq6_restraint are also here if you care    
- **PSWQ**: RPS used 10-item version instead of 16. therefore the maximum possible value for this scale on RPS is 50 instead of 96. may make sense to standardize if using total score. R15 doesn't have PSWQ    
- **PCLC** is *NOT* in DH3 or R15    
- **EPSI** not in DH3, online IE, or in vivo     
- **PSWQ** RPS uses 10-item version

In sum, this dataset contains the following measures: EDE-Q, BDI, FOFM, OCI, SAAS, EPSI, FMPS, EFQ, PSWQ, PCLC   