

# Linear regression in Python

 ##what is linear regression? 
 
 It is a process to find relationships between variables.

In order to use linear regression in Python we need to import it:

    from sklearn.linear_model import LinearRegression

### Some important functions to fit a linear regression model:

|||
|--------|-------------------|
|lm.fit()|fits a linear model|
|lm.predict()|Uses estimated coefficients with the linear model to predict Y|
|lm.score()|The coefficient of determination is returned|

Note: With increeasing data, the error in prediction might also increase.

### Training and validation data sets

Usually linear regression isn't implemented on the entire data set, it's usually used on some training and testing data sets to monitor it's performance and efficiency.

Note: scilit learn provides a function for training and testing by spliting, called train_test_split().

Note: A good why to visualize errors in data is by using Residual plots.

## Things I want to know more about

 none
## Resources

[sources1](https://realpython.com/linear-regression-in-python/)

[sources2](https://towardsdatascience.com/train-test-split-and-cross-validation-in-python-80b61beca4b6)

