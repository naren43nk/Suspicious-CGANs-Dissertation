# Suspicious-CGANs-Dissertation  
**Enhancing Suspicious Transaction Detection using Conditional GANs with Typology Control: A Realism, Privacy, and Generalizability Study**

---

## Project Overview
This repository contains the research artifacts, code, and experimental outputs for my MSc Data Science dissertation at the University of Surrey.  
The dissertation investigates whether **Conditional Generative Adversarial Networks (CGANs)** with typology conditioning can improve suspicious transaction detection under **extreme class imbalance** in the **SAML-D** dataset (synthetic AML benchmark dataset).

Key contributions include:
- Implementation of **CGAN** and **WGAN-GP with typology control**.  
- Evaluation of **realism** (KL divergence, JS divergence, Wasserstein distance, PCA, UMAP).  
- **Classifier utility benchmarking** (XGBoost trained on real, augmented, synthetic, and SMOTE/ROS baselines).  
- **Privacy analysis** using Membership Inference Attacks (MIA) and Differentially Private CGAN (DP-CGAN).  
- **Fairness and explainability** with SHAP values, demographic parity, and equal opportunity metrics.  
- **Generalization tests** across temporal splits to assess drift robustness.  

---

## Repository Structure

```text
Suspicious-CGANs-Dissertation/
│
├── notebooks/      # Jupyter notebooks for each experimental phase
├── results/        # Evaluation outputs (CSV metrics, summary reports)
├── plots/          # Figures and visualizations (UMAP, SHAP, drift curves)
├── .gitignore      # Excludes large datasets/models
└── README.md       # Project overview (this file)
```
---

## Methodology
The dissertation was executed in **8 structured phases**, aligned to academic and experimental rigor:

1. **Data Preprocessing & EDA** – feature engineering, imbalance quantification, drift baselining.  
2. **CGAN Training (WGAN-GP variant)** – typology conditioning, KL-divergence monitoring.  
3. **Classifier Evaluation** – XGBoost utility tests under different augmentation settings.  
4. **Realism Analysis** – statistical & visual similarity metrics.  
5. **Privacy Evaluation** – MIA, DP-CGAN, privacy–utility trade-off.  
6. **Generalization Tests** – temporal drift and cross-quarter validation.  
7. **Explainability & Fairness** – SHAP analyses, demographic parity & EO gap metrics.  
8. **Final Summary & Discussion** – synthesis of realism, privacy, fairness, and utility findings.  

---

##  Key Results (Highlights)
- **Macro-F1 improvement** for rare typologies with CGAN augmentation.  
- **KL divergence < 1** achieved with WGAN-GP, ensuring stable synthetic generation.  
- **DP-CGAN** demonstrated reduced MIA vulnerability, though at the cost of classifier utility.  
- SHAP analyses revealed that augmentation primarily strengthened recognition of minority typologies.  
- Fairness audits indicated **balanced detection rates** across typologies with CGAN-based augmentation.  

---

## Ethical Considerations
- The project uses the **SAML-D dataset**, a **synthetic AML dataset** widely used in academic research, ensuring **no real customer data** is processed.  
- Privacy-preserving methods (DP-CGAN, MIA audits) were explicitly integrated to balance **utility with confidentiality**.  
- All experiments comply with academic and institutional ethical standards.  

---

##  How to Reproduce
1. Clone the repository:

   git clone git@github.com:naren43nk/Suspicious-CGANs-Dissertation.git
   cd Suspicious-CGANs-Dissertation

2.Install dependencies (recommended with conda/venv):
pip install -r requirements.txt

3.Navigate to the notebooks/ folder and follow the experimental phases in order.

## Citation

If referencing this work in academic contexts:

Mohan, N. (2025). Enhancing Suspicious Transaction Detection using Conditional GANs with Typology Control: A Realism, Privacy, and Generalizability Study. MSc Dissertation, University of Surrey.

## Acknowledgements

Supervisor: Dr. Nishanth Sastry, University of Surrey

Faculty of Computer Science and Electronic Engineering

My family and peers for their continuous support
