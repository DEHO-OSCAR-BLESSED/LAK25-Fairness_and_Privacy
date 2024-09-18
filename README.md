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

We used the the DOMIAS， which is a density-based Membership Inference Attack (MIA) model proposed in (Van Breugel et al., 2023). This model designed to detect local overfitting in synthetic data generators. It operates by comparing the densities of real and synthetic data distributions to infer whether a specific real sample was part of the training data. If the synthetic data model overfits in certain regions, DOMIAS identifies this overfitting by computing a membership score based on the ratio of the two densities:


  > S(x) = \frac{p_{\text{gen}}(x)}{p_{\text{real}}(x)}

Here:

    >  pgen(x) is the density of the synthetic data.
    >  preal(x) is the density of the real data.

A higher score S(x)S(x) suggests a greater likelihood that the sample xx was used during training, particularly in overfitted regions where the synthetic data mimics the real data closely.

### (4)	K-anonymization

K-anonymity is a property of a dataset that indicates the re-identifiability of its records. A dataset is k-anonymous if quasi-identifiers for each person in the dataset are identical to at least k – 1 other people also in the dataset (Google, 2015).

## Reference
- Google (2015). Computing k-anonymity for a dataset. [online] Google Cloud. Available at: https://cloud.google.com/sensitive-data-protection/docs/compute-k-anonymity
- Horan , C. (2021). Wasserstein Distance and Textual Similarity. Neptune.ai. https://neptune.ai/blog/wasserstein-distance-and-textual-similarity
- Nielsen, F. (2019). On the Jensen–Shannon Symmetrization of Distances Relying on Abstract Means. Entropy, 21(5), 485. https://doi.org/10.3390/e21050485
- Van Breugel, B., Sun, H., Qian, Z., & Van Der Schaar, M. (2023). Membership Inference Attacks against Synthetic Data through Overfitting Detection. 206. https://arxiv.org/pdf/2302.12580
