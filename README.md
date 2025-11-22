# Engine Performance Analysis & Fault Detection

## Project Overview
This project addresses the challenge of **engine performance monitoring** and **fault detection** through data-driven analysis.
The primary objectives are to:
- Reduce downtime through **early fault detection**
- Optimize **maintenance schedules** using predictive analytics
- Enhance **safety and operational efficiency** by identifying key fault indicators

---
## Dataset Information
**File name:** `engine_failure_dataset.csv`
**Size:** 146 KB
**Shape:** 1001 Rows × 11 Columns
**Source:** [Kaggle Dataset – Engine Failure Detection](https://www.kaggle.com/datasets/ziya07/engine-failure-detection-dataset)

### Dataset Description
The dataset simulates sensor readings from various types of engines to detect failures in mechanical systems, especially in automotive applications.
It captures data on **engine performance, fault conditions, and operational modes** over time.

**Columns include:**
- `Time_Stamp`
- `Temperature (°C)`
- `RPM` (Revolutions per Minute)
- `Fuel_Efficiency (km/liter)`
- `Vibration_X`, `Vibration_Y`, `Vibration_Z`
- `Torque (Nm)`
- `Power_Output (kW)`
- `Fault_Condition`
- `Operational_Mode`

---
## Data Analysis & Computation

### 1) Data Cleaning
- No missing values or duplicate rows were found in the dataset.

### 2) Exploratory Data Analysis (EDA)

#### Reading Data & Overview
- Imported required libraries (`pandas`, `numpy`, `matplotlib`, `seaborn`)
- Checked dataset structure, column types, and non-null values
- Generated **descriptive statistics** for numerical columns
- Calculated **correlation coefficients** and visualized using a **heatmap**

#### Univariate Analysis
- **Numerical Features:** Plotted histograms for Temperature (°C), RPM, Fuel Efficiency, Torque, and Power Output (kW)
  (Used 14 bins and grey color scheme for consistency)
- **Categorical Features:** Used count plots to visualize the frequency of `Fault_Condition` and `Operational_Mode`

####  Outlier Detection
- Created boxplots for Temperature, RPM, Fuel Efficiency, Torque, and Power Output to identify potential outliers.
####  Bi-variate Analysis
- **Torque vs Power Output:** Analyzed linear relationships using scatter plots.
- **Temperature vs Fault Condition:** Observed trends in fault occurrence related to temperature.
- **Fault Condition by Operational Mode:** Boxplots revealed how fault distribution varies across modes.
- **Categorical Interaction:** Used count-plot with `hue='Fault_Condition'` to compare operational modes by fault status.

####  Pivot Table Analysis
- Created a pivot table summarizing the count of `Fault_Condition` grouped by `Operational_Mode`
- Visualized results using a **grouped bar chart** to show fault counts per mode.

---

## Tools & Technologies
- **Programming:** Python (`pandas`, `numpy`, `matplotlib`, `seaborn`)
- **Visualization:** Tableau (Interactive Dashboard)
- **IDE:** Jupyter Notebook / Google Colab
   **Dashboard:** [View on Tableau Public](https://public.tableau.com/views/engine_faliure_dashboard/Dashboard1?:language=en-US&:sid=&:redirect=auth&showOnboarding=true&:display_count=n&:origin=viz_share_link)

## Results & Insights
The analysis provided valuable insights into the key factors affecting **engine efficiency, reliability, and fault conditions**.

- **Correlation Analysis:** Strong positive correlation between **Torque** and **Power Output**, confirming that higher torque increases power generation.
- **Distribution Analysis:** Identified variations, skewness, and outliers in engine parameters.
- **Fault Condition Analysis:** Faults vary significantly across **Operational Modes** (Idle, Cruising, Heavy Load), guiding targeted maintenance strategies.
- **Boxplots & Heatmaps:** provided a clearer understanding of fault distributions and variable interdependencies, helping in predictive maintenance planning.
- **Dashboard Overview:** Simplified real-time exploration of KPIs, helping stakeholders monitor engine performance effectively.

---
Overall, this project sets the stage for:
- Optimizing **fuel efficiency**
- Improving **fault detection**
- Enhancing **engine reliability**
---
## Challenges & Limitations
-Dataset may not capture all influencing factors (e.g., environmental conditions)
-Limited sample size may affect generalizability
-Requires further validation with real-world data

## Author
**Author:** Jameela Al-Smadi
**Contact:** [jameelasmadi98@gmail.com](mailto:jameelasmadi98@gmail.com)
**LinkedIn:** [https://www.linkedin.com/in/jameela-smadi/]

---

### Summary
This project demonstrates how **data analytics and visualization** can transform raw sensor data into actionable insights — driving smarter maintenance and higher engine performance.
