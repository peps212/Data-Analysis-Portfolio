# 1st project: E-commerce company project - Linear regression model

## What is the project about?

The data set is about an Ecommerce company based in New York City that sells clothing. Customers come in to the store, have sessions meetings with a personal stylist, then they can go home and order either on a mobile app or website for the clothes they want.

The company is trying to decide whether to focus their efforts on their mobile app experience or their website. In order to do so, I analyzed the set of data which contains various information about the customers and created a linear regression model that will help the business make a data-driven decision.

## What steps did a take to solve the problem?

### 1) Exploratory Data Analysis
  
After importing the data from a csv file into a Pandas dataframe, I used the Seaborn library to explore the dataset and check for possible correlations.

![image](https://user-images.githubusercontent.com/91633570/135598044-59fc3c2e-188f-46e8-bce5-2903928e9877.png)

We can already see a clear correletion between particular data


![image](https://user-images.githubusercontent.com/91633570/135600146-6cb26e27-9bc6-4ce1-be61-4c26e1e71a5e.png) ![image](https://user-images.githubusercontent.com/91633570/135600294-07566d86-5d62-4310-a974-63d972442050.png)

### 2) Trained and tested the regression model 
 
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

Going back to what the company asked, should they focus more on their mobile app or on their website? There are two ways to think about this: Develop the Website to catch up to the performance of the mobile app, or develop the app more since that is what is working better. In addition, it would be smart to consider the importance of the lenght of the membership, the company should focus their efforts on making sure to create good relationships with their customers, in order to increasy loyality and sales.
