Gender Inequality in Online Job Markets
==============================

In this project we explore gender inequality in online job markets with regards to pay and job opportunities. [Freelancer.com](https://www.freelancer.com/) serves as our platform in focus, and to account for confounding variables (and make equivalent comparisons), a genetic matching approach is used to find close counterfactuals.


Project Process
------------

1. [DONE] Extract data for various occupations (designer, software engineer, copywriter, and accountant) from Freelancer.com
2. [DONE] Clean and preprocess extracted data (e.g. first name extraction, NA removal, etc.)
3. [DONE] Predict gender based on first names and images
4. [DONE] Manually annotate profiles with low confidence predictions from Step 3 via profile
5. [WIP] Conduct EDA on the data to uncover initial trends and insights
6. Conduct genetic matching procedure to find close counterfactuals (i.e. same occupation, experience level, location, skills, etc.) differing solely across gender
7. Analyze pay and job opportunities against counterfactuals to evaluate inequality seemingly based solely on gender 
8. Present findings in a writeup and other formats (e.g. infographic, dashboard, or Medium article

Project Organization
------------


    ├── LICENSE
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── raw            <- The original, immutable data dump.
    │   ├── interim        <- Intermediate data that has been cleaned and transformed.
    │   ├── annotated      <- Annotated data after cleaning and transformation
    │   └── processed      <- The final, canonical data sets for modeling.
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         and a short `-` delimited description, e.g. `1.0-data-exploration`.                  
    │
    ├── references         <- Data dictionaries, codebooks, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    └── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
                              generated with `pip freeze > requirements.txt`

Authors
------------
- [L Xia](https://github.com/l-xia)
- [Korede Akande](https://github.com/KoredeAkande)
- [Daniel Hernández](https://github.com/DHDaniel)
    


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
