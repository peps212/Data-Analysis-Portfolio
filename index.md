# Giuseppe's Portofolio
The code for the following projects can be found by clicking on the "View on GitHub" button above.

# 1st Project: E-commerce Company - Linear regression model

## What is the project about?

The data set is about an Ecommerce company based in New York City that sells clothing. Customers come in to the store, have sessions meetings with a personal stylist, then they can go home and order either on a mobile app or website for the clothes they want.

The company is trying to decide whether to focus their efforts on their mobile app experience or their website. In order to do so, I analyzed the set of data which contains various information about the customers and created a linear regression model that will help the business make a data-driven decision.

## What steps did I take?

### 1) Exploratory Data Analysis
  
After importing the data from a csv file into a Pandas dataframe, I used the Seaborn library to explore the dataset and check for possible correlations.

![image](https://user-images.githubusercontent.com/91633570/135598044-59fc3c2e-188f-46e8-bce5-2903928e9877.png)

We can already see a clear correletion between particular sets of data


![image](https://user-images.githubusercontent.com/91633570/135600146-6cb26e27-9bc6-4ce1-be61-4c26e1e71a5e.png) ![image](https://user-images.githubusercontent.com/91633570/135600294-07566d86-5d62-4310-a974-63d972442050.png)

### 2) Trained and tested the linear regression model 
 
The user's data I used to train this model is:
- Average session lenght 
- Time spent on the app 
- Time spent on the website 
- Lenght of the membership.

I then tested the model to evaluate its efficiency:

![image](https://user-images.githubusercontent.com/91633570/135608223-b55ed5b6-7263-4bce-9f9d-e7f2d6a8bbaf.png)

In this graph we can find the true values that we tried to predict in the x axis and the predicted values from the model on the y axis. Since the result is a almost a constant straight line, we can confirm that the model's predictions are indeed reliable.

### 3) Calculated the coefficients
 
![coeff](https://user-images.githubusercontent.com/91633570/135609501-3cce5982-9458-4b12-a528-207459e57bb3.PNG)

#### How can we interpret these coefficients?

- Holding all other features fixed, a 1 unit increase in Avg. Session Length is associated with an increase of 25.7 total dollars spent.
- Holding all other features fixed, a 1 unit increase in Time on App is associated with an increase of 38.22 total dollars spent.
- Holding all other features fixed, a 1 unit increase in Time on Website is associated with an increase of 0.72 total dollars spent.
- Holding all other features fixed, a 1 unit increase in Length of Membership is associated with an increase of 61.57 total dollars spent.

### Conclusion 

Going back to what the company asked, should they focus more on their mobile app or on their website? There are two ways to think about this: develop the Website to catch up to the performance of the mobile app, or develop the app more since that is what is working better. 

it would also be smart to consider the importance of the lenght of the membership, the company should focus their efforts on making sure to create good relationships with their customers, in order to increase loyality and therefore sales.





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

- Daily Time Spent on Site
- Age
- Area Income
- Daily Internet Usage
- Sex

### 3) Tested the predictions of the model

Finally, I tested the model using the initial data set as a reference and as we can see with the following classification report, the model has a 91% average efficiency in predicting whether or not the user clicked on a specific ad.

![evaluation](https://user-images.githubusercontent.com/91633570/135644455-0d9afa9a-c5f7-4473-b49c-702642b329bd.PNG) 

And with the following confusion matrix we can see the actual guesses of the model

![conf_matrix](https://user-images.githubusercontent.com/91633570/135645225-b5635704-ca83-40f5-9f8a-230a9db0a71b.PNG)
 



# 3rd Project: Brief Analysis of Bank Stock prices
### What is the project about? 
This finance project focuses on analyzing the stock prices and returns of the following banks and creating financial indicators that can be used for technical analysis.

List of the banks: 
 - Bank of America - BAC
 - CitiGroup - C
 - Goldman Sachs - GS
 - JPMorgan Chase - JPM
 - Morgan Stanley - MS
 - Wells Fargo - WFC
 
### Importing the data
I imported the stock prices data using the using the pandas_datareader library, which allowed me to retrieve the stocks data from 1/1/2006 to 1/1/2016.

![bank_data](https://user-images.githubusercontent.com/91633570/135750679-8fa895f8-8e83-4cf3-8e93-fc3cf61e1876.PNG)

### Working with the dataset
Now we can extrapolate the informations we want from the dataset:
- What is the maximum close price for each of the stocks?

![stock1](https://user-images.githubusercontent.com/91633570/135751200-31d300c6-48a0-4cc3-9628-9da36f29988b.PNG)![Stock2](https://user-images.githubusercontent.com/91633570/135751204-9a85e95d-feb5-4e4e-b4f7-daac7ee52b23.PNG)


- Calculating the banks' returns for each day

![Returns](https://user-images.githubusercontent.com/91633570/135752028-82348919-c3f9-4b5a-a727-2e7514330b8f.PNG)

And we can also find what was the worst return day for each bank: 

![worst](https://user-images.githubusercontent.com/91633570/135752071-b0353141-e9c5-4d00-accb-a9da654858e3.PNG)

- Using standard deviation to identify the stock with the highest volatility

![risky](https://user-images.githubusercontent.com/91633570/135752155-5d08c054-f593-4769-8148-dd3bc6ceaf55.PNG)

### Plotting the prices of each bank over the 10 years period

![10y](https://user-images.githubusercontent.com/91633570/135752554-ad0ed49f-62dc-4d2b-8abf-94ccca338a11.PNG)


## Financial Indicators on the MS chart

in this section of the project I plotted and created the functions for four different financial indicators:

### SMA
I plotted the Simple Moving Average by calculating the everage of a selected range of closing prices by the number of periods in that range

![SMA](https://user-images.githubusercontent.com/91633570/135752814-86d41e88-74ce-48d7-ac73-94265fcc805d.PNG)


### EMA
The Exponential Moving Average is quite similar to the SMA, but it places a greater weight and significance on the most recent data points

![EMA](https://user-images.githubusercontent.com/91633570/135752912-e1c0c291-824e-4ed3-936b-af05f9738052.PNG)

### MACD
The Moving Average Convergence Divergence shows the relationships between two moving averages of a stock and it is calculated by subtracting the 26 period EMA from the 12 period EMA

![MACD](https://user-images.githubusercontent.com/91633570/135755675-afc5f985-6c44-4cb2-bcca-a2fa447f4ef7.PNG)

### RSI
The Relative Strenght Index measures the magnitude of recent price changes to evaluate overbought or oversold conditions in the price of a stock.

![RSI](https://user-images.githubusercontent.com/91633570/135755891-f149bb72-b083-4d91-967f-ab14737a86fe.PNG)

