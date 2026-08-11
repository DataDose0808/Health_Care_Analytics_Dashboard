# 🏥 Healthcare Analytics Dashboard

### Patient, Demographic, Hospital & Billing Insights | Excel • Power BI • DAX

> An end-to-end healthcare analytics project that transforms healthcare data into interactive dashboards and actionable insights across patient demographics, hospital activity, medical conditions, insurance providers, medications, and billing performance.

---

## 📊 Project Overview

Healthcare organizations generate large volumes of patient and operational data. Without effective analysis and visualization, it can be difficult to identify patterns in patient demographics, hospital activity, medical conditions, treatment, and healthcare billing.

This project was developed to explore healthcare data and build an interactive analytical solution that allows users to understand:

* 👥 Patient population and demographics
* 🏥 Hospital-level patient activity
* 🩺 Distribution of medical conditions
* 💳 Billing performance across insurance providers
* 💊 Medication and medical-condition patterns
* 📈 Patient and billing trends over time
* ⏱️ Average patient length of stay

The final solution combines data preparation, data modeling, DAX calculations, exploratory analysis, and interactive dashboard design in Power BI.

---

## 🎯 Business Objective

The primary objective of this project is to provide a centralized analytical view of healthcare activity that can support data-driven decision-making.

### Key business questions

#### Patient Analytics

* How many patients are represented in the dataset?
* How is the patient population distributed by gender?
* Which age groups contain the highest number of patients?
* How does patient volume change over time?

#### Hospital Analytics

* Which hospitals record the highest patient volumes?
* How are medical conditions distributed across hospitals?
* Are there noticeable differences in patient activity between hospitals?

#### Clinical Analytics

* Which medical conditions are most common?
* How are medical conditions distributed across demographic groups?
* What medications are associated with different medical conditions?

#### Financial Analytics

* What is the total billing amount?
* Which insurance providers account for the highest billing amounts?
* Which medical conditions generate the highest billing?
* How does billing performance change over time?

#### Operational Analytics

* What is the average patient length of stay?
* How does healthcare activity vary across different periods?

---

# 🛠️ Tools & Technologies

| Tool / Technology   | Purpose                                                |
| ------------------- | ------------------------------------------------------ |
| **Microsoft Excel** | Data preparation and initial analysis                  |
| **Power BI**        | Data modeling, visualization and dashboard development |
| **DAX**             | Measures, KPIs and analytical calculations             |
| **Power Query**     | Data transformation and preparation                    |
| **GitHub**          | Project documentation and portfolio presentation       |

---

# 🗂️ Project Structure

The Power BI solution is organized around a dimensional data model designed to support flexible analysis.

### Core tables

```text
Dim Patient
Dim Hospital
Dim Medication
Fact Hospital
DateTable
Dax Measures
```

Additional parameter tables are used to support interactive dashboard functionality and dynamic analysis.

### Data Model Concept

```text
                 ┌─────────────────┐
                 │   DateTable     │
                 └────────┬────────┘
                          │
                          │
┌─────────────────┐       │       ┌─────────────────┐
│   Dim Patient   │───────┼───────│  Fact Hospital  │
└────────┬────────┘       │       └────────┬────────┘
         │                │                │
         │                │                │
         ▼                │                ▼
┌─────────────────┐       │       ┌─────────────────┐
│ Dim Medication  │       │       │  Dim Hospital   │
└─────────────────┘       │       └─────────────────┘
                          │
                          ▼
                  ┌─────────────────┐
                  │  DAX Measures   │
                  └─────────────────┘
```

The model separates descriptive dimensions from analytical/fact data, allowing the dashboard to slice healthcare activity across multiple dimensions.

---

# 📊 Dashboard

The final Power BI report contains **three interactive analytical pages**.

---

## 1️⃣ Healthcare Overview

### Purpose

The **Healthcare Overview** page provides a high-level summary of healthcare activity and allows users to quickly understand the overall patient and hospital landscape.

### Key KPIs

The dashboard includes:

* 👥 **Patients**
* 💰 **Total Billing Amount**
* ⏱️ **Average Length of Stay**
* 🩺 **Most Common Condition**

The KPI cards also incorporate analytical measures such as year-over-year comparisons where applicable.

### Visual Analysis

The page includes:

* Patient distribution by gender
* Patient trends over time
* Patient volume by hospital
* Hospital vs. medical-condition analysis
* Dynamic date filtering
* Interactive analytical selectors

### Analytical Questions Answered

> How many patients are represented?

> Which hospitals handle the largest patient volumes?

> What is the most common medical condition?

> How is the patient population distributed by gender?

> How does patient activity change over time?

---

## 2️⃣ Healthcare Demographics

