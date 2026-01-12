# A Study on Effective False Discovery Rate (FDR) Control Methods in Multiple Testing

---

## 1. Research Overview

This study addresses the accumulation of **Type I errors** in **multiple hypothesis testing**.  
Traditional control metrics such as the **Family Wise Error Rate (FWER)** are overly conservative as the number of hypotheses increases, leading to a significant loss of statistical power.

To overcome these limitations, the study introduces **False Discovery Rate (FDR)** as an alternative error criterion and focuses on evaluating the **Benjamini–Hochberg (BH) procedure**.  
The research examines its theoretical validity and empirical performance under **positive regression dependency (PRDS)** through both simulation and real-world data analysis.

---

## 2. Research Topics

- Problem of inflated Type I error in multiple hypothesis testing  
- Limitations of FWER (Family Wise Error Rate) control methods  
- Introduction and definition of FDR (False Discovery Rate)  
- Step-by-step mechanism of the Benjamini–Hochberg (BH) procedure  
- Evaluation of BH stability under correlated (dependent) hypotheses  
- Comparative analysis using simulation and real gene-expression data  

---

## 3. Methods Used

| Category | Method | Author(s) | Description |
|-----------|---------|-----------|--------------|
| **FWER Control** | Bonferroni | – | Divides α by the number of hypotheses (α/m); highly conservative |
|  | Holm | Holm (1979) | Sequentially adjusted Bonferroni method |
| **FDR Control** | Benjamini–Hochberg (BH) | Benjamini & Hochberg (1995) | Controls FDR at a specified level q under independence or positive dependence |
|  | Benjamini–Yekutieli (BY) | Benjamini & Yekutieli (2001) | Extension applicable under arbitrary dependency structures |

---

## 4. Simulation Study (Overview & Results)

**Overview**  
- Number of hypotheses: 200  
- Sample size: 50 per group  
- Correlation levels: ρ = 0, 0.1, 0.5, 0.9  
- Methods compared: No Correction, Bonferroni, Holm, BH (Benjamini-Hochberg)
- Repetitions: 500  
- Evaluation metrics: Statistical Power

**Results Summary**

| Condition | Method | Power | FDR Control | Remarks |
|------------|---------|--------|--------------|----------|
| Independent (ρ = 0) | Bonferroni / Holm | Low | Stable | Overly conservative |
| Independent (ρ = 0) | BH | High | Appropriate | Efficient and reliable |
| Positive Dependence (ρ = 0.5, 0.9) | BH | Maintained | Stable | Valid under dependency |

➡ **Summary:**  
The BH procedure achieved higher power than FWER-based methods while maintaining FDR control.  
Even under positive correlation, BH remained effective, providing a **practical balance between power and error control** for real-world data settings.

---

## 5. Real Data Analysis (Overview & Results)

**Overview**  
- **Dataset:** Cervical cancer gene-expression data  
- **Groups:** 28 patients vs. 24 controls  
- **Number of genes:** 20,261  
- **Goal:** Identify genes with significant expression differences between groups  
- **Methods applied:** No Correction, Bonferroni, Holm, Benjamini–Hochberg (BH)

**Results Summary**

| Method | Number of Rejected Hypotheses |
|---------|-------------------------------|
| No Correction | 8,514 |
| Benjamini–Hochberg (BH) | 6,417 |
| Bonferroni / Holm | 780 |

➡ **Summary:**  
Bonferroni and Holm detected only 780 significant genes, showing their conservativeness.  
In contrast, the BH procedure identified 6,417 significant genes while maintaining proper FDR control,  
demonstrating its **robustness and practical utility for high-dimensional biological data**.

---

## 6. References

1. Benjamini, Y., & Hochberg, Y. (1995). *Controlling the False Discovery Rate: A Practical and Powerful Approach to Multiple Testing.*  
   Journal of the Royal Statistical Society: Series B (Methodological), 57(1), 289–300.  

2. Benjamini, Y., & Yekutieli, D. (2001). *The Control of the False Discovery Rate in Multiple Testing under Dependency.*  
   The Annals of Statistics, 29(4), 1165–1188.

---
## * Included File

| Filename | Description |
|-----------|-------------|
| `다중 검정에서의 효과적인 거짓 발견 확률 제어 방법 연구.pdf` | Final UROP research report |
