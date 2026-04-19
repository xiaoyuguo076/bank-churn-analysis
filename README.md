# Bank Customer Churn Analysis

## Project Overview
This project addresses a core business problem in retail banking: **customer churn**. Acquiring new customers is significantly more expensive than retaining existing ones, making churn prevention a high-priority objective. The analytical question is: *What key demographic and behavioural factors predict whether a bank customer will churn?*

The target audience includes junior data analysts and product managers who need actionable insights to design effective retention strategies. The final product is a clear, visual report highlighting risk factors such as age, account balance, complaints, and active membership status.

## Dataset
- **Source**: Kaggle – [Bank Customer Churn Records](https://www.kaggle.com/datasets/radheshyamkollipara/bank-customer-churn)
- **Access Date**: 17 April 2026
- **Description**: 10,000 synthetic customer records from an anonymous multinational bank. Includes demographic attributes (age, gender, geography), account information (tenure, balance, number of products), and a target variable `Exited` (1 = churned, 0 = retained).

## Repository Contents
| File | Description |
|------|-------------|
| `102project419.ipynb` | Complete analytical workflow (data loading, EDA, preprocessing, feature engineering, modeling, evaluation) |
| `Customer-Churn-Records.csv` | Raw dataset (10,000 rows, 18 columns) |
| `README.md` | This file |

## How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/xiaoyuguo076/bank-churn-analysis.git
   ### Key Findings (EDA Highlights)
- **Age**: Customers over 50 have significantly higher churn rates.
- **Balance**: Zero‑balance customers are more likely to churn; high‑balance customers also show elevated risk.
- **Complain**: Customers who filed a complaint have extremely high churn probability.
- **IsActiveMember**: Active members are much less likely to churn.
- **Geography**: Germany has a higher churn rate than France or Spain.

### Feature Engineering
Added `Balance_to_Salary_Ratio` to capture financial dependency (balance / estimated salary). High ratio indicates greater loss risk if churned.

### Model Performance
| Model | Accuracy | Precision | Recall | F1‑Score | ROC AUC |
|-------|----------|-----------|--------|----------|---------|
| Logistic Regression | 0.9987 | 0.9967 | 0.9967 | 0.9967 | 0.9993 |
| Random Forest | 0.9987 | 0.9967 | 0.9967 | 0.9967 | 0.9997 |

### Business Implications
- Target customers who **complained** with retention offers.
- Monitor **older customers (50+)** and **high balance/low salary**.
- Engage **inactive customers** (zero balance, non‑active members).

### Limitations
- Synthetic data (not generalizable to real banks).
- Class imbalance (~20% churn).
- No temporal information.

### AI Tools Disclosure
| Tool | Version | Access Date | Purpose |
|------|---------|-------------|---------|
| DeepSeek | latest (April 2026) | 18 April 2026 | Markdown structure, code comments, phrasing |
| Google Gemini | 1.5 Pro | 18 April 2026 | Debug seaborn, one‑hot encoding examples, disclosure formatting |

### Author
- **Student ID**: Xiaoyu Guo 2472807
- **Course**: ACC102 Mini Assignment – Track 2
- **Repository**: [https://github.com/xiaoyuguo076/bank-churn-analysis](https://github.com/xiaoyuguo076/bank-churn-analysis)
