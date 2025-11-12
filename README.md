---
title: "Call Centre KPI Dashboard - Power BI"
author: "Harsh Arora"
tools: ["Power BI", "Power Query", "DAX", "Excel", "GitHub"]
date: "November 2025"
license: "MIT"
dataset: "Call Center_Call Center.csv"
description: "Interactive Power BI dashboard to monitor call centre performance through key metrics like total calls, duration, response SLA, sentiment, and channel performance."
---

# 📞 Call Centre KPI Dashboard — Power BI

An interactive Power BI dashboard designed to visualize and analyze key performance indicators (KPIs) for a call centre.  
The dashboard helps stakeholders monitor call volume, performance trends, SLA compliance, and customer sentiment to make data-driven decisions.

---

## 🔍 Project Summary

- **Objective:** Enable real-time visibility into call-centre performance metrics.  
- **Audience:** Operations managers, analysts, and customer service leads.  
- **Data Source:** CSV dataset — `Call Center_Call Center.csv`.  
- **Scope:** Covers calls across multiple channels, cities, and customer issues.

---

## 📊 Dashboard Overview

### 🏠 Home View
![Dashboard Overview](dashboard-overview.png)

### 📋 Grid / Detailed View
![Grid View](dashboard-grid-view.png)

---

## 🎯 Key Insights

| KPI | Description |
|------|--------------|
| **Total Calls:** 33K | Total number of customer calls received |
| **Total Call Duration (hrs):** 13.74K | Total call hours handled |
| **Total Call Duration (mins):** 824K | Total duration in minutes |
| **Average Call Duration:** 25.02 mins | Mean duration per call |
| **Response Time %:** 87.35% | Percentage of calls answered within SLA |
| **Top Reasons:** Billing Question, Payments, Service Outage |
| **Top Cities:** Los Angeles, Baltimore, Chicago, Denver |
| **Top Channels:** Call Centre, Chatbot, Email, Web |

---

## 🧭 Dashboard Pages

### **1️⃣ Home View**
- KPI cards: total calls, duration, average duration, SLA %
- Daily call trends  
- U.S. map visualization (Total Calls by State)  
- Tree map for “Total Calls by Reason”  
- Donut chart for channel distribution  
- Bar chart for sentiment analysis  
- Bar chart for calls by city  

### **2️⃣ Grid View**
- Row-level breakdown by ID, customer name, channel, state, reason, response time, city, and call duration.  
- Filters on **Date, Channel, City** for granular analysis.  

---

## 🛠️ Tools & Technologies

| Tool / Technology | Purpose |
|--------------------|----------|
| **Power BI Desktop** | Dashboard creation and data visualization |
| **Power Query** | Data extraction, cleaning, and transformation |
| **DAX (Data Analysis Expressions)** | Calculated metrics and KPIs |
| **CSV (Call Center_Call Center.csv)** | Primary data source |
| **Git & GitHub** | Version control and portfolio hosting |

---

## 🧮 Data Model Overview

- **Fact Table:** `Call Center_Call Center`  
- **Key Columns:**  
  - Call ID  
  - Customer Name  
  - Channel (Call-Centre, Web, Chatbot, Email)  
  - State, City  
  - Reason for Call  
  - Response Time (Within SLA / Above SLA / Below SLA)  
  - Call Duration (minutes)  
  - Sentiment  

---

### Sample DAX Measures
```DAX
Total Calls = COUNTROWS('Call Center_Call Center')
Average Call Duration = AVERAGE('Call Center_Call Center'[Call Duration (min)])
Response Within SLA % = 
    DIVIDE(
        CALCULATE(COUNTROWS('Call Center_Call Center'), 'Call Center_Call Center'[Response Time] = "Within SLA"),
        COUNTROWS('Call Center_Call Center')
    )


### 📂 Repository Structure

Call-Centre-KPI-PowerBI/
│
├── Call-Centre-KPI-Dashboard.pbix
├── Call Center_Call Center.csv
├── dashboard-overview.png
├── dashboard-grid-view.png
├── README.md
├── LICENSE
└── .gitignore

---
### 🚀 How to Use
	1. Clone or Download this repository:
		git clone https://github.com/kartikarora328/Call-Centre-KPI-PowerBI
	2. Open the file Call-Centre-KPI-Dashboard.pbix in Power BI Desktop.
	3. When prompted, connect to the CSV dataset:
		• Go to Transform Data → Data Source Settings → Change Source.
		• Select your local path for Call Center_Call Center.csv.
	4. Refresh the dataset and explore the visuals interactively.

---

### 📈 Skills Demonstrated
	• Power BI Dashboard Design & UX
	• Power Query ETL process
	• DAX measure creation
	• KPI tracking and SLA visualization
	• Sentiment and trend analysis
	• Data storytelling & insight generation
	• Git & GitHub portfolio management

---

### ⚙️ Future Enhancements
	• Add trend comparison across months or quarters
	• Integrate live API for real-time call logs
	• Create predictive metrics for call volume & SLA forecasting
	• Add drill-through detail pages by agent or city

---

### 👨‍💻 Author
**Harsh Arora**  
📧 [kartikarora328@gmail.com]  
🔗 [LinkedIn](https://www.linkedin.com/in/harsh-arora-80445167)

---

⭐ Acknowledgment
Dataset: Sample Call Centre Interaction Data
Special thanks to open data contributors for enabling analytics and visualization projects.

---

### 📜 License
This project is licensed under the MIT License.
See the LICENSE file for details.

---

### ✅ Metadata Summary
| Field | Details |
|--------|----------|
| **Project** | Call Centre KPI Dashboard - Power BI |
| **Author** | Harsh Arora |
| **Created** | November 2025 |
| **Tool** | Microsoft Power BI |
| **Category** | Data Visualization / Analytics |
| **License** | MIT |
| **Dataset Source** | Call Center_Call Center.csv |
| **Status** | Completed |
