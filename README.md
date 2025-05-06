# 🧪 Colistin_PopPK_Model

This repository contains a population pharmacokinetic (PopPK) model of **colistin** and its prodrug **colistin methanesulfonate (CMS)** in **critically ill ICU patients**, developed using **Monolix**. The aim is to optimize dosing strategies in patients with variable renal function and renal replacement therapy (RRT) status by achieving therapeutic **PK/PD targets (AUC/MIC ≥ 60)** while minimizing toxicity.

---

## 📌 Project Highlights

- ✅ Developed a **parent-metabolite PK model** using Monolix.
- ✅ Incorporated covariates including **creatinine clearance (CrCL)**, **age**, **weight**, and **RRT**.
- ✅ Used **SAEM algorithm** for model estimation and diagnostics (GOF, VPC).
- ✅ Simulated dosing regimens and individualized exposure outcomes.

---

## 🧬 Model Description

### Parent Drug (CMS):
- **Route**: Extravascular (oral)
- **Absorption**: First-order (`ka`)
- **Distribution**: Two-compartment model (`V`, `k12`, `k21`)
- **Elimination**: Linear (`k`)
- **Conversion**: Transformed to colistin via `Kpm`

### Metabolite (Colistin):
- **Compartment**: One-compartment (`V`)
- **Elimination**: Linear (`km`)
- **No back-conversion assumed**

---

## 🧰 Tools Used

| Category          | Tools / Methods                         |
|-------------------|------------------------------------------|
| PopPK Modeling    | Monolix (SAEM, SCM/COSSAC)               |
| Data Analysis     | R (ggplot2, dplyr), VPCs, GOF            |
| Simulation        | Post hoc parameter simulation (AUC/MIC)  |
| Model Diagnostics | Residuals, shrinkage, bootstrap (planned)|

---

## 📁 Project Structure

