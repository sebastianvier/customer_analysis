# customer_analysis

This is a Linear regression Model I built. The idea was to check a way to predict the amount of claim based on numerical and categorical data. For the numerical data the correlation was shown in only 3 columns. The model didn't improve once one of the other columns was added. 

For the numerical data, a logarithmic transformation was applied on one of the three columns, because the correlation decreased when applied to the others.


For the categorical data, I run boxplot on all the categories and look if the mean and the inner quartile range was different between the values. With those I use OneHotEncoder to encode the data.

After that the data was concatenated and the run through a ols linear model.

The best result was obtained by dropping the outlier values of the customer_lifetime_value column though the difference between dropping and not, was not too big.