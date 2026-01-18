# Engine Performance Analysis & Fault Detection

## Project Overview
This project focuses on **engine performance monitoring** and **fault detection** using data-driven analytics. It demonstrates how exploratory data analysis (EDA), statistical insights, and visualization can transform raw engine sensor data into actionable knowledge that supports predictive maintenance, operational optimization, and risk reduction.

Key Objectives:
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
#### Statistical Summary Highlights
- Temperature values centered around ~90°C with higher extremes indicating potential overheating
- RPM values ranged widely, reflecting varying operational loads
- Fuel efficiency showed moderate variability
- Torque and Power Output reflected expected engine performance behavior
---
### Analytical Techniques
#### Correlation Analysis
- Calculated correlation coefficients between numerical variables
- Visualized relationships using a correlation heatmap
  
**Key Insight:**
- No strong linear correlation observed between individual features and Fault_Condition
- Torque and Power Output showed a weak positive relationship, consistent with physical expectations
- Results suggest fault conditions depend on multi-factor or non-linear interactions
  
#### Univariate Analysis

**Numerical Features**
- Histograms plotted for:
- Temperature (°C)
- RPM
- Fuel Efficiency
- Torque
- Power Output (kW)
Used 14 bins and a grey color palette for visual consistency

**Categorical Features**
Count plots for:
 - Fault_Condition
 - Operational_Mode

#### Outlier Detection
- Boxplots created for all major numerical variables
- Distributions were largely symmetrical with no significant outliers detected

#### Bivariate Analysis
- Torque vs Power Output: Scatter plots showed no strong linear dependency
- Temperature vs Fault Condition: Examined trends in fault occurrence

**Conclusion:**

Findings reinforce the heatmap insight that faults are not driven by single variables

#### Fault Condition by Operational Mode
Boxplots used to analyze fault variability across:
 - Idle
 - Cruising
 - Heavy Load

**Key Findings:**
- Cruising mode showed the lowest variability (most stable)
- Idle and Heavy Load modes exhibited higher fault variability

#### Categorical Interaction Analysis
Count plots with hue = Fault_Condition used to compare operational modes
Observations:
- Fault Condition 2 was the most frequent across modes, especially during Cruising
- Fault Condition 3 occurred least frequently, particularly under Heavy Load

#### Pivot Table Analysis
- Created pivot tables summarizing fault counts grouped by operational mode
- Visualized results using grouped bar charts

**Insights:**
- Idle mode showed the highest occurrence of Fault Condition 0
- Cruising mode dominated by Fault Condition 2
- Heavy Load mode exhibited fewer extreme faults
---
## Analytical Poster Overview
This project includes a research-style analytical poster summarizing the full EDA and insights in a concise visual format.
### Poster Highlights:
- Problem Statement and business context
- Dataset overview and structure
- Correlation heatmap interpretation
- Fault condition behavior across operational modes
- Fault frequency comparison
- Limitations and future recommendations

## Interactive Dashboard
An interactive Tableau dashboard was created to enable intuitive exploration of engine KPIs and fault behavior.
### Dashboard Features:
- Dynamic filtering by Operational Mode and Fault Condition
- Visualization of engine performance metrics
- Fault distribution monitoring for decision support
 (Dashboard link will be added after upload to Tableau Public)
--- 
## Tools & Technologies
- **Programming:** Python (`pandas`, `numpy`, `matplotlib`, `seaborn`)
- **Visualization:** Tableau (Interactive Dashboard)
- **IDE:** Jupyter Notebook / Google Colab
   **Dashboard:** [View on Tableau Public](https://public.tableau.com/views/engine_faliure_dashboard/Dashboard1?:language=en-US&:sid=&:redirect=auth&showOnboarding=true&:display_count=n&:origin=viz_share_link)
---
## Results & Insights
The analysis provided valuable insights into the key factors affecting **engine efficiency, reliability, and fault conditions**.
- Engine faults show mode-dependent behavior, not single-variable causation
- Cruising mode is the most stable operational state
- Idle and Heavy Load modes require closer monitoring due to higher variability
- Visualization techniques (heatmaps, boxplots, dashboards) significantly improved interpretability
---
**Project Impact**
- Supports predictive maintenance planning
- Enables targeted operational strategies
- Enhances engine reliability and safety

Overall, this project sets the stage for:
- Optimizing **fuel efficiency**
- Improving **fault detection**
- Enhancing **engine reliability**
---
## Challenges & Limitations
-Dataset may not capture all influencing factors (e.g., environmental conditions)
-Limited sample size may affect generalizability
-Requires further validation with real-world data

---
## Author
**Author:** Jameela Al-Smadi
**Contact:** [jameelasmadi98@gmail.com](mailto:jameelasmadi98@gmail.com)
**LinkedIn:** [https://www.linkedin.com/in/jameela-smadi/]

---
