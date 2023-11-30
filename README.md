# Automated ETL Pipeline for Flight Data Analysis on Databricks

## Overview
This automated ETL pipeline is designed for the Databricks platform. It extracts flight data, performs transformation to identify patterns such as average delays by flight origin, and loads the results into Delta Lake. The pipeline is configured to run automatically, ensuring up-to-date data is available for analysis with minimal manual intervention.

## Getting Started

### Prerequisites
- Access to a Databricks workspace
- Apache Spark setup within Databricks
- An understanding of Databricks Jobs and scheduling

### Installation and Setup
1. Log in to your Databricks workspace.
2. Import the `.ipynb` notebooks into your workspace using the UI or via the Databricks CLI.
3. Ensure the selected Databricks runtime is compatible with the libraries used in the notebooks, including Delta Lake.

### Configuring the Automated ETL Pipeline
1. **Extract.ipynb**: Configure this notebook to extract data from the source. This can be set to trigger upon availability of new data or on a schedule.
2. **Transform.ipynb**: Set up this notebook to perform data transformation. Include data cleaning, validation, and analysis steps.
3. **Load.ipynb**: Configure this notebook to load the transformed data into Delta Lake. This should be set to trigger after the successful completion of the `Transform.ipynb` notebook.

### Scheduling the Pipeline
1. In the Databricks workspace, navigate to the `Jobs` section.
2. Create a new job, and attach the `Extract.ipynb` notebook to run as the first task.
3. Add subsequent tasks for `Transform.ipynb` and `Load.ipynb`, ensuring they run in the correct order.
4. Configure the job's schedule according to your data processing needs (e.g., daily, weekly, upon event trigger).
5. Set up alerts to notify you of the job's success or failure.

## Monitoring and Maintenance
- Regularly check the job runs and logs for any errors or warnings.
- Update the notebooks if there are changes in the data source or transformation logic.
- Keep the Databricks runtime and Delta Lake version up-to-date to utilize the latest features and improvements.

## Conclusion and Recommendations

### Conclusions
Our automated ETL pipeline has identified key areas where flight delays are prevalent, especially for shorter routes.

### Recommendations
- Enhance route planning and scheduling using insights from the transformed data.
- Integrate real-time data sources to improve the responsiveness of delay management strategies.
- Continuously monitor the pipeline's performance and adjust as needed for efficiency.

## Authors
- **Gunel Aghakishiyeva**
