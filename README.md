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
├── dinosaur_genera.cleaned.SEPT.2022.xlsx
├── dinosaurs_all.xlsx
├── json
│   ├── dino_monthly_cumulative_201507-202209.json
│   ├── dino_monthly_desktop_201507-202209.json
│   └── dino_monthly_mobile_201507-202209.json
├── plots
│   ├── max_min_average_views.png
│   ├── top_10_peak_page_views.png
│   └── articles_with_fewest_months_data.png
├── requirements.txt
```
## Input Data Files
dinosaur_genera.cleaned.SEPT.2022.xlsx - Input data file that contains the subset of article names of dinosaur wikipedia pages.


## Output Data Files

### JSON Files
dino_monthly_desktop_201507-202209.json - JSON file that contains all articles pages view data for desktop access type
dino_monthly_mobile_201507-202209.json - JSON file that contains all articles pages view data for mobile access type
dino_monthly_cumulative_201507-202209.json - JSON file that contains the cumulative page views of all articles for both desktop and mobile access type

### Screenshots

Examples of output plots generated by the functions

- **Screenshot of plot 1: ** Maximum Average and Minimum Average

The first graph contains time series for the articles that have the highest average page requests and the lowest average page requests for desktop access and mobile access. The graph has four lines (max desktop, min desktop, max mobile, min mobile).

[Image1](https://github.com/TharunKumarReddy5/data-512-homework_1/blob/main/plots/max_min_average_views.png)
![Alt text](https://github.com/TharunKumarReddy5/data-512-homework_1/blob/main/plots/max_min_average_views.png "Articles with fewest Months of Data")

- **Screenshot of plot 2: ** Top 10 Peak Page Views

The second graph contains time series for the top 10 article pages by largest (peak) page views over the entire time by access type. The graph has the top 10 for desktop and top 10 for mobile access (20 lines).

[Image2](https://github.com/TharunKumarReddy5/data-512-homework_1/blob/main/plots/top_10_peak_page_views.png)
![Alt text](https://github.com/TharunKumarReddy5/data-512-homework_1/blob/main/plots/top_10_peak_page_views.png "ML Pipeline Hyperparameter Diagram")

- **Screenshot of plot 3: ** Fewest Months of Data

The third graph contains pages that have the fewest months of available data. The plot will have relatively short time series, some may only have one month of data. The graph has the 10 articles with the fewest months of data for desktop access and the 10 articles with the fewest months of data for mobile access.

[Image3](https://github.com/TharunKumarReddy5/data-512-homework_1/tree/main/plots/articles_with_fewest_months_data.png)
![Alt text](https://github.com/TharunKumarReddy5/data-512-homework_1/blob/main/plots/articles_with_fewest_months_data.png "Articles with fewest Months of Data")

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
