
![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Last Commit](https://img.shields.io/github/last-commit/femarivera/Alfa-errors-Two-Sample-t-test
)
![Issues](https://img.shields.io/github/issues/femarivera/Alfa-errors-Two-Sample-t-test
)

# R Simulations: Understanding Alpha Errors in Two-Sample *t*-Tests  

This project explores **α-errors (Type I errors)** in a two-sample *t*-test under different sample sizes.  
The idea: simulate, test, and visualize how often we falsely reject the null hypothesis when the samples actually come from the **same normal distribution**.  

---

## How it works  

1. **Simulation setup**  
   - Define a vector of sample sizes → `sample_sizes`  
   - Set significance level → `sign_level`  
   - Choose number of simulations → `total_simulations`  
   - Specify tests per simulation → `tests_per_simulation`  

2. **Within each simulation**  
   - Two samples of equal size are drawn from a normal distribution (`rnorm()` with random mean & sd).  
   - A series of *t*-tests is performed.  
   - Results are classified as **significant / not significant** based on `sign_level`.  

3. **Output**  
   - For each sample size, the ratio of significant tests is computed.  
   - Results are visualized with **boxplots**, showing the empirical Type I error vs. the theoretical `sign_level`.  

---

## Example Output  

Boxplots of α-errors across simulations, with the significance threshold marked for reference:  

---
