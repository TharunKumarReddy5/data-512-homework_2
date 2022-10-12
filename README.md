[![MIT License](https://img.shields.io/apm/l/atomic-design-ui.svg?)](https://github.com/tterb/atomic-design-ui/blob/master/LICENSEs)
![contributors](https://img.shields.io/github/contributors/TharunKumarReddy5/data-512-homework_2.svg)
![codesize](https://img.shields.io/github/languages/code-size/TharunKumarReddy5/data-512-homework_2.svg) 
![pullrequests](https://img.shields.io/github/issues-pr/TharunKumarReddy5/data-512-homework_2.svg) 
![closedpullrequests](https://img.shields.io/github/issues-pr-closed-raw/TharunKumarReddy5/data-512-homework_2.svg)

# data-512-homework_2

This repository contains the Homework 2 for DATA 512 Human Centered Data Science course at the University of Washington - Masters in Data Science program

# Goal: Considering Bias in Data

data-512-homework_2 project is an analysis exercise with primary goal to understand the general biases in the models that originate from the bias in the input data used for training the model. This short analysis on the quality of wikipedia articles of politicians based on regions gives a good clarityon how the coverage and quality of data varies among countries. It helps us understand the causes and consequences of biased data in large, complex data science projects.

## Datasource Information

The input data for this project is extracted from the below wikipedia (politicians wikipedia pages) and prb (population) web pages. Additionally, two more endpoints are used for page information and ORES scores. The datasource endpoints are licensed under the [CC-BY-SA 3.0]( CC-BY-SA 3.0 and GFDL licenses) and [GFDL licenses](CC-BY-SA 3.0 and GFDL licenses). ORES is a machine learning tool that can provide estimates of Wikipedia article quality. The ORES API endpoint provides the article quality estimates from best to worst:

FA - Featured article

GA - Good article

B - B-class article

C - C-class article

Start - Start-class article

Stub - Stub-class article

 - [Politicians by Nationality](https://en.wikipedia.org/wiki/Category:Politicians_by_nationality)
 - [World Population](https://www.prb.org/international/indicator/population/table/)
 - [ORES REST API](https://www.mediawiki.org/wiki/ORES)
 - [Wikimedia Foundation REST API terms of use](https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions)

## Dependencies

Install the dependencies from the requirements.txt file using

    python -m pip install -r requirements.txt

## Issues and Special Considerations

1. There are few duplicates in the politicians input data file. All the absolute duplicates are filtered from the data but the duplicates at article name level are taken into account for per-capita calculations. 
2. There are few countries where the population is 0. This can be because the value is in millions and is rounded to the nearest decimal. These countries are filtered at Step 4 where the article-per-capita is calculated as they give infinity values because of 0 in the denominator
3. Regions with cumulative population values are eliminated and the countries are mapped to the regions that are closest/lowest in the hierarchy of regions

## Research Implications

Include write-up paragraphs. One of your paragraphs should reflect on what you have learned, what you found, what (if anything) surprised you about your findings, and/or what theories you have about why any biases might exist (if you find they exist).

What biases did you expect to find in the data (before you started working with it), and why?
What (potential) sources of bias did you discover in the course of your data processing and analysis?
What might your results suggest about (English) Wikipedia as a data source?
What might your results suggest about the internet and global society in general?
Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might create biased or misleading results, due to the inherent gaps and limitations of the data?
Can you think of a realistic data science research situation where using these data (to train a model, perform a hypothesis-driven research, or make business decisions) might still be appropriate and useful, despite its inherent limitations and biases?
How might a researcher supplement or transform this dataset to potentially correct for the limitations/biases you observed?

## Repository Structure
Here are the main folders in our github data-512-homework_2 repository:
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
- population data (population_by_country_2022.csv) - Consists of countries, region and population for each country/region
- Politicians data (politicians_by_country.SEPT.2022.csv) - Consists of crawled Wikipedia article pages about politicians fropm wide range of countries

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
