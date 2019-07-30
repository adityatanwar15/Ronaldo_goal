# Ronaldo_goal
It is model based that I have worked on whether the Ronaldo is going to score or not.

This dataset was part of competetion problem I had faced ,This was my first model I have built from scratch so please mind the errors.

Understanding uptill now :

We have few rows with missing is_goal data which is our test data. We have to predict the probaability for the missing rows is_goal column with our machine learnign model

The data we will use for train is the rows which are having any particular value of is_goal present.

Now once we have segregated the train data and test data.

We will divide our data into X, y i.e input and output set, -->So we will put the output Y column as is_goal and for -->Other columns will be our input X.

Now as the data we have in X constitutes of the columns with different data types , so we would require to do some exploratory data analysis before we could make use of the same in our model.

The first thing is that : the columns pertaining to numerical value have a lot of Null(NAN) values present in them, we tend to use filler functions to treat them first like FillNa() to fill the null values with the mean average or some by default value or we can simply drop them altogether but that might lead to loss of data.

Note : We can also use SimpleImputer to transform our data .

question for myself? We are doing above steps in the hope of having better performance on our system i,e lesser mean absolute error, mean squared error or whichever evaluation metric we are using . or is it a necessity to implicate our Data into Ml Model that is it won't be working with NAN values or throwing.

okay so once we have treated the null values with our imputer/fillna for numerical or i.e non object data type then we can work over our categorical features .

As the categorical variable data also possesss significant amout of business information it would very much apt to bring our categorical into numerical so that they can inculcated to be included into our model.

We have tried using label encoder for our data which will encode each of the term with a numerical value and i have seen mean absolute error for my model hasn't reduced much after using it.

For using label encoder I have filtered categorical variables and the variables with the data set similar in train , validation and test are good to be taken for label encoding.

