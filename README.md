# Module 1 Final Project : Predicting House Sales in King County 
### Emily J. Cain - October 2018

## OSEMN Data Science Process

### Obtain
* Read in from csv file

### Scrub
* Change values to correct type as needed
* Replace or remove null or placeholder values
* Change formatting as needed
* Check for typos and duplicates

### Explore
* Understand the data through visualization, inspection, and descriptive statistics
* Explore relationships with visualization
* Understand why certain values were collected and included in dataset
* Generate questions that can be answered from the data

### Modeling - an Iterative Process
* Use questions to guide modeling
* Generate meaningful visualizations
* Normalize values as needed
* Use models to examine relationships between variables
* Assess model fit
* Repeat as needed

### iNterpret
* Draw conclusions from the data that answer initial questions or that raise new questions
* Evaluate meaning of results from a technical perspective
* Evaluate meaning of results for non-technical stakeholders
* Present and communicate results based on audience

### Question 1: What data will be useful for my analysis and for the stakeholders?
* Import libraries
* Obtain raw data from csv
* Clean the data by dealing with null values, placeholder values, and extreme outliers
* Determine which data (if any) will not be useful and drop from the dataset
* Use visualization and Exploratory Data Analysis (EDA) to identify the most useful and promising data

### Question 1 Answered
Determining which data would be useful in my analysis involved cleaning the data, replacing or removing null and placeholder values, investigating value counts, and removing data that I did not think would be useful.
* I dropped the `views` column because I felt it was not a consistent variable and could have a different value if the same house went on the market multiple times. Although it could have been useful in my analysis since it appeared that more views were associated with higher prices, I felt this was an unreliable variable and ultimately useless to the stakeholders.
* I dropped the `waterfront` column because of the very small number of waterfront properties. I first checked to see if waterfront had an immediately apparent relationship with price, and it did not. Due to the small number of waterfront properties and lack of apparent relationship with price, I decided this would not be useful for my analysis or for the stakeholders.
* I dropped the `id` column from the dataframe because I already had an index to identify my rows, and the id had nothing to do with a home's price.
* I replaced or dropped the placeholder rows in the `sqft_basement` column based on the relationship between the `sqft_living` and `sqft_above` values.
* I changed the `date` column to the proper format but ultimately dropped this column due to the fact that it was just another identifying value like `id` and was therefore not useful for my analysis.
* I dropped the `yr_renovated` column for the same reasons I dropped the 'waterfront' column. Very few homes were either renovated or had information about the year renovated, and there was not a clear association between this value and price.
* I did some early exploration with the `zipcode` variable but decided to keep the column until I could learn more about these values.

### Question 2: Which data will I use as the best predictors of price in my model?
* Check for colinearity
* Scale data as needed
* Normalize data as needed
* Create models
* Evaluate models based on various values
  * r-squared and r-squared adjusted
  * pvalues
  * mean squared error
  * root mean squared error
  * coefficients
* Evaluate models
* Repeat as needed
