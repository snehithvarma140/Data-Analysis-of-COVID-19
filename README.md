COVID-19 State-Wise Data Analysis in India
An exploratory data analysis (EDA) and visualization project focused on COVID-19 tracking across Indian states and union territories. This project utilizes Python and Pandas to clean raw state-level time-series data, extract latest cumulative metrics, and visualize national trends over time using Matplotlib.

📊 Dataset Overview
The dataset (states.csv) contains daily time-series records of COVID-19 metrics across Indian states.

Total Records: 45,614 rows

Features (7 columns):

Date - Date of record

State - State or Union Territory name

Confirmed - Cumulative confirmed COVID-19 cases

Recovered - Cumulative recovered cases

Deceased - Cumulative deceased cases

Other - Other non-standard classifications

Tested - Cumulative COVID-19 test samples conducted

🔑 Key Features & Pipeline
Google Colab Environment Setup: Mounts Google Drive for direct dataset streaming.

Data Inspection & Health Checks: Checks dataset dimensions (df.shape), column data types (df.info()), missing values (isnull()), and duplicate entries (duplicated()).

Data Preprocessing & Cleaning:

Converts string date columns into Pandas datetime objects.

Filters out aggregate records such as "India" and "State Unassigned" to isolate regional state-wise data.

State-Level Aggregation:

Extracts the latest cumulative statistics for 36 states/union territories.

Merges latest confirmed case figures with valid testing counts.

Monthly Time-Series Aggregation:

Converts dates into monthly periods (YearMonth).

Resamples state records to generate monthly national trend summaries.

Data Visualization:

Line Plot: Monthly COVID-19 trends (Confirmed, Recovered, Deceased) plotted in Crores.

Horizontal Bar Chart: Comprehensive ranking of all 36 states by total confirmed cases in Lakhs.

📈 Analysis & Insights Highlights
Dataset Scale: Processes over 45,000 temporal rows with zero missing values across core features.

Highest Impact States: Maharashtra, Kerala, Karnataka, and Tamil Nadu recorded the highest total confirmed COVID-19 cases.

National Trend: Clear visualization of case spikes and recovery rates over the entire tracking timeline.

🛠️ Project Structure
Plaintext
.
├── covid_analysis.ipynb   # Main Jupyter/Colab notebook containing code & execution outputs
├── states.csv             # COVID-19 state-level raw dataset
└── README.md              # Project documentation
🚀 How to Run
Clone the repository:

Bash
git clone https://github.com/your-username/covid19-india-analysis.git
cd covid19-india-analysis
Install required dependencies:

Bash
pip install pandas matplotlib
Execute the notebook:
Open covid_analysis.ipynb in Google Colab, Jupyter Notebook, or VS Code, ensure states.csv is present in the working directory, and run all cells sequentially.

💻 Tech Stack
Language: Python 3

Data Processing: Pandas

Visualization: Matplotlib

Environment: Google Colab / Jupyter Notebook