### Purpose

The **Healthcare Demographics** page focuses on understanding the characteristics and distribution of the patient population.

### Key Analysis

The dashboard analyzes:

* 👥 Patient age groups
* ⚥ Gender distribution
* 🗺️ Geographic distribution
* 🩺 Medical conditions
* 📊 Age group × gender relationships

### Visualizations

The page includes:

* Patient volume by age band
* Geographic patient distribution using a map
* Age-band and gender comparison
* Medical-condition filtering
* Interactive demographic selectors
* Date-based filtering

### Analytical Questions Answered

> Which age groups contain the most patients?

> How does gender distribution vary across age groups?

> Where are patients geographically distributed?

> How does the distribution change when filtering by medical condition?

---

## 3️⃣ Healthcare Insights

### Purpose

The **Healthcare Insights** page moves beyond patient demographics to explore financial and healthcare patterns.

### Key Analysis

The dashboard examines:

* 💳 Billing by insurance provider
* 🩺 Billing by medical condition
* 📈 Billing trends over time
* 💊 Medication by medical condition
* 👥 Patient volume across medication categories

### Visualizations

The page includes:

* Insurance-provider billing treemap
* Medical-condition billing analysis
* Billing trend over time
* Medical-condition × medication matrix
* Gender-based billing comparisons
* Interactive date filtering

### Analytical Questions Answered

> Which insurance providers account for the highest billing?

> Which medical conditions contribute most to billing?

> How does billing change over time?

> What medications are associated with different medical conditions?

> How does billing vary across patient demographics?

---

# 📐 DAX & Analytical Measures

DAX was used to create reusable measures that power the dashboard KPIs and visualizations.

Key measures implemented in the model include:

```text
Patients
Total Billing Amount
Avg Length of Stay
Most Common Condition
%YoY Patients
%YoY Billing
Selected Date Range
```

These measures allow the dashboard to dynamically respond to filters and provide consistent calculations across different visualizations.

### Example analytical logic

The dashboard uses measures rather than relying solely on static calculated values, allowing users to interact with:

* Year
* Month
* Quarter
* Medical condition
* Gender
* Hospital
* Age band
* Insurance provider
* Medication

This makes the report an interactive analytical tool rather than a static collection of charts.

---

# 🎛️ Interactive Dashboard Features

The report was designed with interactivity in mind.

Users can dynamically explore the data using:

* 📅 Year filters
* 📅 Month filters
* 📅 Date/period selection
* 🩺 Medical-condition filters
* 🔎 Dynamic field/parameter selectors
* 🏥 Hospital analysis
* 👥 Demographic segmentation

The dashboard also uses navigation/action controls to improve the overall user experience.

---

# 🔍 Analytical Approach

The project followed an end-to-end analytics workflow.

```text
Raw Healthcare Data
        ↓
Data Preparation
        ↓
Data Cleaning & Transformation
        ↓
Data Modeling
        ↓
DAX Measure Development
        ↓
Exploratory Data Analysis
        ↓
Dashboard Development
        ↓
Insight Generation
        ↓
Business Recommendations
```

---

# 📈 Key Analytical Areas

## Patient Demographics

The analysis examines the patient population across:

* Age bands
* Gender
* Medical conditions
* Geographic location

This provides a clearer understanding of the population being served.

---

## Hospital Performance

Hospital-level analysis allows users to compare patient volumes across healthcare facilities and examine how medical conditions are distributed between hospitals.

This can support:

* Capacity planning
* Resource allocation
* Hospital performance monitoring
* Identification of high-volume facilities

---

## Medical Conditions

Medical conditions are analyzed from both patient-volume and financial perspectives.

This creates an opportunity to compare:

> **How frequently does a condition occur?**

against

> **How much billing is associated with the condition?**

This distinction is important because the most common condition is not necessarily the condition generating the highest billing.

---

## Insurance & Billing

Insurance providers are analyzed based on billing amounts to provide visibility into the financial side of healthcare activity.

The dashboard enables users to compare billing across:

* Insurance providers
* Medical conditions
* Time periods
* Patient demographics

---

## Medication Analysis

Medication patterns are explored alongside medical conditions.

This helps identify relationships between:

* Medical conditions
* Medications
* Patient volumes

The analysis provides another perspective on healthcare utilization.

---

# 💡 Business Value

The dashboard can support healthcare stakeholders by providing a centralized view of patient and financial activity.

Potential applications include:

### 🏥 Healthcare Management

Monitoring patient volumes and hospital activity to support operational planning.

### 📊 Resource Planning

Using demographic and hospital patterns to support allocation of healthcare resources.

### 💰 Financial Monitoring

Tracking billing patterns across insurance providers and medical conditions.

