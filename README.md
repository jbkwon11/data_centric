# Data-Centric AI Design Strategies for College Dropout Prediction Systems

This is the official repository for the paper: **"Data-Centric AI Design Strategies for College Dropout Prediction Systems"**. 

This study demonstrates that data design decisions—such as label refinement and determining data sufficiency—are as critical as algorithmic improvements in building effective early warning systems for student success.

## Overview
Conventional model-centric approaches often overlook the nuances of administrative data. Using over 80,000 real-world academic records, we empirically analyze three key data-centric factors:
1. **Label Design:** Refining borderline cases like zero-horizon dropouts and students on leave.
2. **Data Sufficiency:** Identifying the optimal training set size via learning curve analysis.
3. **Grade-Level Modeling:** Comparing unified models against grade-specific architectures.

## Key Findings
* **Performance Gain:** Refining ambiguous labels to align with predictive goals improved the F1-score for at-risk students from **0.240 to 0.499**.
* **Data Efficiency:** Learning curve analysis revealed a performance saturation point at approximately **12,000 instances**, suggesting that data quality is more important than volume.
* **Statistical Validity:** A **5,000-iteration paired bootstrap test** confirmed that the observed improvements are statistically significant ($p < .05$).

## Repository Structure

The experimental notebooks are organized by the flow of the paper:

### 1. Label Design & Refinement (Experiment 1)
Evaluates the impact of refining Zero-Horizon Dropouts (ZHD) and On-Leave students.
* **Zero-Horizon Dropout (ZHD) Impact:**
  * `1-1_zhd_test_t_0_1.ipynb`
  * `1-1_zhd_test_t_0_2.ipynb`
  * `1-1_zhd_test_t_1_1.ipynb`
  * `1-1_zhd_test_t_1_2.ipynb`
* **On-Leave Case Refinement:**
  * `1-2_leave_F_test_t_1_1.ipynb`
  * `1-2_leave_T_test_t_1_1.ipynb`
  * `1-2_leave_F_test_t_1_2.ipynb`
  * `1-2_leave_T_test_t_1_2.ipynb`

### 2. Statistical Significance Testing (Experiment 2)
* `1-3_sign_test.ipynb`: Implements the **Paired Bootstrap Test (N=5000)** to derive 95% Confidence Intervals (CI) and p-values for AP and F1(opt) metrics. (Used for Table 4 in the paper).

### 3. Data Sufficiency Analysis (Experiment 3)
* `2_sufficiency_t_1_1.ipynb`: Generates learning curves to analyze how model performance scales with training data size.

## Data Availability
Due to institutional privacy regulations (e.g., Personal Information Protection Act) and the sensitive nature of student academic records, the raw dataset (80,000+ rows) used in this study **cannot be shared publicly**. 

However, the provided notebooks include the full execution logs, output metrics, and visualization results to ensure the transparency and reproducibility of the methodology.

## Citation
If you find this repository or our paper useful for your research, please consider citing our work:

```bibtex
@article{kwon2026,
  title={Data-Centric AI Design Strategies for College Dropout Prediction Systems},
  author={Jin Baek Kwon},
  journal={KIPS Transactions on Software and Data Engineering},
  year={2026},
  note={Under Revision}
}
```
## Contact
For any inquiries regarding the code or paper, please contact `jbkwon@sunmoon.ac.kr`.
