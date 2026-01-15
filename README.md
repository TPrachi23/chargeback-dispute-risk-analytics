# Chargeback & Dispute Risk Analytics

## Project Overview
This project analyzes **post-transaction payment risk** by examining chargebacks and disputes across transactions, merchants, and customer behavior. Using transaction-level and dispute-level data, the analysis identifies **chargeback drivers, win/loss patterns, merchant risk cohorts, and policy-relevant insights** to support loss mitigation and payments risk strategy decisions.

The project simulates a real-world **fintech / payments risk analytics workflow** commonly used by card networks, payment processors, and e-commerce platforms.

---

## Business Problem
High chargeback rates expose payment ecosystems to:
- Direct financial losses (disputed amounts + fees)
- Card network monitoring programs
- Increased operational overhead
- Merchant termination or restrictions

The objective is to **identify where risk concentrates, why disputes occur, and which operational or policy levers improve outcomes**.

---

## Key Questions Answered
- Which merchants and cohorts drive **chargeback rate breaches**?
- Which **dispute reasons** contribute most to financial loss?
- What factors influence **dispute win vs loss outcomes**?
- How do **merchant tenure and behavior** affect risk exposure?
- Which dispute types are **operationally preventable**?

---

## Core Metrics
- **Chargeback Rate** = Disputes ÷ Transactions  
- **Win Rate** = Won Disputes ÷ Total Disputes  
- **Net Loss** = Lost Dispute Amount + Chargeback Fees  
- **Net Loss Rate** = Net Loss ÷ Transaction Volume  
- **Evidence Quality Score**
- **Response Time (Days)**

---

## Data Model (Synthetic, Industry-Realistic)

### Transactions
- Transaction ID  
- Date  
- Merchant ID  
- Amount  
- Channel (Card-Present / Card-Not-Present)  
- Country  

### Disputes
- Dispute ID  
- Reason Code (Fraud, No Auth, Not Received, etc.)  
- Dispute Amount  
- Outcome (Win / Loss)  
- Evidence Quality Score  
- Response Time  
- Chargeback Fee  

### Merchants
- Risk Tier (Low / Medium / High)  
- Tenure (Months)  
- Monthly Volume  
- Refund Rate  

---

## Tools & Techniques
- **Python (Pandas, NumPy)**
- Risk Metrics Engineering
- Cohort Analysis (Tenure × Risk Tier)
- Win/Loss Driver Analysis
- Policy & Merchant Behavior Analysis
- Data Visualization (Matplotlib)

---

## Key Insights
- **Early-tenure, high-risk merchants** exhibit the highest chargeback and loss rates
- Fraud disputes dominate volume but show **low win rates**
- Operational disputes (duplicate, processing errors) show **significantly higher win rates**
- **Evidence quality and faster response times** materially improve dispute outcomes
- Risk is unevenly distributed — **targeted controls outperform blanket policies**

---

## Repository Structure
chargeback-dispute-risk-analytics/
├── README.md
├── chargeback_dispute_risk_analytics.py
├── data/
│ ├── merchants.csv
│ ├── transactions.csv
│ └── disputes.csv
└── outputs/
├── merchant_month_risk_metrics.csv
├── dispute_reason_overall.csv
├── dispute_reason_by_tier.csv
├── win_loss_drivers_slices.csv
├── cohort_risk_summary.csv
├── overall_chargeback_rate_trend.png
├── dispute_volume_by_reason.png
├── win_rate_by_evidence_bucket.png
└── cohort_chargeback_rate_table.png


---

## How to Run
1. Clone the repository  
2. Run `chargeback_dispute_risk_analytics.py` (or notebook version)  
3. Outputs are generated in the `outputs/` directory  

Designed to run seamlessly in **Google Colab or local Python environments**.

---

## Use Cases
- Payments Risk & Fraud Analytics  
- Fintech & Card Network Risk Monitoring  
- Merchant Risk Strategy  
- Trust & Safety Analytics  
- Policy & Compliance Decision Support  

---

## Why This Project Matters
This project demonstrates the ability to:
- Translate payment data into **actionable risk insights**
- Identify **loss drivers and preventable disputes**
- Support **policy, onboarding, and merchant strategy** with analytics
- Communicate findings clearly to technical and non-technical stakeholders

---

## Author
**Prachi Thakur**  
Data & Risk Analytics  
GitHub: https://github.com/TPrachi23
