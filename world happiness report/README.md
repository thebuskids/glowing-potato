# Exploratory Data Analysis - World Happiness Report 2024

In this project, we will be performing exploratory data analysis (EDA) on the World Happiness Report 2024 data captured from 143 countries.

## Definitions

Regional indicator: region

Ladder score: based on the Cantril Ladder with steps 0 to 10. The top of the ladder represents the best possible life

Log GDP per capita: log of the average value of goods and services produced per person in a country or region

Social support: feeling of having a network of people who are there for you in times of need, who offer encouragement, and who provide a sense of belonging

Healthy life expectancy: number of years a person is expected to live in good health, considering their lifespan and the prevalence of disabilities and diseases

Freedom to make life choices: level of personal autonomy and control individuals have over their own lives, including their ability to make choices about education, work, relationships, and where to live, without excessive restrictions imposed by society or government

Generosity: the residual from regressing the national average of GWP responses to the donation question “Have you donated money to a charity in the past month?” on log GDP per capita i.e. a country with a higher GDP per capita would need to show proportionally more generosity to earn a high score

Perceptions of corruption: degree to which people in a country believe that corruption is widespread throughout the government or within businesses

Dystopia + residual: imaginary country that has the world's least happy people; serves as a benchmark against which all other countries can be compared

## Overview

The aim of this project is to explore how happiness a.k.a. ladder scores differ between countries in 2024. We also aim to look at some of the possible correlations between happiness (ladder score) and macro-economic and socioeconomic indicators like GDP per capita and healthy life expectancy, using techniques like seaborn's `pairplot` and `heatmap`, as well as `corr`.

Since the data is available, we will also explore the trend in GDP per capita across countries over the years to see if there are any meaningful insights.

## Dataset

Information about the dataset:

- **Source:** https://www.kaggle.com/datasets/jainaru/world-happiness-report-2024-yearly-updated
- **Structure:** 143 rows, 12 columns
- **Features:** 10 columns of `float` type, 2 columns of `object` type

## EDA Process

- Data Cleaning & Transformation
- Handling of Missing Values
- Data Visualization

## Key Findings

- Generally, countries tend skew toward happy in 2024.
- There is a positive correlation between ladder / happiness score and gdp per capita, social support, healthy life expectancy.
- There was a fall in GDP per capita which coincides with the COVID-19 pandemic.
