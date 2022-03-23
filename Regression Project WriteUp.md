# Regression Project Write Up
### Predicting movie domestic gross revenue

##### Abstract

The goal of this project was to find the best fitting regression model that can be used to predict movie domestic gross revenue based on different genre and MPAA rating features. Data was scrapped from Box Office Mojo, and I looked at all the movies released in the United States since 2017, amounting to a total of 1063 data points. From each movie webpage, data from other categories were collected as well (see below). Once the data was cleaned and organized into a complete dataframe, I split the data into train and test sets at 80/20 split respectively. Then I leveraged the train data set against three different regression models (linear regression, ridge regression, and 2nd degree polynomial regression) and used K-fold cross validation to determine the best fit model. The best R^2 I got was 0.3, which suggests only 30% of the domestic gross revenue’s variance can be explained by the features I selected. 


##### Design

The success in finding a relationship between movie revenue and the selected features can help movie production companies make key decisions on the type of movie to shoot and the content to go with it. This relationship can be very important if it produces a viable prediction as it will increase profits gained. 

##### Data

As mentioned previously. The bulk of data points (1,063) were scraped from [Box Office Mojo](https://www.boxofficemojo.com/year/2022/?grossesOption=totalGrosses). Additional data from 12 categories were collected as well. 

1. Movie title
2. Movie distributor
3. Opening date
4. Release date
5. Days since release date
6. MPAA rating 
7. Movie run time
8. Movie genre
9. Widest release (number of theatres)
10. Domestic gross revenue
11. International gross revenue
12. World-wide gross revenue

The target feature was domestic gross revenue and the features of interest were: 

1. Movie run time
2. Widest release (number of theatres)
3. Movie genre
4. MPAA rating 

Movie genre and rating were object type categories, so data cleaning and feature engineering were required to transform the data sets. 

Total number of features that were included in the regression analysis: 18

##### Algorithms

Feature engineering: created dummy sets for both genre and MPAA rating - converted categorical data to binomial data sets

Models:
1. Linear regression
2. Ridge regression
3. Polynomial Degree 2 regression
4. Model train/test split 80/20
5. Kfolds cross validation technique k = 4 

##### Tools

1. BeautifulSoup + request for data scraping
2. Pandas, Numpy, Regularization for data manipulation/cleaning
3. Sklearn and Statsmodel for data regression analysis and model fitting
4. Matplotlib for data visualization 

##### Communication

Please view presentation slides [here](https://github.com/tesung/Regression-Project/blob/main/Regression%20Proj%20Presentation.pdf)