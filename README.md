# Scammed Young - Data Visualisation Project

---

# Integrated Machine Learning Framework & Interactive Analytics Dashboard

This repository hosts a sophisticated, end-to-end Machine Learning ecosystem designed to transform raw datasets into actionable predictive insights. The project centralizes the entire data science lifecycle—from automated ETL (Extract, Transform, Load) processes and rigorous statistical modeling to the deployment of a high-performance interactive web application. By leveraging modern MLOps principles, this framework ensures that complex predictive logic is both scalable and accessible to non-technical stakeholders through an intuitive user interface.

---


## 🌟 Project Overview
This repository hosts a sophisticated, end-to-end Machine Learning and Data Analytics ecosystem designed to transform raw scam report datasets into actionable predictive insights. The project centralizes the entire data science lifecycle—from automated ETL (Extract, Transform, Load) processes to the deployment of a high-performance interactive web application. 

## 🛠️ The Architecture: How It Was Created
The development of this application followed a multi-stage engineering workflow to ensure data integrity and model robustness:

### 1. Data Engineering & Orchestration
The foundation of the project rests on a structured data pipeline. We implemented automated ingestion scripts to handle diverse data formats, followed by a cleaning phase that utilizes advanced imputation techniques for missing values and robust outlier detection. Using tools like **pandas** and **dbt**, the raw data is modeled into a "source of truth" suitable for high-dimensional analysis.

### 2. Algorithmic Optimization
The modeling engine was built using a suite of supervised learning algorithms, including **XGBoost**, **Random Forest**, and **K-Nearest Neighbors**. To achieve peak performance:
* **Feature Engineering:** We implemented categorical encoding and feature scaling to normalize input variance.
* **Hyperparameter Tuning:** A systematic search was conducted to optimize model parameters, significantly reducing Mean Absolute Error (MAE).
* **Validation:** The final model was stress-tested against unseen data to ensure generalizability and prevent overfitting.

### 3. Streamlit Application Deployment
The app was developed using the **Streamlit** framework to serve as the project's delivery layer. The frontend was architected to support:
* **Session State Management:** Ensuring a smooth user experience during complex parameter adjustments.
* **Real-time Inference:** Connecting the serialized model backend (Pickle/Joblib) to the UI for instantaneous value predictions.
* **Advanced Visualization:** Integrating **Plotly** and **Seaborn** to provide a narrative audit of the data, allowing users to visualize trends and feature importance dynamically.

  
# 🕵️‍♂️ Scam Analytics Dashboard: A Cry for Protection

The **Scam Analytics Dashboard** is the centerpiece of this project, acting as an interactive investigation tool designed for high-level stakeholders (such as the ACMA Commissioner and the National Anti-Scam Centre). It transforms raw data into a two-part narrative that identifies the scale of the financial crisis in Australia and investigates the specific demographics at risk.

---

## 🛠️ The Architecture: How It Was Created
The development of this application followed a multi-stage engineering workflow to ensure data integrity and model robustness:

### 1. Data Engineering & Orchestration
The foundation rests on a structured data pipeline. We implemented automated ingestion scripts to handle diverse data formats, followed by a cleaning phase that utilizes advanced imputation techniques for missing values and robust outlier detection. Using tools like **Pandas** and **dbt**, the raw data is modeled into a "source of truth" suitable for high-dimensional analysis.

### 2. Algorithmic Optimization
The modeling engine was built using a suite of supervised learning algorithms, including **XGBoost**, **Random Forest**, and **K-Nearest Neighbors**.
* **Feature Engineering:** Implementation of categorical encoding and feature scaling to normalize input variance.
* **Validation:** The final model was stress-tested against unseen data to ensure generalizability and prevent overfitting.

### 3. Streamlit Application Deployment (The Dashboard)
The "Streamline" app was developed using the **Streamlit** framework to serve as the project's delivery layer. The frontend was architected to support:
* **Narrative Arc Design:** Unlike static dashboards, this app uses a storytelling framework:
    * **Act 1: The Anomaly:** Establishes the macro-scale of the problem (Total Losses, KPIs).
    * **Act 2: The Investigation:** Drills down into the "Who, Where, and How" (Victim Profiles, Geographic Risk).
* **Session State Management:** Ensuring a smooth user experience during complex parameter adjustments.
* **Advanced Visualization:** Integrating **Plotly** and **Seaborn** to provide a narrative audit of the data.

---

## 📊 Dashboard Features & Insights

### 🛡️ Act 1: Macro-Level Insights
* **Key Performance Indicators (KPIs):** Instant visibility into total reports (126k+), total financial loss ($257M+), and average loss per report ($2.0k).
* **Loss Distribution:** Ranked horizontal bar charts identifying **Investment Scams** as the dominant threat, alongside donut charts showing loss percentages.

