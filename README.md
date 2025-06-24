# Sales Data Analytics (2014–2018)

## Overview
This project leverages data analytics techniques to analyze Acme Co.’s 2014–2018 USA sales dataset, aiming to enhance sales performance and inform strategic business decisions. By applying exploratory data analysis (EDA), we uncover key revenue and profit drivers, seasonal trends, outliers, and customer segments to optimize pricing, promotions, and market expansion. The insights derived will support the development of a Power BI dashboard for data-driven decision-making and sustainable growth in the sales domain.

## Problem Statement
The objective is to analyze Acme Co.’s 2014–2018 sales data to:
- Identify key drivers of revenue and profit across products, channels, and regions.
- Uncover seasonal trends and anomalies to improve forecasting and planning.
- Detect pricing and margin risks through outlier analysis.
- Align sales performance with budgets to reduce concentration risk.
- Provide actionable recommendations for pricing, promotions, and market expansion strategies.

## Objectives
- **Performance Insights**: Identify top-performing products, channels, and regions driving revenue and profit.
- **Trend Analysis**: Detect seasonal patterns and anomalies to optimize sales planning.
- **Risk Identification**: Highlight pricing and margin risks from outlier transactions.
- **Strategic Recommendations**: Inform pricing, promotion, and market-expansion strategies.
- **Visualization**: Lay the foundation for a Power BI dashboard to visualize key metrics and trends for stakeholders.

## Data Source
The dataset is provided in an Excel file (`sales_2014_2018.xlsx`) located in the `data/` directory. It contains sales transactions from 2014 to 2018, including columns for product, channel, region, customer segment, revenue, profit margin, unit price, and budget details.

## Repository Structure
- `data/`:
  - `sales_2014_2018.xlsx`: Raw sales dataset.
  - `cleaned_sales_data.csv`: Processed dataset after cleaning.
- `notebooks/`:
  - `acme_sales_eda.ipynb`: Main EDA notebook with data profiling, analysis, and visualizations.
- `visualizations/`:
  - Charts and plots (e.g., revenue distributions, seasonal trends, customer segmentations).
- `reports/`:
  - `sales_analysis_report.pdf`: Detailed report summarizing findings and recommendations.
- `code/`:
  - `data_cleaning.py`: Scripts for data preprocessing and cleaning.
  - `visualization_utils.py`: Helper functions for generating plots.
- `docs/`:
  - `analytics_methodology.md`: Documentation on data analytics techniques used (e.g., statistical analysis, clustering).
- `README.md`: Project overview and setup instructions.
- `requirements.txt`: List of required Python libraries.

## Methodology
1. **Data Profiling & Cleaning**:
   - Verified schema and corrected data types (e.g., dates, numeric fields).
   - Handled missing budget values using imputation or exclusion based on data patterns.
   - Removed duplicates and ensured consistency across transactions.
2. **Univariate & Bivariate Analysis**:
   - Analyzed distributions of revenue, profit margin, and unit price using histograms and box plots.
   - Explored performance breakdowns by product, channel, region, and customer segment.
3. **Trend & Seasonality Analysis**:
   - Charted monthly and yearly sales to identify recurring patterns (e.g., Q4 holiday surges, Q1 dips).
   - Used time-series decomposition to quantify seasonal effects.
4. **Outlier Detection**:
   - Identified extreme transactions using z-scores and IQR for revenue and unit price.
   - Flagged high-risk transactions for further investigation.
5. **Correlation & Segmentation**:
   - Calculated correlations between revenue, margin, and other metrics using Pearson/Spearman methods.
   - Clustered customers by revenue vs. profit margin using k-means clustering for targeted strategies.

## Key Findings
- **Top Performers**: Products A and B, online channels, and the West region contribute ~60% of total revenue.
- **Seasonal Trends**: Sales peak in November–December (Q4) due to holiday demand, with consistent Q1 declines.
- **Outliers**: Transactions with unit prices >99th percentile indicate potential overpricing; low-margin deals suggest excessive discounting.
- **Customer Segments**: High-revenue, low-margin customers represent a concentration risk, while mid-tier customers show stable margins.
- **Recommendations**:
  - Adjust pricing for low-margin products to improve profitability.
  - Launch targeted promotions in Q1 to boost sales during low periods.
  - Explore market expansion in underperforming regions like the Midwest.

## Setup Instructions
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/username/acme-sales-analysis.git
   cd acme-sales-analysis
   ```
2. **Install Dependencies**:
   Ensure Python 3.8+ is installed, then run:
   ```bash
   pip install -r requirements.txt
   ```
   Required libraries: pandas, numpy, matplotlib, seaborn, scipy, scikit-learn, openpyxl.
3. **Run the Notebook**:
   Launch Jupyter Notebook and open `notebooks/acme_sales_eda.ipynb`:
   ```bash
   jupyter notebook
   ```
4. **Access Data**:
   Ensure `sales_2014_2018.xlsx` is in the `data/` folder. Update file paths in the notebook if necessary.

## Visualizations and Dashboards
- Visualizations include:
  - Histograms and box plots for revenue, margin, and unit price distributions.
  - Bar charts for product, channel, and region performance.
  - Time-series plots for monthly and yearly sales trends.
  - Scatter plots for customer segmentation (revenue vs. profit margin).
- These visualizations are stored in the `visualizations/` directory and will be used to design a Power BI dashboard.

## How to Contribute
We welcome contributions to enhance this project! Here’s how you can get involved:
- **Star the Repository**: If you find this project useful, give it a star to show your support.
- **Leave Feedback**: Share your thoughts, questions, or suggestions in the Issues section.
- **Contribute Code**:
  - Fork the repository and create a pull request with your changes.
  - Ensure code follows PEP 8 standards and includes comments.
- **Share the Project**: Spread the word with others who might benefit from or contribute to this analysis.
- **Add Features**: Suggest or implement new analyses, visualizations, or predictive models.

## Next Steps
- Build a Power BI dashboard to interactively visualize key metrics and trends.
- Develop predictive models (e.g., time-series forecasting) to estimate future sales.
- Conduct deeper analysis of underperforming regions and customer segments.
- Integrate additional datasets (e.g., marketing spend) for richer insights.

