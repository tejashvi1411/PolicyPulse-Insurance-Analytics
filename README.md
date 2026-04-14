# 📊 PolicyPulse Insurance Premium & Payout — Power BI Dashboard

> An interactive Power BI dashboard for an insurance company, analyzing **premium collections, policyholder demographics, investment returns, claims, and sales performance** — all in one place.


---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Dashboard Pages](#-dashboard-pages)
- [Data Model](#-data-model)
- [Key Insights](#-key-insights)
- [Tech Stack](#-tech-stack)
- [File Structure](#-file-structure)
- [Getting Started](#-getting-started)
- [What's Next](#-whats-next)
- [Author](#-author)

---

## 🧭 Project Overview

The **PolicyPulse Dashboard** provides a 360° analytical view of an insurance company's performance. It is built to support business leaders, financial teams, and analysts in making **data-driven decisions** by surfacing KPIs across premiums, payouts, investments, and the sales hierarchy.

### KPIs Tracked

| KPI | Description |
|-----|-------------|
| 💰 Total Premium Collected | Aggregate premiums across all active policies |
| 📋 Policy Count by Category | Breakdown of policy volume by type |
| 📤 Payout & Claim Ratio | Claims vs. total premium to assess payout exposure |
| 📈 Investment vs. Maturity Returns | Fund performance relative to maturity obligations |
| 🛡️ Annual Premium vs. Protection Value | Coverage adequacy relative to policyholder payments |
| 🏆 Sales Performance by Hierarchy | Agent → Regional → Zonal performance drill-down |
| 👤 Policyholder Demographics | Age, gender, and location segmentation |

---

## 🖥️ Dashboard Pages

### 1. Insurance Overview
High-level executive summary showing total premium, active policy count, payout ratio, and claims overview at a glance.


---

### 2. Insurance Summary (Policyholder Details)
Customer segmentation by **gender**, **age group**, and **geographic location** — answering *"Who are our customers and where are they?"*



---

### 3. Investment vs. Maturity
Side-by-side comparison of invested capital against maturity payout amounts — surfacing fund utilization efficiency across plans and policy types.


---

### 4. Annual Premium vs. Protection Value
Evaluates whether customers receive proportionate protection value relative to the premiums they pay — critical for pricing strategy and product design decisions.


---

### 5. Premium Analysis
Trend analysis of premium collections over time, across regions and policy types — used for **forecasting** and identifying growth patterns or seasonal dips.



---

### 6. Sales Hierarchy (Chart & Matrix Views)
Dual-view of the sales organization's performance:
- **Chart View** — visual breakdown of Zonal → Regional → Agent performance
- **Matrix View** — drill-down table with precise numbers at each level



---

##  Data Model

Built on a clean **Star Schema** with one central fact table and six dimension tables.
FCT.Insurance_Policy_Table (Fact)
│
├── DM.Customer_Detail_Table
├── DM.Insurance_Agent_Table
├── DM.Policy_Type
├── DM.Policy_Protection_Plan
├── DM.Regional_Manager
└── DM.Zonal_Manager

| Table | Type | Contains |
|-------|------|----------|
| `FCT.Insurance_Policy_Table` | **Fact** | Policy transactions — premiums, payouts, investments, dates |
| `DM.Customer_Detail_Table` | Dimension | Age, gender, location per policyholder |
| `DM.Insurance_Agent_Table` | Dimension | Agent details linked to each policy |
| `DM.Policy_Type` | Dimension | Life, health, motor, and other policy categories |
| `DM.Policy_Protection_Plan` | Dimension | Coverage tiers, protection values, plan metadata |
| `DM.Regional_Manager` | Dimension | Regional management hierarchy |
| `DM.Zonal_Manager` | Dimension | Zonal management hierarchy (above regional) |

---

## Key Insights

### 1. Investment-to-Maturity Gaps Exist Across Products
Not all protection plans return proportional maturity values. Some plans show a notably lower return ratio, signaling candidates for product restructuring or repricing.

### 2. Customer Demographics Are Concentrated
The 30–50 age group typically drives the majority of premium contribution. Without segmentation, this skew is invisible — and marketing spend can be misallocated as a result.

### 3. Protection Value Misalignment Is a Hidden Opportunity
Lower-tier premium customers often hold disproportionately high protection values compared to higher-tier customers — a classic cross-sell and upsell opportunity that gets missed without direct visualization.

### 4. Sales Performance Follows the Pareto Principle
~20% of agents account for the vast majority of premiums collected. The Sales Hierarchy page makes it immediately clear *which* regions and managers sit behind top performers — enabling better coaching and structural replication.

### 5. Payout Ratios Differ Significantly by Policy Type
Aggregate payout ratios mask risk concentration. Health, life, and motor policies each carry different payout profiles — and segmenting by type reveals which categories require closer actuarial attention.

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| **Power BI Desktop** | Report design, DAX measures, and publishing |
| **Microsoft Excel / CSV** | Source data |
| **Power Query (M)** | Data cleaning and transformation |
| **DAX** | Custom KPI measures — ratios, trends, running totals |

**Visual types used:** Pie Chart · Donut Chart · Treemap · Stacked Bar · Area Chart · Clustered Column · Line + Combo Chart · Table · Matrix

---

## File Structure
📦 Insurance-Premium-Payout-Power-BI-Project
┣ 📊 Tru Secure CreDebit Dashboard.pbix   ← Main Power BI file
┣ 📄 FCT.Insurance_Policy_Table.csv        ← Fact table
┣ 📄 DM.Customer_Detail_Table.csv
┣ 📄 DM.Insurance_Agent_Table.csv
┣ 📄 DM.Policy_Type.csv
┣ 📄 DM.Policy_Protection_Plan.csv
┣ 📄 DM.Regional_Manager.csv
┣ 📄 DM.Zonal_Manager.csv


---

## 🧠 Skills Demonstrated

- Data Cleaning & Transformation (Power Query / M)
- Star Schema Data Modeling & Relationships
- DAX Measures & KPI Calculations
- Dashboard Design & UX for Business Users
- Business Intelligence & Stakeholder Reporting

---
