Gender Inequality in Online Job Markets
==============================

In this project we explore gender inequality in online job markets by investigating whether thee is any difference in hourly rates charged by male and female freelancers. [Freelancer.com](https://www.freelancer.com/) serves as our platform in focus, and to account for confounding variables (and make equivalent comparisons), a genetic matching approach is used to find close counterfactuals.

We scraped data from Freelancer based on four queries - accountant, copywriter, software engineer, and designer - and extracted approximately 10,000 rows of data. After cleaning the dataset, we conducted exploratory data analysis, which helped inform our matching process. We found that most occupations (except accounting) were dominated by men, and male freelancers tended to be more technical. From the exploratory analysis, we concluded that there seemed to be some earning inequalities, with male accountants earning significantly more on average than female accountants, and female translators earning significantly more, on average, than male translators. Male software engineers and copywriters earned slightly more than their female counterparts, while female designers and marketers earned slightly more than their male counterparts. We also saw that, on average, female freelancers charged less per hour. These differences in charged hourly rates do not appear to be driven by strong differences in skillset and certifications.

After encoding location size, conducting gender identification, and categorizing skills and certifications, we moved on to genetic matching. We experimented with a number of approaches, but struggled to create properly balanced treatment and control groups, especially on important covariates such as technical skills. However, we did find roughly similar treatment effects across these approaches:
![image](https://user-images.githubusercontent.com/44119914/164786174-ac1d3acc-1473-4f09-bf65-f615be604094.png)
 
To help fix our balance issue, we created separate DataFrames split by occupation and then matched on confounding variables such as join date, location, and average rating to find the treatment effect:
![image](https://user-images.githubusercontent.com/44119914/164786327-ccbb11b8-e124-4e70-95f4-603ed12a3b04.png)

Although this approach helps us better control for the impact of occupation on hourly rate, the smaller sample sizes made it difficult for us to achieve statistical significance, although we do come close on designer and software engineer, the two occupations with the largest sample sizes. From these results, we can see that there seems to be the largest pay gap between males and females in software engineering and the smallest in copywriting but to reach more conclusive results, we would need a larger dataset.


Project Process
------------

1. [DONE] Extract data for various occupations (designer, software engineer, copywriter, and accountant) from Freelancer.com
2. [DONE] Clean and preprocess extracted data (e.g. first name extraction, NA removal, etc.)
3. [DONE] Predict gender based on first names and images
4. [DONE] Manually annotate profiles with low confidence predictions from Step 3 via profile
5. [DONE] Conduct EDA on the data to uncover initial trends and insights
6. [DONE] Conduct genetic matching procedure to find close counterfactuals (i.e. same occupation, experience level, location, skills, etc.) differing solely across gender
7. [DONE] Analyze pay and job opportunities against counterfactuals to evaluate inequality seemingly based solely on gender 
8. [WIP] Present findings in a writeup and other formats (e.g. infographic, dashboard, or Medium article

Project Organization
------------


    ├── LICENSE
    ├── README.md                  <- The top-level README for developers using this project.
    ├── data
    |   ├── codebook               <- Codebooks for original and processed dataset
    |   ├── cities                 <- External dataset on cities in the US
    │   ├── raw                    <- The original, immutable data dump.
    |   ├── gender-annotated       <- Outputs from gender annotation - these are the final "original" files before matching-specific preprocessing.
    |   ├── profile-images         <- Profile images from freelancers from scraping - used to determine gender.
    │   ├── interim                <- Intermediate data that has been cleaned and transformed.
    │   ├── annotated              <- Annotated data after cleaning and transformation
    │   └── processed              <- The final, canonical data sets for modeling.
    │
    ├── models                     <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks                  <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                                 and a short `-` delimited description, e.g. `1.0-data-exploration`.                  
    │
    ├── reports                    <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures                <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt           <- The requirements file for reproducing the analysis environment, e.g.
    │                                 generated with `pip freeze > requirements.txt`
    │
    └── setup.py                   <- The Python setup file that sets up the environment with the required packages (including non-python packages)

Authors
------------
- [L Xia](https://github.com/l-xia)
- [Korede Akande](https://github.com/KoredeAkande)
- [Daniel Hernández](https://github.com/DHDaniel)
    


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
