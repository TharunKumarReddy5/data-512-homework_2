[![MIT License](https://img.shields.io/apm/l/atomic-design-ui.svg?)](https://github.com/tterb/atomic-design-ui/blob/master/LICENSEs)
![contributors](https://img.shields.io/github/contributors/TharunKumarReddy5/data-512-homework_2.svg)
![codesize](https://img.shields.io/github/languages/code-size/TharunKumarReddy5/data-512-homework_2.svg) 
![pullrequests](https://img.shields.io/github/issues-pr/TharunKumarReddy5/data-512-homework_2.svg) 
![closedpullrequests](https://img.shields.io/github/issues-pr-closed-raw/TharunKumarReddy5/data-512-homework_2.svg)

# data-512-homework_2

This repository contains the Homework 2 for DATA 512 Human Centered Data Science course at the University of Washington - Masters in Data Science program

## Research Implications
Include write-up paragraphs. One of your paragraphs should reflect on what you have learned, what you found, what (if anything) surprised you about your findings, and/or what theories you have about why any biases might exist (if you find they exist).

What biases did you expect to find in the data (before you started working with it), and why?
What (potential) sources of bias did you discover in the course of your data processing and analysis?
What might your results suggest about (English) Wikipedia as a data source?
What might your results suggest about the internet and global society in general?
Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data?
Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might still be appropriate and useful, despite its inherent limitations and biases?
How might a researcher supplement or transform this dataset to potentially correct for the limitations/biases you observed?

## TO BE EDITED

# Professionalism & Reproducibility : Goal

data-512-homework_2 project is an analysis exercise with primary goal to learn and incorporate the best practices for project documentation, as outlined in "Assessing Reproducibility" and "The Basic Reproducible Workflow Template" from The Practice of Reproducible Research.

## Datasource Information

The data for this project is extracted from the Pageviews API. The datasource endpoint is licensed under the [CC-BY-SA 3.0]( CC-BY-SA 3.0 and GFDL licenses) and [GFDL licenses](CC-BY-SA 3.0 and GFDL licenses). The Pageviews API (documentation, endpoint) provides access to desktop, mobile web, and mobile app traffic data from July 2015 through the previous complete month. Leveraging the API, I collected the pageviews information using a subset of Wikipedia article pages from July 2015 to September 2022. Please find below the subset of the English Wikipedia that represents a large number of dinosaur related articles.

 - [Pageviews API Endpoint](https://wikimedia.org/api/rest_v1/#!/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end)
 - [Pageviews API Documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews)
 - [Wikimedia Foundation REST API terms of use](https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions)
 - [Dinosaur articles](https://docs.google.com/spreadsheets/d/1zfBNKsuWOFVFTOGK8qnTr2DmHkYK4mAACBKk1sHLt_k/edit?usp=sharing)

## Dependencies

Install the dependencies from the requirements.txt file using

    python -m pip install -r requirements.txt

## Issues and Special Considerations

The code has embedded exception handling to cover and highlight the articles for which we are not able to pull the page views information. As of now we are able to pull the information for all the dinosaur articles. Check for the comments in the code to debug the exceptions. 

## Repository Structure:
Here are the main folders in our github data-512-homework_1 repository:
```bash
.
├── DATA 512 Homework 2 Tharun.ipynb
├── README.md
├── LICENSE
├── input
│   ├── politicians_by_country_SEPT.2022.csv
│   └── population_by_country_2022.csv
├── logs
│   ├── page_info_error_log.txt
│   └── scores_error_log.txt
├── output
│   ├── wp_countries-no_match.txt
│   └── wp_politicians_by_country.csv
├── plots
│   ├── bottom10_countries_by_coverage.png
│   ├── bottom10_countries_by_quality.png
│   ├── regions_high_quality_coverage.png
│   ├── regions_total_coverage.png
│   ├── top10_countries_by_coverage.png
│   └── top10_countries_by_quality.png
├── requirements.txt
```
## Input Data Files
population data (population_by_country_2022.csv) - Consists of countries, region and population for each country/region
Politicians data (politicians_by_country.SEPT.2022.csv) - Consists of crawled Wikipedia article pages about politicians fropm wide range of countries

## Output Data Files

### Countries with No Match
wp_countries-no_match.txt - All countries for which there are no matches i.e., either the population dataset does not have an entry for the equivalent Wikipedia country, or vice-versa

### Consolidated Data
wp_politicians_by_country.csv - Consolidated the remaining data that contains politicians data with population data into a single CSV file

### Screenshots

Examples of output plots generated by the functions

- **Screenshot of plot 1: ** Top 10 Countries by Coverage

The first graph contains the bar plot indicating the top 10 countries by coverage (total-article-per-capita)

[Image1](https://github.com/TharunKumarReddy5/data-512-homework_2/blob/main/plots/top10_countries_by_coverage.png)
![Alt text](https://github.com/TharunKumarReddy5/data-512-homework_2/blob/main/plots/top10_countries_by_coverage.png "Top 10 Countries by Coverage")

- **Screenshot of plot 2: ** Bottom 10 Countries by Coverage

The second graph contains the bar plot indicating the bottom 10 countries by coverage (total-article-per-capita)

[Image2](https://github.com/TharunKumarReddy5/data-512-homework_2/blob/main/plots/bottom10_countries_by_coverage.png)
![Alt text](https://github.com/TharunKumarReddy5/data-512-homework_2/blob/main/plots/bottom10_countries_by_coverage.png "Bottom 10 Countries by Coverage")

- **Screenshot of plot 3: ** Top 10 Countries by High Quality Articles Coverage

The third graph contains the bar plot indicating the top 10 countries by high quality coverage (high-quality-article-per-capita)

[Image3](https://github.com/TharunKumarReddy5/data-512-homework_2/blob/main/plots/top10_countries_by_quality.png)
![Alt text](https://github.com/TharunKumarReddy5/data-512-homework_2/blob/main/plots/top10_countries_by_quality.png "Top 10 Countries by High Quality Articles Coverage")

- **Screenshot of plot 4: ** Bottom 10 Countries by High Quality Articles Coverage

The fourth graph contains the bar plot indicating the bottom 10 countries by high quality coverage (high-quality-article-per-capita)

[Image4](https://github.com/TharunKumarReddy5/data-512-homework_2/blob/main/plots/bottom10_countries_by_quality.png)
![Alt text](https://github.com/TharunKumarReddy5/data-512-homework_2/blob/main/plots/bottom10_countries_by_quality.png "Bottom 10 Countries by High Quality Articles Coverage")

- **Screenshot of plot 5: ** Geographic Regions by Total Coverage

The fifth graph contains the bar plot indicating the regions by coverage (article-per-capita)

[Image5](https://github.com/TharunKumarReddy5/data-512-homework_2/blob/main/plots/regions_total_coverage.png)
![Alt text](https://github.com/TharunKumarReddy5/data-512-homework_2/blob/main/plots/regions_total_coverage.png "Regions Articles Coverage")

- **Screenshot of plot 6: ** Geographic Regions by High Quality Articles Coverage

The sixth graph contains the bar plot indicating the regions by high quality coverage (high-quality-article-per-capita)

[Image6](https://github.com/TharunKumarReddy5/data-512-homework_2/blob/main/plots/regions_high_quality_coverage.png)
![Alt text](https://github.com/TharunKumarReddy5/data-512-homework_2/blob/main/plots/regions_high_quality_coverage.png "Regions High Quality Articles Coverage")

## Code Style

Languages used: Python
Coding Style:
    - PEP 8
    - Docstrings

Following sofware design principles have been considered while packaging MLPA:

- Modular design
    - *'Somewhat General Purpose'* module
    - Deep Modules
    - Separation of Concerns
- Reusability/Extensibility
- Intuitable
- Exception Handling

## Authors
- [Tharun Kumar Reddy Karasani](https://github.com/TharunKumarReddy5)

![GitHub Contributors Image](https://contrib.rocks/image?repo=TharunKumarReddy5/data-512-homework_1)

## Contribute

This project is an open-source project- open to the Python user community for contribution.
