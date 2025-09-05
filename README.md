## Metis Project 5: COVID-19 and Household Gender Equality

by [Matt Ranalletta](https://www.linkedin.com/in/matthewranalletta/)

## Summary

In July 2020, Facebook (in conjunction with the World Bank, UN Women, Equal Measures 2030, and Ladysmith) [surveyed half a million people](https://dataforgood.fb.com/docs/gendersurveyreport/) on their platform in 208 countries and territories around the world, to capture household gender dynamics during the COVID-19 pandemic. 
<br><br>
There were two goals for this project: (1) to explore how gender equality at home has gotten worse during COVID-19; and (2) to discover the influencing factors and how that varied by country.
<br><br>
I created a regression model to predict the amount of hardship a household felt during the pandemic. The “hardship” value was based on aggregated percentages of people from the survey who felt that COVID-19 has made their life harder, including less access to medicine, losing a job, or being forced to migrate to a different location. I used both COVID data per capita as well as demographic questions from the global survey as features in the regression model to predict that hardship value.


## Methodologies

1. Merged two sets of data:
   - [Facebook survey on household gender equality](https://github.com/mattranalletta/05-gender-equality-COVID-19/blob/main/data/sog_agg_country.csv), taken in July 2020
   - [Worldwide COVID-19 cases and deaths, per country](https://github.com/mattranalletta/05-gender-equality-COVID-19/blob/main/data/owid-covid-data.csv)
2. Performed exploratory data analysis and cleaning.
3. Used regression modeling techniques (linear, polynomial, Lasso, Ridge) to do initial modeling.
4. Feature engineered and removed outliers to find the best model.
5. Visualized results in Tableau and Google Slides.

## Findings and Conclusions

After training and feature engineering a model, I ended up with a .57 R-squared value and a 3.71 RMSE, with all countries having COVID-19 hardship values in the range of 10 to 37.

Top features with positive correlation to COVID-19 hardship:
- Country in the Americas (+2.55)
- More likely to have internet access (+2.01) - surprising!
- COVID-19 cases per capita (+0.99)
- More likely to say you have an unsafe home (+0.95)
- Country in Sub-Saharan Africa (+0.88)

Top features with negative correlation:
- Living alone (-1.72) - also surprising; possibly due to those living alone tending to be wealthier in the first place, so they experienced less hardship
- Higher Human Development Index (-0.71)
- COVID-19 deaths per capita (-0.57)
- “Men and women should have equal opportunities” (-0.50)
- Population of country (-0.15)

## Deliverables

- [Data collection]()
- [EDA notebook](https://github.com/mattranalletta/05-gender-equality-COVID-19/blob/main/code/covid_EDA.ipynb)
- [Regression Model notebook](https://github.com/mattranalletta/05-gender-equality-COVID-19/blob/main/code/covid_regression.ipynb)
- [Presentation - Google Slides](https://docs.google.com/presentation/d/1vzg987GceCEmjcfCDQ6YUQ-qbpBd01dMGILZwP2vn5E/edit?usp=sharing) / [PDF](https://github.com/mattranalletta/05-gender-equality-COVID-19/blob/main/presentation/Household%20Gender%20Equality%20during%20COVID-19.pdf)

## Technologies and Libraries Used

- Jupyter Notebook
- Python
- Pandas
- Matplotlib
- Scikit-learn regression modeling
   - Linear 
   - Polynomial
   - LassoCV
   - RidgeCV
- Tableau
