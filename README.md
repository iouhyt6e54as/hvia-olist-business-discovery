# HVIA Task 01 — Olist Business Discovery

**Data Analysis Internship — Trial Task**
Prepared for: **HVIA — Data & AI Solutions**

A business-first exploration of the [Olist Brazilian E-Commerce public dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) — understanding the company, exploring the data, extracting business-relevant findings, and proposing a Data & AI solution Olist could realistically use.

---

## 🎯 Objective

This project follows the workflow requested by HVIA:

**Understand → Analyze → Propose → Pitch**

Rather than producing a fixed list of charts, the goal was to think like a business analyst:
research the company independently, explore the dataset without being spoon-fed, find patterns
worth investigating, and connect those findings to a realistic Data/AI solution.

## 🏢 About Olist

Olist is a Brazilian retail-technology company (founded 2015, Curitiba) that helps small and
medium-sized merchants sell across 170+ marketplaces (Mercado Livre, Amazon, Shopee, and more)
through one integrated hub — covering marketplace integration, ERP, payments/credit, logistics,
and AI-driven tools. Full details are in the notebook's Company Research section.

## 🗂️ Dataset

**Olist Brazilian E-Commerce Public Dataset** (Kaggle, public, anonymized)
~100,000 real orders placed between 2016–2018 across multiple Brazilian marketplaces.

🔗 Source: https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

The dataset is provided as 9 CSV files (customers, orders, order items, payments, reviews,
products, sellers, geolocation, category translation) connected through shared ID columns.
The table relationships are explained in detail inside the notebook.

> **Note:** raw CSV files are not included in this repository due to size. Download them from
> the Kaggle link above and place them in a folder named `dataset/` in the project root before
> running the notebook.

## 📊 What's Inside the Notebook

| Section | Content |
|---|---|
| 1. Company Research | Who Olist is, business model, customers, ecosystem |
| 2. Dataset Understanding | Table structure, relationships, analytical grain |
| 3–5. Data Loading, Audit & Merge | Loading, quality checks, building the master analysis table |
| 6–7. Business Questions & EDA | Sales trend, geography, delivery performance, category performance, payments, seller concentration, repeat purchase behavior |
| 8. Key Findings | Summary of the most important patterns found in the data |
| 9. Business Interpretation | What the findings mean for Olist's operations |
| 10. HVIA Solution Ideas | Two concrete Data/AI solution proposals grounded in the findings |
| 11. Outreach Draft | Sample LinkedIn outreach message to Olist |
| 12. Limitations & Next Steps | Honest caveats about the data and analysis |

## 🔑 Key Findings (highlights)

- **8.1%** of delivered orders arrived after their estimated delivery date — and late orders
  received noticeably lower review scores than on-time ones. Delivery reliability is the
  strongest satisfaction signal found in the data.
- Demand is geographically concentrated: **São Paulo alone accounts for ~42%** of delivered
  orders, and the top 3 states cover **~67%**.
- Revenue is concentrated among sellers: the **top 10% of sellers generate ~66%** of total
  observed item value — a classic long-tail pattern.
- Only **~3%** of unique customers placed more than one order within the observed period.

## 💡 Proposed HVIA Solutions

1. **Predictive Delivery Risk System** — flag orders at high risk of late delivery at the point
   of purchase, so Olist can intervene before it damages seller reputation and customer trust.
2. **Seller Growth & Health Analytics** — a scoring/recommendation layer that helps the
   long tail of small/medium sellers (not just the top performers) grow, since revenue is
   heavily concentrated at the top today.

## 🛠️ Tools Used

- Python 3
- pandas, numpy
- matplotlib
- Jupyter Notebook

## ▶️ How to Run

```bash
# 1. Clone this repository
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>

# 2. Install dependencies
pip install pandas numpy matplotlib jupyter

# 3. Download the dataset from Kaggle and place the 9 CSV files in a folder named "dataset/"
#    https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

# 4. Launch the notebook
jupyter notebook olist_analysis_final.ipynb
```

## ⚠️ Limitations

- The dataset covers a historical period (2016–2018) and does not reflect Olist's current
  operations.
- Findings are descriptive/associative, not causal.
- Some fields (review text, a few delivery timestamps) contain missing values.
- Repeat-purchase rate is measured only within the observed dataset window.

## 👤 Author

# **Shahd Ahmed Farghaly**
Data Analysis Trial Task — HVIA Data & AI Solutions
# shahdfarghaly2005@gmail.com
*This project was completed as part of an HVIA Data & AI Solutions internship trial task,
evaluating research, analytical thinking, and business communication skills using a real-world
dataset.*
