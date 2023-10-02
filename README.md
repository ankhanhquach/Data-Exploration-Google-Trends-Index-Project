# Data-Exploration

# Data Exploration Project

**Author:** Nick Huntington-Klein
**Date:** 2023-03-08

## Overview

Welcome to the Data Exploration Project! In this project, you will embark on a journey to compile and analyze messy real-world data to answer a research question. This project involves data cleaning, analysis, and interpretation.

## Data

The project's data is stored in a ZIP file named `Data_Exploration_Rawdata.zip`, which contains several files:

1. **trends_up_to_....csv**: These files are generated using Google Trends and represent the Google Trends index for specific keywords for a given month or week. Each keyword is indexed with a keynum and reflects a university in the United States, identified by schname. Multiple files exist because the Google Trends API has rate limits.

2. **Most+Recent+Cohorts+(Scorecard+Elements).csv**: This dataset is sourced from the College Scorecard and contains extensive information about United States colleges and their graduating students. The variable names may not be self-explanatory, but documentation is available in `CollegeScorecardDataDictionary-09-08-2015.csv`.

3. **id_name_link.csv**: This file is used to match colleges between the Scorecard data (identified by unitid and opeid/UNITID and OPEID) and the Google Trends data (identified by schname). You can use join functions (refer to `help(join)`) after loading the tidyverse library to facilitate this matching.

## Notes about the Data

- Multiple keywords represent each university, and the number of keywords varies among universities.

- Google Trends measures the popularity of search terms on Google over time.

- Google Trends indices are only comparable to themselves. Standardize the indices by subtracting the mean and dividing by the standard deviation for each term to make them reasonably comparable.

- Some universities share the same schname, which can complicate linking Scorecard data to Google Trends data. For this assignment, you can choose to drop all universities that share the exact name with another university.

## Research Question

The main research question for this project is as follows:

**Research Question:** 
Did the release of the College Scorecard at the start of September 2015 influence student interest in high-earning colleges relative to low-earning ones, as measured by Google searches for keywords associated with those colleges?

## Analysis

To answer the research question, you will need to perform at least one regression and create one graph as part of your analysis. Here are some considerations for your analysis:

1. **Defining "High-Earning" and "Low-Earning" Colleges**: You will need to decide how to categorize colleges as "high-earning" and "low-earning." This choice should be explained and justified in your analysis.

2. **Data Level**: Determine the level at which the data should be analyzed. You can keep the data as is, with one row per week per keyword, or aggregate it by grouping and summarizing, e.g., one week per college, one month per college, or one month per keyword. Explain your choice.

3. **Regression Model Design**: Design your regression model to address the research question. Consider transformations, functional forms, standard error adjustments, and how to interpret the results.

## Important Project Notes

- This project may require a significant amount of time, including data preparation and potential rework. Plan your schedule accordingly, starting well in advance of the deadline.

- Ensure that your analysis directly addresses the research question. Don't stray into unrelated analyses.

- Interpret the coefficients in your regression model carefully. Explain how they relate to the research question.

## The Writeup

Your project should include an RMarkdown file that performs the analysis and displays the results, along with explanations. Here are some key points to cover in your writeup:

1. Include at least one regression and one graph.

2. Explain why you performed the specific analysis you did and the choices you made in assembling it.

3. Clarify how your analysis directly addresses the research question.

4. Describe any additional analyses you conducted that influenced the design of your main analysis.

5. Summarize the real-world implications of your results.

6. There is no strict minimum or maximum length for the writeup, but a typical analysis should be around two pages of text.

## Your Project Submission

You will submit your project as a GitHub repository. Ensure that your repository follows the appropriate file structure:

- **data**: Folder for data files.
- **code**: Folder for code files.
- **processed_data**: Folder for any processed data files.

Additionally:

- If data files are too large for the repository, you can leave them out.

- Ensure code chunks are visible in your knitted document.

- You can separate data preparation and analysis code into different scripts if desired.

- Use relative file paths instead of absolute file paths.

- When reading `trends_up_to` files, you can use `import_list()` from the `rio` package with the `rbind=TRUE` option.

## Grading Rubric

Your project will be evaluated based on the following criteria:

- Meeting the project requirements and file structure (5%).

- Data cleaning quality (20%).

- Choice and justification of analyses (25%).

- Interpretation of individual results (20%).

- Broad interpretation of results in the context of the research question (20%).

- Clarity and engagement of writing (10%).

Remember that this project is an opportunity to demonstrate your data analysis skills, so ensure that your work is thorough, well-documented, and directly addresses the research question. Good luck with your Data Exploration Project!
