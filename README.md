# Dynamic Technology Adoption in the Smartphone Industry

This repository contains the full pipeline and empirical code for my PhD thesis:  
**"Dynamic Technology Adoption in the Smartphone Industry with Exogenous Technology Shifts"**

## 📊 Overview

This research estimates a structural model of firm behavior in the U.S. smartphone industry from 2011–2021. Firms decide when to adopt new cellular technologies (e.g., 4G, 4.5G, 5G), while facing demand-side incentives shaped by consumer preferences and competition.

The project combines:
- Discrete Choice Demand Estimation (Berry-Levinsohn-Pakes / BLP)
- Dynamic Supply Modeling (Rust-style Nested Fixed Point)
- Real-world data from IDC, PhoneArena, and exchange rate sources

---

## 🧱 Repository Structure

| Folder                      | Description                                                                 |
|--------------------         |-----------------------------------------------------------------------------|
| `Data_cleaning_pipeline/`   | Clean and merge raw smartphone data from IDC, PhoneArena, etc.              |
| `demand_estimation/`        | Implements BLP-style demand estimation using 2-stage GMM.                   |
| `supply_dynamics/`          | Dynamic modeling of firm adoption decisions under technology shifts.        |
| `data/`                     | Public-safe processed samples and file templates (not raw IDC data).        |
| `docs/`                     | Additional writeups or visualization figures.                               |

---

## 🗃️ Data Sources

- IDC product-level shipment and specs data (2011–2021)
- PhoneArena smartphone hardware specs
- Federal Reserve foreign exchange rate data (Yen, Won, Yuan to USD)

⚠️ Proprietary data (IDC, PhoneArena) is not included in this repo. 
---

## 📈 Estimation Flow

1. **Data Cleaning (`data_pipeline/`)**  
   Prepare a panel of smartphone products with consistent brand-model specs and technology classifications (4G, 4.5G, 5G).

2. **Demand Estimation (`demand_estimation/`)**  
   Estimate consumer preferences using BLP-style random coefficients logit demand. Instruments include cost shifters and product characteristic variation.

3. **Dynamic Supply Modeling (`supply_dynamics/`)**  
   Estimate firm adoption behavior using a dynamic discrete choice model. Technology availability is exogenous and evolves over time.

---

## 📎 Related Links

- [My Website](https://econaneesharora.com/)
- [LinkedIn](https://www.linkedin.com/in/aneesharora)
<!-- - [My Blog (BLP Series)](https://sites.google.com/view/aneesharora/blog)   -->


---

## 📄 License

MIT License. Please cite appropriately if reusing methods or materials.

