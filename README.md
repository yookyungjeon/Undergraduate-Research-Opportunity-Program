# A Study on Effective False Discovery Rate (FDR) Control Methods in Multiple Testing


---

## 1. Research Overview

This project investigates statistical methods for controlling **Type I error** in **multiple hypothesis testing**.  
Traditional approaches that control **FWER (Family Wise Error Rate)** tend to be overly conservative as the number of hypotheses increases, which reduces the overall statistical **power**.  

To address this limitation, the study introduces **FDR (False Discovery Rate)** as an alternative criterion and focuses on the **Benjamini–Hochberg (BH) procedure**, comparing its performance and theoretical validity with FWER-based approaches such as **Bonferroni** and **Holm**.  
Additionally, the robustness of the BH procedure is examined under **positive regression dependency (PRDS)** conditions.

---

## 2. Research Topics

- Problem of inflated Type I error in multiple hypothesis testing  
- Limitations of FWER (Family Wise Error Rate) control methods  
- Introduction and definition of FDR (False Discovery Rate)  
- Step-by-step mechanism of the Benjamini–Hochberg (BH) procedure  
- Validity of the BH procedure under correlated hypotheses (positive dependence)  
- Comparison of statistical power through simulation and real gene-expression data analysis  

---

## 3. Methods Used

| Category | Method | Author(s) | Description |
|-----------|---------|-----------|--------------|
| **FWER Control** | Bonferroni | – | Divides α by the number of tests (α/m); most conservative approach |
|  | Holm | Holm (1979) | Sequentially adjusted Bonferroni correction |
| **FDR Control** | Benjamini–Hochberg (BH) | Benjamini & Hochberg (1995) | Controls FDR at level q under independence or positive dependence |
|  | Benjamini–Yekutieli (BY) | Benjamini & Yekutieli (2001) | Extended version valid under arbitrary dependency structures |

---

## 4. Simulation Design

- **Data structure:**  
  - Number of hypotheses: 200  
  - Sample size: 50 per group  
  - Correlation levels among hypotheses: ρ = 0.1, 0.5, 0.9  
  - 500 Monte Carlo repetitions  

- **Compared methods:**  
  - No Correction  
  - Bonferroni  
  - Holm  
  - Benjamini–Hochberg (BH)  

- **Evaluation metrics:**  
  - Statistical power  
  - False Discovery Rate (FDR)  
  - Type I error control accuracy  

---

## 5. Simulation Results

| Condition | Method | Power | FDR Control | Notes |
|------------|---------|--------|--------------|-------|
| Independent (ρ = 0) | Bonferroni / Holm | Low | Stable | Overly conservative |
| Independent (ρ = 0) | BH | High | Good | Efficient control |
| Positive dependence (ρ = 0.5, 0.9) | BH | Stable | Maintained | Valid under dependence |

**Summary:**  
The BH procedure achieved **higher statistical power** than FWER-based methods and maintained stable FDR control even when the tests were positively correlated.  
These findings confirm that BH provides a **practical balance between power and reliability**, making it well-suited for high-dimensional real-world data such as gene-expression analyses.

---

## 6. References

1. Benjamini, Y., & Hochberg, Y. (1995). *Controlling the False Discovery Rate: A Practical and Powerful Approach to Multiple Testing.*  
   Journal of the Royal Statistical Society: Series B (Methodological), 57(1), 289–300.

2. Benjamini, Y., & Yekutieli, D. (2001). *The Control of the False Discovery Rate in Multiple Testing under Dependency.*  
   The Annals of Statistics, 29(4), 1165–1188.

---
