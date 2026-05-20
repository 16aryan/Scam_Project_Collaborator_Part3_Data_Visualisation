# Scammed Young - Data Visualisation Project

## Project Contact Information
* **Name:** Aryan Goel
* **Student ID:** 26040826
* **Student Email:** Aryan.Goel-1@student.uts.edu.au

---

## Contribution 1

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


## Interactive Dashboard

---

### Key Features
#### Interactive Multi-Dimensional Filtering System
* Dynamic filtering by State/Territory, Age Group, Scam Type, and Date Range
* Real-time synchronization across all visualizations and metrics
* One-click filter reset for intuitive, non-technical user experience

#### Core KPI Dashboard & Metrics Visualization
* Displays total reports, total financial loss, average loss per report, and time span
* Includes contextual metrics: loss per minute, average interval between reports
* Clearly distinguishes full dataset, Australia-only data, and filtered dataset

#### Advanced Interactive Data Visualizations
* Monthly loss trend chart with 3-month linear forecasting
* Top scam type analysis (bar chart + pie chart)
* Victim profile analysis: report count vs. average loss by age group
* Geographic risk mapping: state-level hazard score and loss distribution
* Risk bubble matrix for identifying high-risk victim segments

#### Composite State Hazard Score
* Custom risk algorithm: Total Loss (40%) + Loss Per Capita (25%) + Avg Loss Per Report (20%) + Total Reports (15%)
* Standardized score (0–100) for ranking regional scam risks
* Supports priority-based decision-making for policymakers

#### Automated Data Preprocessing & Cleaning
* Automated formatting for currency, dates, and state names
* Integration with ABS population data for per-capita loss calculation
* Filtering of overseas records to focus on domestic scam analysis
* Data caching for high-performance page loading

#### Data Export & Insight Presentation
* Export filtered dataset to CSV for external analysis
* Highlighted insight cards (pull quotes) for key findings
* State-specific narrative analysis and risk summaries
* Professional dark-themed UI optimized for presentations

#### Robustness & Usability
* Error handling for missing values, zero division, and outliers
* Responsive wide-screen layout for desktops and projectors
* Tab-based organization for logical, structured analysis

### Data Dictionary
#### Raw Original Fields
| Field Name        | Data Type | Description                                                         |
|-------------------|-----------|---------------------------------------------------------------------|
| Month             | Date      | Month when the scam was reported                                    |
| State             | String    | State/Territory of the victim (e.g., NSW, VIC, QLD)                 |
| Age Group         | String    | Age category of the victim                                          |
| Scam Type         | String    | Category of scam (e.g., investment, dating, phishing)               |
| Number of Reports | Integer   | Count of scam reports in the segment                                |
| Financial Loss    | Numeric   | Total monetary loss in AUD                                          |
| Contact Channel   | String    | Medium used to contact the victim (sms, email, social media, etc.)  |

#### Geographic & Demographic Fields
| Field Name        | Data Type | Description                                    |
|-------------------|-----------|------------------------------------------------|
| State Code        | String    | Standardized state abbreviation                |
| State Population  | Integer   | Official population from ABS census data       |
| Latitude          | Numeric   | Geographic center latitude of the state        |
| Longitude         | Numeric   | Geographic center longitude of the state       |


#### Calculated & Derived Fields
| Field Name                 | Data Type | Description                                                 |
|----------------------------|-----------|-------------------------------------------------------------|
| Average Loss per Report    | Numeric   | Total loss divided by total reports                         |
| Loss per Capita            | Numeric   | Total loss divided by state population                      |
| Hazard Score               | Numeric   | Composite state-level scam risk score (0–100)               |
| Total Reports (Filtered)   | Integer   | Total reports after applying user filters                   |
| Total Loss (Filtered)      | Numeric   | Total financial loss after applying user filters            |
| Loss per Minute            | Numeric   | Estimated loss per minute for contextual impact             |


#### Visualization & Analysis Fields
| Visualization Type      | Key Fields Used                          |
|-------------------------|------------------------------------------|
| Monthly Trend Chart     | Month, Financial Loss                    |
| Top Scam Types          | Scam Type, Total Loss                    |
| Age Group Analysis      | Age Group, Reports, Average Loss         |
| Geographic Risk Map     | State, Hazard Score, Loss per Capita     |
| Risk Bubble Matrix      | Reports, Average Loss, Total Loss        |


### How to Run
> streamlit run streamlit_app_group19_advanced.py
