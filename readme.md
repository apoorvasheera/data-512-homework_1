
# Professionalism and Reproducibility

### Objective
This repository aims to demonstrate best practices for open scientific research by constructing, analyzing, and publishing a dataset of monthly article traffic for a select set of pages from English Wikipedia from July 1, 2015, through September 30, 2024.

The analysis focuses on the principles of reproducibility and transparency, illustrating how to document and publish research results that can be verified and extended by other researchers.

### Installation

To set up the environment and run the Jupyter notebook, you need to create a conda environment from the provided `environment.yml` file. Run the following command to create the environment:

```sh
conda env create -f environment.yml
```

This command will set up all the necessary dependencies required to execute the notebook.

### Data Description

The dataset constructed for this project consists of monthly article traffic data for a selection of English Wikipedia articles related to rare diseases. The traffic data was gathered using the Wikimedia Pageviews API.

#### Data Files
- **Final Output Files**: The final dataset files (`rare-disease_monthly_mobile_201507-202409.json`, `rare-disease_monthly_desktop_201507-202409.json`, `rare-disease_monthly_cumulative_201507-202409.json`) consolidate the pageviews data across different access types to provide a comprehensive overview. 
- **Intermediary Data Files**: The script may generate intermediary JSON files such as `rare-disease_monthly_mobile-web_201507-202409.json`, `rare-disease_monthly_mobile-app_201507-202409.json` which contain raw pageviews data by access type (e.g., mobile-web, mobile-app).
- **Input Data Files**: We use a pre-created file `rare-disease_cleaned.AUG.2024.csv` with article details (title, pageid, url) to generate our dataset.


#### Data Schema for output files
- **disease**: The name of the Wikipedia article, representing a specific disease.
- **month**: The month in `YYYYMMDDHH` format indicating the time period for the pageviews.
- **views**: The total number of views for the article during the specified month.

### Usage

The main analysis is performed in the Jupyter notebook `professionalism-and-reproducibility.ipynb`. This notebook includes the following steps:
1. Data Extraction: Pulling monthly pageviews data from the Wikimedia API for selected articles.
2. Data Processing: Processing the data to create cumulative files.
3. Data Analysis and Visualization: Generating plots that represent key findings, such as peak traffic and time series of views for different access types.

To run the notebook:
1. Activate the environment:
   ```sh
   conda activate homework-1
   ```
2. Launch Jupyter Notebook:
   ```sh
   jupyter notebook
   ```
3. Open `professionalism-and-reproducibility.ipynb` to execute the cells.

### License

The data used in this project is obtained from Wikipedia and is subject to the [Wikimedia Foundation Terms of Use](https://foundation.wikimedia.org/wiki/Policy:Terms_of_Use). The dataset we have created should also adhere to these terms, which require appropriate attribution and prohibit commercial reuse without permission. The ToU state that you are legally responsible for all 
of your contributions, edits, and reuse of Wikimedia content under the laws of the United States of America and other applicable laws

### API Documentation

The pageviews data is retrieved using the Wikimedia Pageviews API. For more details, refer to the official [API documentation](https://doc.wikimedia.org/generated-data-platform/aqs/analytics-api/).

### Known Issues and Considerations
- **Data Gaps**: Some months might have missing data due to Wikipedia's data collection constraints or outages.
- **Accuracy**: The traffic data reflects user activity but may be influenced by bots or automated queries.
- **Data Formats**: The `month` column is in a custom date format (`YYYYMMDDHH`), which may require conversion to a more standard format for some analyses.

### Attributions
- The Wikimedia Foundation for providing open access to Wikipedia data.
- Dr. David W. McDonald for his example code and rare-disease dataset

### Resources
- [Wikimedia Foundation Terms of Use](https://foundation.wikimedia.org/wiki/Policy:Terms_of_Use)
- [Wikimedia Pageviews API Documentation](https://doc.wikimedia.org/generated-data-platform/aqs/analytics-api/)

Feel free to contribute to this repository by submitting pull requests or reporting issues.


