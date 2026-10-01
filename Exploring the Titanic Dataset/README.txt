# Titanic Dataset Exploratory Data Analysis (EDA)

## Project Overview
This project provides an exploratory data analysis (EDA) of the Titanic passenger dataset. The objective is to investigate the structural layout of the data, clean missing values, uncover hidden demographic insights, and analyze the primary factors that determined passenger survival rates.

## Data Pipeline & Workflow

1. Structural Inspection
- Dimension Mapping: Evaluated the dataset grid using shape dimensions to verify total row counts and column footprints.
- Feature Typing: Audit column formats (info()) to separate numerical metrics from text labels.
- Missing Value Identification: Located and quantified missing entries per column to map data gaps before visualization.

2. Grouping & Stratification
- Demographic Segmentation: Implemented pd.cut() to transform continuous numeric ages into distinct category groups (Child, Teenager, Adult, Senior).
- Survival Analysis: Isolated and group passenger parameters using categorical features to calculate distinct metrics.

3. Distribution Comparison
- Relative Frequency Scaling: Leveraged value_counts(normalize=True) to convert raw survival distributions into normalized decimals.
- Target Filters: Applied boolean index masks (train[...]) to inspect independent features exclusively within the isolated survivor and non-survivor cohorts.

## Core Data Insights

- Gender Dynamics: Female survival tracking stands at ~74%, while Male survival drops to ~19%. Confirms strict execution of the historical "women and children first" evacuation protocol.
- Socioeconomic Class: 1st Class records the highest survival rates, scaling down progressively to the lowest rates in 3rd Class. Ticket tiering and deck placement drastically altered physical access to upper deck lifeboats.
- Age Buckets: Children achieved high survival percentages compared to the Adult and Senior cohorts. Evacuation logs confirm strong physical priority given to protecting the youth onboard.
- Relative Frequency: The Survivor cohort is dominated by females and 1st class tickets, while the Non-Survivor cohort is overwhelmingly male and 3rd class. Survival was not random; it was highly dependent on demographic indicators.
