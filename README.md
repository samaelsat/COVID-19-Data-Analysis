COVID-19 Data Analysis & Visualization
A comprehensive data analysis project that visualizes COVID-19 statistics including cases, deaths, and population data across different countries and time periods.
📊 Overview
This project analyzes COVID-19 pandemic data using Python data science libraries to provide insights through various visualizations including:

Time series analysis of confirmed cases and deaths
Country-wise comparison of total cases
Population analysis by country/region
Correlation between population and total cases

📁 Dataset
The project uses three CSV datasets:

country_wise_latest.csv - Latest country-wise COVID-19 statistics
day_wise.csv - Daily time series data of COVID-19 cases
worldometer_data.csv - Worldometer data including population statistics

Dataset Source
The datasets are from the COVID-19 dataset archive. You can download them from Kaggle's COVID-19 Dataset.
🔧 Requirements
Python Version

Python 3.7 or higher

Libraries
bashpip install numpy pandas matplotlib seaborn
Or install all dependencies at once:
bashpip install -r requirements.txt
requirements.txt
numpy>=1.21.0
pandas>=1.3.0
matplotlib>=3.4.0
seaborn>=0.11.0
📂 Project Structure
covid19-analysis/
├── data/
│   ├── country_wise_latest.csv
│   ├── day_wise.csv
│   └── worldometer_data.csv
├── covid_analysis.py
├── requirements.txt
└── README.md
🚀 Installation & Setup
1. Clone the Repository
bashgit clone https://github.com/yourusername/covid19-analysis.git
cd covid19-analysis
2. Install Dependencies
bashpip install -r requirements.txt
3. Download Dataset

Download the COVID-19 dataset from Kaggle
Place the CSV files in the data/ folder or update the file paths in the code

4. Update File Paths
Edit the file paths in covid_analysis.py to match your local directory:
pythoncountry_df = pd.read_csv(r'data/country_wise_latest.csv')
day_wise_df = pd.read_csv(r'data/day_wise.csv')
worldometer_df = pd.read_csv(r'data/worldometer_data.csv')
5. Run the Analysis
bashpython covid_analysis.py
📈 Visualizations Generated
1. COVID-19 Cases and Deaths Over Time

Line graph showing the progression of confirmed cases and deaths
Time series visualization with optimized date ticks
Helps identify trends and peaks in the pandemic

2. Top 10 Countries by Total Cases

Bar chart displaying countries with the highest COVID-19 cases
Allows quick comparison between most affected nations
Sorted in descending order

3. Population Analysis by Countries/Regions

Bar chart showing population distribution across countries
Provides context for understanding case numbers relative to population

4. Population vs Total Cases Scatter Plot

Scatter plot correlating population size with total COVID-19 cases
Helps identify if larger populations correlate with more cases
Useful for understanding pandemic spread patterns

🔍 Data Processing Steps

Data Loading: Reads three CSV files into pandas DataFrames
Data Exploration:

Displays first few rows of each dataset
Shows column names
Checks data types and structure


Data Cleaning:

Identifies missing values
Removes rows with null values
Displays cleaned dataset shapes


Visualization: Creates four different plots for comprehensive analysis

📊 Key Features

✅ Comprehensive data cleaning and preprocessing
✅ Multiple visualization types (line, bar, scatter)
✅ Time series analysis
✅ Comparative country analysis
✅ Population correlation studies
✅ Professional plot formatting with labels and legends

🛠️ Customization
Modify Number of Top Countries
Change the number in the head() function:
pythontop_countries = country_df.sort_values(by='TotalCases', ascending=False).head(20)  # Show top 20
Adjust Figure Sizes
Modify the figsize parameter:
pythonplt.figure(figsize=(16, 8))  # Wider and taller plot
Change Color Schemes
Update color parameters in plots:
pythonplt.plot(day_wise_df['Date'], day_wise_df['Confirmed'], label='Confirmed Cases', color='blue')
Add More Visualizations
You can extend the analysis by adding:

Recovery rate analysis
Death rate percentages
Active cases trends
Regional comparisons

🐛 Troubleshooting
File Not Found Error

Ensure CSV files are in the correct directory
Use absolute paths or verify relative paths
Check file names match exactly (case-sensitive)

Missing Column Error

Verify column names in your CSV files match the code
Use print(df.columns) to check available columns
Update column names in the code if they differ

Plot Not Displaying

Add plt.show() at the end of each plot
If using Jupyter Notebook, use %matplotlib inline
Check if running in an environment that supports GUI

📝 Future Enhancements

 Add interactive plots using Plotly
 Include vaccination data analysis
 Create a dashboard using Streamlit or Dash
 Add statistical analysis and predictions
 Export visualizations as PDF report
 Add data update automation

🤝 Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

Fork the project
Create your feature branch (git checkout -b feature/AmazingFeature)
Commit your changes (git commit -m 'Add some AmazingFeature')
Push to the branch (git push origin feature/AmazingFeature)
Open a Pull Request

📄 License
This project is open source and available under the MIT License.
🙏 Acknowledgments

Dataset provided by Kaggle's COVID-19 community
Worldometer for real-time COVID-19 statistics
Python data science community for excellent libraries
