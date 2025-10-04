# 🏥 Hospital Management Dashboard (Power BI + SQL)

**A complete analytics dashboard for hospital operations**  
Visualize patient demographics, billing, doctor performance, and key metrics, built with Power BI and powered by SQL data transformation.

---

## 📄 Table of Contents

1. [Overview](#overview)  
2. [Key Metrics & Visuals](#key-metrics--visuals)  
3. [Data Flow & SQL Transformations](#data-flow--sql-transformations)  
4. [Getting Started / How to Run](#getting-started--how-to-run)  
5. [Folder Structure](#folder-structure)  
6. [Screenshots / Preview](#screenshots--preview)  
7. [Future Enhancements](#future-enhancements)  
8. [License & Usage](#license--usage)  
9. [Credits / Acknowledgements](#credits--acknowledgements)  

---

<img width="884" height="494" alt="Hospital Management Dashboard" src="https://github.com/user-attachments/assets/7760793c-7094-48e7-8db5-d14bfa11f171" />

## 🔍 Overview

This project is a **Hospital Management Dashboard** built using **Power BI Desktop**, with data extracted and cleaned via **SQL scripts**. It provides stakeholders (hospital admins, analysts) with insights into patient statistics, financials, doctor distribution, and geographic / treatment trends in a user‑friendly, interactive format.

**Objectives:**

- Monitor hospital performance through KPIs  
- Enable interactive filtering and slicing by doctor, treatment, location  
- Expose trends in disease, billing, and pending payments  
- Demonstrate a complete data pipeline: SQL → cleaned data → Power BI model → visual dashboard  

---

## 📊 Key Metrics & Visuals

### 🔢 KPIs / Measures  
- **Total Patients**  
- **Average Patient Age**  
- **Total Doctors**  
- **Total Amount Billed**  
- **Amount Paid**  
- **Amount Pending**

### 📈 Core Visualizations  
- **Doctors by Specialization** → Column chart  
- **Total Bill by Payment Mode** → Donut / Pie chart  
- **Diseases over Time / by patient counts** → Line chart  
- **Amount Pending by State** → Map or bar chart  
- **Total Received / Flow of Payments** → Ribbon / Flow / Sankey chart  
- **Slicers / Filters** for:  
  • Treatment Type  
  • Doctor Name  
  • State  
  • City  

These visuals let users drill down and analyze by different dimensions (doctor, location, treatment, etc.).

---

## 🛠 Data Flow & SQL Transformations

### 📦 Data Source & Extraction  
You likely have tables like: `Patients`, `Doctors`, `Treatments`, `Billing`, `Payments`.  
Use `extract_tables.sql` to pull relevant columns and join basic relations.

### 🧹 Cleaning & Transformations  
In `clean_data.sql` (or similar), perform:

- Null / missing value handling  
- Date formatting, converting to consistent types  
- Joins between tables (e.g. patients → treatments → billing)  
- Deriving new fields (e.g. `Age = YEAR(CURRENT_DATE) – YEAR(DateOfBirth)`)  
- Aggregations (sum of billing, payment statuses)  
- Logic to compute pending amounts (e.g. `Pending = Billed – Paid`)  

### 🔄 Workflow  
1. Run the extraction script  
2. Run the cleaning / transformation script  
3. Export or push final table(s) (CSV, database view)  
4. Connect Power BI to the cleaned dataset  
5. Build the data model, define DAX measures  
6. Create visuals, embed interactions, publish (if desired)  

Showing a diagram in the README (data pipeline: source → SQL → cleaned → Power BI → Dashboard) helps readers understand at a glance.

---

## 🚀 Getting Started / How to Run

Here’s how someone else (or future you) can run or review your dashboard:

1. **Clone this repository**  
   ```bash
   git clone https://github.com/harshitrai88/hospital_Management.git
   cd hospital_Management
