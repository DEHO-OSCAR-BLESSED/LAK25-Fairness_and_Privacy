# LAK25-Fairness_and_Privacy

This repository contains all supplementary results for our paper submitted to LAK25 conference.

## privacy evaluation metrics

### (1)	Jensen-Shannon divergence (JSD)
   The Jensen–Shannon divergence (JSD) is a symmetrized and smoothed version of the Kullback–Leibler divergence. It is defined by (Nielsen, 2019)
 
 > JSD(P, Q) = (1/2) * (D_KL(P || M) + D_KL(Q || M))

 > - D_KL(Q || M)) represents the Kullback-Leibler divergence from distribution P to distribution Q.
 > - P and Q are the two probability distributions being compared.
 > - M is the average distribution, defined as (P+Q)/2

### (2)	Wasserstein distance (WD)

![image](https://github.com/ql909/mathematical_definitions/assets/108169831/7b64ead0-18cc-4d5c-9f23-416344aeba9a) (Horan , 2021)

### (3)	Membership interference attack (MIA)

### (4)	K-anonymization

K-anonymity is a property of a dataset that indicates the re-identifiability of its records. A dataset is k-anonymous if quasi-identifiers for each person in the dataset are identical to at least k – 1 other people also in the dataset.
