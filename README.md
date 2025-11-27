# 📊 PhonePe Pulse Data Visualization (2018–2023)

![PhonePe Pulse](https://img.shields.io/badge/PhonePe-Pulse-purple?logo=phonepe&logoColor=white)
[![Tableau](https://img.shields.io/badge/Tableau-Visualization-yellow?logo=powerbi)](https://powerbi.microsoft.com/)
![EDA](https://img.shields.io/badge/Focus-Fin%20Tech%20Insights-purple)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

An interactive Tableau dashboard analyzing **PhonePe digital payments trends** across India from **2018 to 2023**, featuring geo-visualization, KPIs, time-series insights, transaction trends, user growth, and device brand distribution.

---

# 📑 Table of Contents

- [📌 Overview](#-overview)
- [🎯 Objectives](#-objectives)
- [🗂 Data Sources](#-data-sources)
- [🧱 Architecture](#-architecture)
- [📦 What’s Included](#-whats-included)
- [🔍 Key Insights](#-key-insights)
- [🧩 Data Model](#-data-model)
- [📊 Dashboard Pages](#-dashboard-pages)
- [📁 Repository Map](#-repository-map)

---

## 📌 Overview

This project visualizes PhonePe Pulse data using **Tableau**, offering a unified view of India’s digital payment ecosystem.  
It analyzes trends across **states, districts, years, quarters, user behavior, device brands**, and **transaction categories**.

The dashboard provides:

- Interactive map visualizations
- Trend analysis
- State & district performance
- KPI summary
- Top-performing regions

---

## 🎯 Objectives

- Analyze India’s digital payment patterns using PhonePe Pulse open-source data
- Build a **PhonePe Pulse–style interactive Tableau dashboard**
- Provide actionable insights on:
  - Transaction volume & value
  - User activity & growth
  - Geographical performance
  - Device (brand) distribution
- Enable data exploration through interactive filters (Year, Quarter, State, District, Type etc.)

---

## 🗂 Data Sources

Dataset extracted from publicly available **PhonePe Pulse GitHub repository**, including:

- `aggregated_transaction.csv`
- `aggregated_user.csv`
- `map_transaction.csv`
- `map_user.csv`
- `top_transaction.csv`
- `top_user.csv`

These datasets were pre-processed and cleaned before visualization.

---

## 🧱 Architecture

```
📦PhonePe Pulse Data
│
├── Data Cleaning & Preprocessing (CSV)
│
├── Tableau Data Modeling
│ ├── Relationships (Not Joins)
│ ├── KPI Calculations (YoY, CAGR, ATS)
│ └── Hierarchies (Year → Quarter → State)
│
├── Dashboard Development
│ ├── Geo Visualization (State & District)
│ ├── Trend Analysis
│ ├── Top 10 Insights
│ ├── Device Brand TreeMap
│ └── Interactive Filters
│
└── Final Dashboard (Tableau)
```

---

## 📦 What’s Included

- 📁 Cleaned CSV datasets
- 📊 Tableau Workbook (`.twbx`)
- 🗺️ Geo Analysis (State & District)
- 📈 Trend Visualization
- 🔟 Top 10 Analysis
- 🗂 PPT Presentation with insights
- 📝 README documentation

---

## 🔍 Key Insights

### ⭐ **1. Massive Growth**

- Digital payment value increased from **₹6T (2018)** → **₹64T (2022)**
- Over **10X growth in 5 years**

### ⭐ **2. Top Performing States**

- Maharashtra
- Karnataka
- Telangana
- Tamil Nadu

These states contribute the highest transaction value.

### ⭐ **3. Metro District Dominance**

- Bengaluru Urban
- Hyderabad
- Chennai
- Mumbai Suburban
- Pune

### ⭐ **4. User Device Share**

- Xiaomi & Samsung together command majority of PhonePe users
- Indicates strong penetration among middle-income Android users

### ⭐ **5. Regional Trends**

- South India dominates high-value transactions
- North India dominates user volume due to population size

---

## 🧩 Data Model

The dashboard uses **Tableau Relationships** (NOT joins) for performance efficiency.

### Relationships:

| Primary Table          | Related Table   | Relationship Keys     |
| ---------------------- | --------------- | --------------------- |
| aggregated_transaction | aggregated_user | Year, Quarter, State  |
| aggregated_transaction | map_transaction | Year, Quarter, State  |
| aggregated_user        | map_user        | State, District, Year |
| aggregated_transaction | top_transaction | State                 |
| aggregated_user        | top_user        | State                 |

### Calculated Fields:

- **Year-Quarter Key**
- **Total Value & Total Transactions**
- **Average Ticket Size (ATS)**
- **Active Users Count**

---

## 📊 Dashboard Pages

### **1️⃣ KPI Overview**

- Total Value
- Total Transactions
- Average Ticket Size
- Active Users

### **2️⃣ Geo Visualization**

- State-wise heatmap
- District-wise bubble map

### **3️⃣ Trend Analysis**

- Year-wise line chart (2018–2023)
- YoY / QoQ growth

### **4️⃣ Top 10 States**

- By Transaction Value
- By User Count

### **5️⃣ Device Brand Share**

- Treemap of smartphone brands

### **6️⃣ Filters Panel**

- State
- District
- Year & Quarter
- Brand
- Transaction Type
- Amount Slider

---

## 📁 Repository Map

```
📦 PhonePe-Pulse-Tableau-Dashboard
│
├── 📊 Dashboard
│ └── PhonePePulse.twbx
│
├── 🗂 Data
│ ├── aggregated_transaction.csv
│ ├── aggregated_user.csv
│ ├── map_transaction.csv
│ ├── map_user.csv
│ ├── top_transaction.csv
│ └── top_user.csv
│
├── 📝 Presentation
│ └── PhonePe_Pulse_Presentation.pptx
│
└──📄 README.md

```

---

## 👨‍💻 Author

**Neeraj Kumar**

---
