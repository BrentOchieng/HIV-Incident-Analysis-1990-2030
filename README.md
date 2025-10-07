#  HIV Incidence Analysis in Kenya (1990–2022) and Prediction (2023-2030)

##  Project Overview  
This project explores **HIV incidence trends across Kenyan provinces** from **1990 to 2022**, providing insights into how the epidemic has evolved geographically and temporally.  
Through **data wrangling, exploratory analysis, visualization, feature engineering**, and **forecasting with Prophet**, this analysis identifies key regional differences and predicts possible future HIV incidence trends up to **2030**.

---

##  Objectives  
1. Analyze the **yearly and decadal HIV incidence trends** across all Kenyan provinces.  
2. Identify **provinces with the highest and lowest HIV incidence** over time.  
3. Measure **percentage change and improvement rates** to determine which province improved the fastest.  
4. Group provinces into **regional clusters** (Central, Coastal, Rift, Western, Arid, Urban) to observe aggregated patterns.  
5. Use **Prophet time-series forecasting** to predict HIV incidence up to 2030 for each province.  
6. Create clear and interpretable **visuals and forecasts** that can be viewed directly on GitHub.

---

##  Data Preparation  
The dataset contains yearly HIV incidence rates per 1,000 people across eight provinces:
- Central  
- Coast  
- Eastern  
- Nairobi  
- North Eastern  
- Nyanza  
- Rift Valley  
- Western  

### Key Steps:
- Cleaned and standardized column names.  
- Ensured the `year` column was correctly typed as an integer.  
- Reshaped the dataset using **`pandas.melt()`** for easier plotting and multi-variable comparisons.  
- Created additional engineered features:
  - **Decade grouping** to study 10-year averages.
  - **Year-over-year percentage change** to assess rate improvements.
  - **Regional mapping** (e.g., Urban, Rift, Coastal, Western, Central, Arid).

---

##  Exploratory Data Analysis (EDA)

### 1. Provincial Trends  
Each province’s HIV incidence was visualized over time using **Seaborn line plots**.  
- **Nyanza** consistently recorded the highest incidence levels throughout most of the study period.  
- **North Eastern** showed the lowest incidence, remaining below 1 per 1,000 people.  
- **Central and Nairobi** exhibited significant downward trends after the early 2000s.

### 2. Decadal Distribution  
Grouped data by decade (1990s, 2000s, 2010s, 2020s) to show long-term averages per province.  
- The **2000s decade** marked the peak of HIV incidence in most regions.  
- Steady declines are observed in the 2010s and 2020s, reflecting improved health interventions.

### 3. Regional Grouping  
Mapped provinces into broader regional clusters and visualized mean incidence per region:
- **Western region (Nyanza + Western)** reported the highest cumulative incidence.  
- **Arid and Urban regions** (North Eastern, Nairobi) recorded the lowest averages.

### 4. Percentage Change Analysis  
Calculated **year-over-year percentage change** for each province to determine improvement rates.  
- **Central Province** showed one of the steepest declines in percentage terms, indicating strong health campaign outcomes.  
- Some provinces exhibited fluctuations tied to local outbreaks or reporting inconsistencies.

---

##  Predictive Modeling (Prophet Forecasting)

Used **Meta’s Prophet** library to forecast HIV incidence up to **2030** for each province.

### Model Steps:
1. Converted each province’s data into Prophet-compatible format (`ds` = year, `y` = incidence).  
2. Fitted an individual Prophet model per province.  
3. Generated yearly forecasts (2023–2030) with upper and lower confidence intervals.  


### Forecast Insights:
- **General national trend:** Continued decline in HIV incidence through 2030.  
- **High-risk provinces** (e.g., Nyanza and Western) remain above the national mean but show improvement.  
- **Low-risk provinces** (e.g., North Eastern, Central) likely to stabilize near minimal incidence levels.

---

##  Geographic and Distribution Visuals
- **Pie chart:** Shows average HIV incidence distribution across provinces (1990–2022).
  <img width="886" height="658" alt="image" src="https://github.com/user-attachments/assets/8e0d1561-90db-4078-b398-dab26ad3f8f9" />

- **Decade-based bar chart:** Compares provincial HIV incidence across decades.
  <img width="1384" height="584" alt="image" src="https://github.com/user-attachments/assets/2be667ee-ed76-453e-9ce5-796e9c27f32b" />


- **Facet grid plots:** Visualize individual province trends side by side.
  <img width="1384" height="713" alt="image" src="https://github.com/user-attachments/assets/b18984d1-0e00-4929-82cd-60ff93d29cd5" />

- **Forecast visuals:** Combine predicted incidence trends with confidence bands.
  <img width="1384" height="584" alt="image" src="https://github.com/user-attachments/assets/29ffb265-6f6b-416a-a1de-db2dca2125cb" />


---

##  Key Insights
- HIV incidence in Kenya **peaked in the early 2000s** and has **declined steadily since 2010**.  
- **Nyanza Province** remains the most affected region historically and in projections.  
- **Central and Nairobi** show the **fastest improvement rates**.  
- Forecasting suggests a **national downward trend** continuing toward 2030, driven by public health interventions, awareness, and treatment programs.  

---

## Tools & Technologies
- **Python Libraries:** `pandas`, `numpy`, `matplotlib`, `seaborn`, `prophet`  
- **Visualization Tools:** Matplotlib, Seaborn,  
- **Environment:** Jupyter Notebook  
- **File Outputs:** PDF and PNG charts for visualization sharing  

---

## Project Structure
HIV_Incidence_Analysis/
│
├── data/
│   └── hiv_incidence_1990_2022.csv
│
├── notebooks/
│   └── HIV_Incidence_analysis_1990_2022.ipynb
│
├── visuals/
│   ├── provincial_trends.pdf
│   ├── regional_decade_distribution.pdf
│   └── prophet_forecasts.pdf
│
├── requirements.txt
└── README.md