### 🩺 Clinical Planning

Understanding the prevalence of medical conditions and associated medication patterns.

### 📈 Trend Monitoring

Tracking changes in patient volumes and billing over time.

---

# 🚀 Business Recommendations

Based on the analytical framework developed in this project, healthcare organizations can consider:

### 1. Optimize Resource Allocation

Use hospital and demographic patient-volume patterns to better align healthcare resources with areas of higher demand.

### 2. Monitor High-Impact Medical Conditions

Track conditions with significant patient volumes and/or billing impact to understand their operational and financial implications.

### 3. Strengthen Financial Monitoring

Use insurance-provider and medical-condition billing analysis to improve financial visibility and identify unusual changes in billing patterns.

### 4. Support Targeted Healthcare Planning

Demographic insights can help organizations design services and interventions around the needs of different patient groups.

### 5. Monitor Trends Continuously

Regularly tracking patient and billing trends can help healthcare managers identify changes early and respond appropriately.

---

# 📸 Dashboard Preview

The repository will contain screenshots of the three major dashboard pages.


# 📁 Repository Contents

```text
healthcare-analytics-dashboard/
│
├── README.md
│
├── dashboard/
│   └── Healthcare_Analysis.pbix
│
├── data/
│   ├── raw/
│   │   └── healthcare_dataset.xlsx
│   │
│   └── processed/
│       └── README.md
│
├── screenshots/
│   ├── healthcare-overview.png
│   ├── healthcare-demographics.png
│   └── healthcare-insights.png
│
├── documentation/
│   ├── data-dictionary.md
│   ├── methodology.md
│   ├── key-insights.md
│   └── recommendations.md
│
├── dax/
│   └── measures.md
│
└── LICENSE
```

---

# 🎓 Skills Demonstrated

This project demonstrates practical experience in:

### Data Analysis

* Data cleaning
* Exploratory data analysis
* Descriptive analytics
* Trend analysis
* Demographic analysis
* Financial analysis

### Power BI

* Data modeling
* Interactive dashboard development
* KPI cards
* Slicers
* Drill/filter interactions
* Maps
* Treemaps
* Matrix/pivot analysis
* Trend visualizations
* Dashboard navigation

### DAX

* Measure creation
* KPI calculations
* Aggregations
* Time-based analysis
* Year-over-year analysis
* Dynamic calculations

### Data Storytelling

* KPI-driven dashboard design
* Analytical question development
* Insight generation
* Business recommendations
* User-focused visualization

---

# 📌 Project Highlights

| Area               | Implementation                                |
| ------------------ | --------------------------------------------- |
| Patient Analysis   | Age, gender, condition and patient trends     |
| Hospital Analysis  | Hospital-level patient volume                 |
| Demographics       | Age bands, gender and geographic distribution |
| Clinical Analysis  | Medical-condition and medication analysis     |
| Financial Analysis | Billing and insurance-provider analysis       |
| Time Analysis      | Monthly, quarterly and yearly trends          |
| Data Modeling      | Dimension and fact-based model                |
| DAX                | Reusable analytical measures                  |
| Visualization      | Interactive Power BI dashboards               |
| Reporting          | Three-page analytical report                  |

---

# 🧠 Key Learning Outcomes

This project strengthened practical skills in:

* Turning raw healthcare data into a structured analytical model
* Designing dashboards around business questions
* Creating reusable DAX measures
* Building interactive Power BI reports
* Combining demographic, operational and financial analysis
* Presenting complex data in a simple and decision-friendly format
* Translating analytical findings into business recommendations

---

# 🔮 Future Improvements

Future versions of this project could expand the analysis by introducing:

* Patient readmission analysis
* Length-of-stay analysis by medical condition
* Hospital benchmarking
* Cost-per-patient analysis
* Insurance claim analysis
* Patient outcome analysis
* Predictive patient-volume forecasting
* Advanced statistical analysis
* Automated data refresh
* Role-based dashboard access

---

# ⚠️ Data Disclaimer

This project is intended for **educational, portfolio and analytical demonstration purposes**.

The dashboard should not be used to make clinical diagnoses, determine individual patient treatment, or make medical decisions.

Any healthcare-related recommendations presented in this project are analytical observations and should be interpreted within the appropriate professional and organizational context.



### Core Tools

`Excel` • `Power BI` • `DAX` • `SQL` • `PostgreSQL` • `Data Visualization`

I enjoy working on analytical projects that combine technical data skills with clear business storytelling.



## 📬 Let's Connect

Interested in discussing this project, data analytics, Power BI, or potential collaboration?

Feel free to explore the repository and connect with me.

---

### ⭐ If you find this project useful, consider giving the repository a star.