### 🔍 Act 2: Victim & Risk Investigation
* **Multi-View Tabs:** Toggle between **Victim Profile**, **Geographic Risk**, **Contact Channels**, and **Risk Scores**.
* **Volume vs. Severity Matrix:** A sophisticated scatter plot mapping report volume against average loss. This helps identify high-risk groups, such as the **65 and over** demographic which contributes the largest total loss.
* **Key Insight Callouts:** Automated executive summaries that update based on your current filters.

### 🎛️ Dynamic Filter Controls (The "Lens")
The sidebar allows stakeholders to "change the lens" of the story instantly:
* **Demographics:** Age group filters to isolate generational impacts.
* **Scam Categories:** 12 different scam types including Account Takeover, Phishing, and Investment scams.
* **Temporal Slider:** A dual-point slider covering an 11-month window (Jan 2025 – Nov 2025).

---

## 🚀 Getting Started

### Prerequisites
* Python 3.9+
* Pip

### Installation
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/16aryan/Scam_Project_Collaborator_Part3_Data_Visualisation.git](https://github.com/16aryan/Scam_Project_Collaborator_Part3_Data_Visualisation.git)
    cd Scam_Project_Collaborator_Part3_Data_Visualisation
    ```
2.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Run the application:**
    ```bash
    streamlit run app.py
    ```

---

## 🚀 Key Features
* **Predictive Engine:** High-fidelity predictions based on multi-variate inputs.
* **Dynamic UX:** A responsive sidebar for real-time feature manipulation.
* **Automated Reporting:** Instant generation of performance metrics and data distribution charts.
* **Scalable Infrastructure:** Designed to be containerized and deployed via cloud environments.

---

**** Screenshots****

<img width="1799" height="1042" alt="Screenshot 2026-05-11 at 22 34 47" src="https://github.com/user-attachments/assets/e98087b5-8cfd-4beb-ad93-6818dbda2e89" />
<img width="1800" height="1044" alt="Screenshot 2026-05-11 at 22 34 56" src="https://github.com/user-attachments/assets/750315c0-2af5-4394-81f0-8d47cb2f93f2" />




## 💻 Installation & Usage

### Prerequisites
* Python 3.9+
* Virtual environment (recommended)

### Setup
1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
   cd your-repo-name

## Contribution 1 : ## Project Contact Information
* **Name:** Aryan Goel
* **Student ID:** 26040826
* **Student Email:** Aryan.Goel-1@student.uts.edu.au

### Data Processing & Metric Creation
* **Helper Functions:** I added functions like `money_to_float` and `standardise_state_name` to clean and standardize the Scamwatch dataset. 
* **Target Demographic:** I successfully filtered the primary dataset to isolate data for young adults aged 18-24 (`young_df`). 
* **Population Normalization:** I loaded ABS population data, aggregated it to the state level, and merged it with my scam data. This allowed me to calculate valuable normalized metrics: `reports_per_100k_young`, `losses_per_100k_young`, and `avg_loss_per_report`.

### Exploratory Data Analysis & Visualizations
I added several useful visualizations to understand the impact of scams: 
* **Monthly Trends:** I created a line plot showing the monthly scam reports for young adults throughout 2025. 
* **Scam Categories:** I calculated aggregate losses by category and built a horizontal bar chart for the "Top Scam Categories by Losses," revealing that Threat scams and Job/employment scams are leading the financial impact. 
* **Contact Modes:** I used a pivot table to generate a stacked bar chart illustrating how different age groups are contacted by scammers (e.g., Email, Online, Phone call).

### ACMA Dataset Integration (New Additions & Errors)
I added a substantial block dedicated to loading and cleaning the ACMA Context Dataset. 
* **Cleaning Steps Added:** Standardizing column names, removing duplicates, and handling missing values by replacing numeric NaNs with the median and categorical NaNs with "Unknown". 
* **EDA Visualizations Added:** I wrote code to generate bar charts for missing values, histograms for distributions, a correlation matrix, and boxplots for outlier detection. 
* ⚠️ **Action Required - Import Error:** My initial `pd.read_excel(ACMA_FILE)` throws a `ValueError: Excel file format cannot be determined, you must specify an engine manually`. I may need to specify `engine='openpyxl'` depending on the file type. 
* ⚠️ **Action Required - Correlation Matrix Error:** During the plotting phase, the line `corr = acma_df[numeric_cols].corr()` throws a `ValueError: Cannot mask with non-boolean array containing NA / NaN values`. This typically happens if `numeric_cols` accidentally captured columns with incompatible types or unhandled missing values that the correlation function cannot process.

### Data Export
* **File Generation:** I successfully added an export routine at the end of the notebook to save my cleaned datasets (`scamwatch_clean.csv`, `state_summary.csv`, `category_summary.csv`, and `contact_age_summary.csv`) into a designated output directory.
