# Giuseppe's Portofolio
# 1st Project: E-commerce Company - Linear regression model

## What is the project about?

The data set is about an Ecommerce company based in New York City that sells clothing. Customers come in to the store, have sessions meetings with a personal stylist, then they can go home and order either on a mobile app or website for the clothes they want.

The company is trying to decide whether to focus their efforts on their mobile app experience or their website. In order to do so, I analyzed the set of data which contains various information about the customers and created a linear regression model that will help the business make a data-driven decision.

## What steps did I take?

### 1) Exploratory Data Analysis
  
After importing the data from a csv file into a Pandas dataframe, I used the Seaborn library to explore the dataset and check for possible correlations.

![image](https://user-images.githubusercontent.com/91633570/135598044-59fc3c2e-188f-46e8-bce5-2903928e9877.png)

We can already see a clear correletion between particular data


![image](https://user-images.githubusercontent.com/91633570/135600146-6cb26e27-9bc6-4ce1-be61-4c26e1e71a5e.png) ![image](https://user-images.githubusercontent.com/91633570/135600294-07566d86-5d62-4310-a974-63d972442050.png)

### 2) Trained and tested the linear regression model 
 
The user's data I used to train this model is: Average session lenght, Time spent on the app, Time spent on the website and lenght of the membership.

I then tested the model to evaluate its efficiency:

![image](https://user-images.githubusercontent.com/91633570/135608223-b55ed5b6-7263-4bce-9f9d-e7f2d6a8bbaf.png)

In this graph we can find the true values that we tried to predict in the x axis and the predicted values from the model on the y axis. Since the result is a almost a constant straight line, we can confirm that the model's predictions are indeed reliable.

### 3) Calculated the coefficients
 
![coeff](https://user-images.githubusercontent.com/91633570/135609501-3cce5982-9458-4b12-a528-207459e57bb3.PNG)

#### How can we interpret these coefficients?

Holding all other features fixed, a 1 unit increase in Avg. Session Length is associated with an increase of 25.98 total dollars spent.

Holding all other features fixed, a 1 unit increase in Time on App is associated with an increase of 38.59 total dollars spent.

Holding all other features fixed, a 1 unit increase in Time on Website is associated with an increase of 0.19 total dollars spent.

Holding all other features fixed, a 1 unit increase in Length of Membership is associated with an increase of 61.27 total dollars spent.

### Conclusion 

Going back to what the company asked, should they focus more on their mobile app or on their website? There are two ways to think about this: Develop the Website to catch up to the performance of the mobile app, or develop the app more since that is what is working better. In addition, it would be smart to consider the importance of the lenght of the membership, the company should focus their efforts on making sure to create good relationships with their customers, in order to increase loyality and therefore sales.





# 2nd Project: Advertisment Prediction - Logistic Regression Model

## What is the project about?

In this project I worked on a fake advertising data set, indicating whether or not a particular internet user clicked on an advertisement on a company website. The model I created will try to predict whether or not they will click on an ad based off the known features of that user.

## What steps did I take?

###  1) Exploratory Data Analysis

After importing the data from a csv file into a Pandas dataframe, I used the Seaborn library to explore the dataset to be more familiar with it.

![image](https://user-images.githubusercontent.com/91633570/135640536-810f9d7f-1b80-4b75-9853-54ee247f8065.png) ![image](https://user-images.githubusercontent.com/91633570/135640643-f7d054e8-da04-4026-8dbb-9c343025211c.png)

We can already tell that the most active users are in an age range that goes from 25 to 35 and which Income Area is around $65000.


### 2) Trained the logistic regression model

At this point i trained my model using the following data from the dataframe: 

Daily Time Spent on Site: consumer time on site in minutes
Age: cutomer age in years
Area Income: Avg. Income of geographical area of consumer
Daily Internet Usage: Avg. minutes a day consumer is on the internet
Male: Where 0 is equale to false and 1 to true

### 3) Tested the predictions of the model

Finally, I tested the model using the initial data set as a reference and as we can see with the following classification report, the model has a 91% average efficiency in predicting whether or not the user clicked on a specific ad.

![evaluation](https://user-images.githubusercontent.com/91633570/135644455-0d9afa9a-c5f7-4473-b49c-702642b329bd.PNG) 

And with the following confusion matrix we can see the actual guesses of the model

![conf_matrix](https://user-images.githubusercontent.com/91633570/135645225-b5635704-ca83-40f5-9f8a-230a9db0a71b.PNG)
 


