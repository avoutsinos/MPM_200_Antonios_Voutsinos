# Template GitHub Repository for EpiPandit Lab
## Quantitative veterinary epidemiology and disease ecology lab
==============================

Text summarizing your project.
This R script loads 26 years of hummingbird intake records (6,908 birds, 12 columns) from three California rehabilitation centers, inspects the data's structure, and draws a reproducible random sample of 5,000 birds using set.seed(). Its main features are the tidyverse tools: `dplyr` summarises counts and survival proportions by center, variable and species group, and ggplot2 visualises them as bar charts and faceted panels. The script also converts the `Admitted` text column to a real date with as.Date() and its format argument, builds a Species_group variable, and checks for data problems such as duplicates, uneven reporting across centers and years, and inconsistent values. For outputs, it saves the sampled dataset as a CSV (with row.names = FALSE), saves a 4 × 3 inch PDF plot of birds admitted per center, and prints summary tables and plots of survival by variable, center and species group, alongside a chi-square test to check whether associations are more than chance. Overall, the analysis asks which birds are released versus die, and it uses proportions rather than raw counts, cleaned copies of the data and a fixed seed so that the comparisons are fair and the results are reproducible.
## Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make setup` or `make conda-create`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third-party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. The naming convention is a date (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `03132024-pranav-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── environment.yml   <- The environment file for reproducing the analysis environment, e.g.
    │                         generated with `conda create -f environment.yml`
    │
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to process data
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │
    │   └── visualization  <- Scripts to create exploratory and results-oriented visualizations

--------


## Setup Instructions
------------
1. Clone the repo
2. Create a virtual environment
3. Install the requirements
4. Run the notebooks

```bash
git clone
cd EpiPandit_Template
make conda-create
conda activate EpiPandit_Template
make setup
jupyter notebook
```
<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>.</small></p>
