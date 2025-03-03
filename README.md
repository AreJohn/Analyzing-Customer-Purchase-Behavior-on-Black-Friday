# Analyzing-Customer-Purchase-Behavior-on-Black-Friday

##### This project analyzes Black Friday customer purchase data using Excel to uncover spending patterns and demographics. It provides insights for targeted marketing strategies and sales optimization.

## Introduction 
##### Black Friday, an annual shopping event occurs after Thanksgiving has evolved into a global retail phenomenon. This day marks the start of Christmas shopping season where ecommerce companies offer high promoted sales at discounted prices. It is also the busiest shopping day of the year. Businesses prepare for this day to boost sales and attract customers.

## Scenario
##### As a data analyst working in the marketing analytics team at ALLMart Company, your role is important in interpreting patterns of customer purchase behavior during black Friday. You are tasked with finding the preferences and tendencies of our diverse customer base. Your goal is to discover insights that will not only enhance our understanding of black Friday dynamics but also discover insights that will help ALLMart tailor its offerings and services to meet the unique needs of our customers. 

## Data Collection 
#### The dataset was gotten from ![Kaggle](https://www.kaggle.com/datasets/akashpawar10/wallmart-dataset/) and, it contains the following information:
###### •	User_ID: Unique identifier for each customer.
###### •	Product_ID: Unique identifier for each product.
###### •	Gender: Gender of the customer.
###### •	Age: Age of the customer in bins.
###### •	Occupation: Occupation of the customer (masked).
###### •	City_Category: Category of the City(A,B,C).
###### •	StayInCurrrentCityYears: number of years of stay the customer has been living in their current city.
###### •	Marital_Status: Marital status of the customer.
###### •	Product_Category: Category of product purchased by the customer (masked).
###### •	Purchase: Purchase Amount in USD

##### This analysis is divided into the following stages:
###### Data cleaning, Data Exploration & Analysis, Insights, Recommendations, and Visualization.

## Data Processing & Cleaning
###### Loading the data in Excel; 

![Explore](https://github.com/AreJohn/Analyzing-Customer-Purchase-Behavior-on-Black-Friday/blob/main/assets/images/explore.PNG)
 
##### The dataset contains 10 columns and 550069 rows. The data looks good, I’ll need to work on Gender, Age and Marital_Status table so that they can be useful for analysis.

###### 1.	I used Excel's Remove duplicates feature to check for duplicates, the data did not contain duplicates.
 
![duplicates](https://github.com/AreJohn/Analyzing-Customer-Purchase-Behavior-on-Black-Friday/blob/main/assets/images/duplicates.PNG)

###### 2.	I checked for blanks, the data did not contain blanks

![blanks](https://github.com/AreJohn/Analyzing-Customer-Purchase-Behavior-on-Black-Friday/blob/main/assets/images/blanks%20.PNG)
 
##### Its time to verify the data and make sure its in the right format for analysis:
###### •	Change ‘M’ to Male and ‘F’ to Female from the Gender to the Sex column so it can be understood in data visualization 

![Male](https://github.com/AreJohn/Analyzing-Customer-Purchase-Behavior-on-Black-Friday/blob/main/assets/images/replace%20male%20.PNG)
 
###### •	Changed Marital_Status ‘0’ to Single and ‘1’ to Married in the MaritalStatus column for the same reason using IF Statement

![Marital status](https://github.com/AreJohn/Analyzing-Customer-Purchase-Behavior-on-Black-Friday/blob/main/assets/images/Marital%20status.PNG)

###### •	I created a new column called Age_Group from the Age column by replacing the age groups to Children & Teenagers, Young Adults, Adults, Middle Aged Adults, Older Adults, Young Seniors and Seniors. 

!(Age Group)[https://github.com/AreJohn/Analyzing-Customer-Purchase-Behavior-on-Black-Friday/blob/main/assets/images/Agegroup.PNG]

## Analysis 
#### These are the questions that will guide my analysis:
##### 1.	What is the average amount spent by each customer? 
##### 2.	What’s the total amount spent by customers?
##### 3.	What Gender bought more on black Friday?
##### 4.	What is the average purchase amount for different age group and how does it relate to overall average customer purchase?
##### 5.	How does marital status affect purchase?
##### 6.	What is the average purchase amount for high-value products on black Friday?
##### 7.	Is there any relationship between Stay_In_Current_City_Years and purchase?
##### 8.	How does City_Category influence customer purchase?

#### Pivot tables was used for analysis:
##### 1.	The average amount spent by each customer is $9264.

![avg spent by each customer](https://github.com/AreJohn/Analyzing-Customer-Purchase-Behavior-on-Black-Friday/blob/main/assets/images/avg%20purchase.PNG)
 
##### 2.	The total amount spent by customers was $5,095,812,742.

![total purchase](https://github.com/AreJohn/Analyzing-Customer-Purchase-Behavior-on-Black-Friday/blob/main/assets/images/sum%20purchase.PNG)
 
##### 3.	Males bought more on black Friday accounting for 80% of total purchase. This suggests that gender plays an important role in purchases.

![purchase by sex](https://github.com/AreJohn/Analyzing-Customer-Purchase-Behavior-on-Black-Friday/blob/main/assets/images/what%20gender%20bought%20more.PNG)
 
##### 4.	Average Purchase gradually increases across age groups with children spending the least at $8933 and young seniors spending the most at $9535. Interestingly, all age groups expect *Middle Aged Adults, Seniors and Young Seniors* spend *below the overall purchase average*.

![purchase by age group](https://github.com/AreJohn/Analyzing-Customer-Purchase-Behavior-on-Black-Friday/blob/main/assets/images/Overall%20Average%20Purchase%20for%20agegroups.PNG)
 
##### 6.	Single customers spent more than married customers accounting for 59% of purchase.

![purchase by marital status](https://github.com/AreJohn/Analyzing-Customer-Purchase-Behavior-on-Black-Friday/blob/main/assets/images/sum%20of%20purchase%20married%20vs%20single.PNG)
 
##### 8.	The criteria I used to get high-value products are the top 10 products by purchase. I filtered the top 10 products with the highest average and I used AVERAGE formula to find the average. 
##### The average purchase amount for high-value products is $14,513.

![High Value Products](https://github.com/AreJohn/Analyzing-Customer-Purchase-Behavior-on-Black-Friday/blob/main/assets/images/high%20volume%20products%20.PNG)

##### 7.	Generally, Black Friday spending tends to decrease with longer city residency , except customers who spent less than a year who had the least purchase and customers who spent a year had the highest purchase.
 
![City residency](https://github.com/AreJohn/Analyzing-Customer-Purchase-Behavior-on-Black-Friday/blob/main/assets/images/stay%20in%20current%20city%20years%20.PNG)

##### 8.	To determine how City_Category influence customer purchase, I started by finding the number of customers in different cities 

![City population](http://github.com/AreJohn/Analyzing-Customer-Purchase-Behavior-on-Black-Friday/blob/main/assets/images/population%20of%20customers.PNG)
 
##### city B had the highest population of customers. This city is likely a metropolitan area with high economic development.

##### city C had a smaller population as compared to city B. This city is likely an urban area.

##### city A had the least population of customers. This city is likely a small city or town with less economic development and infrastructure compared to other cities.

##### I then found the sum of purchase by city
 
##### Customers from city A had the least amount of purchase followed by customers in city C and customers from city B had the highest overall purchase. This suggests that city category influences customer purchase, this may be attributed to factors such as closeness to warehouse or competition.

![purchase by city](https://github.com/AreJohn/Analyzing-Customer-Purchase-Behavior-on-Black-Friday/blob/main/assets/images/purchase%20by%20city.PNG)

## Insights 
##### 1.	The number of customers that participated in this edition of black Friday was 550,069.
##### 2.	The average amount spent by each customer is $9264.
##### 3.	The total amount spent by customers was $5,095,812,742.
##### 4.	Average Purchase gradually increases across age groups with children spending the least at $8933 and young seniors spending the most at $9535. Interestingly, all age groups expect Middle Aged Adults, Seniors and Young Seniors spent below the overall average purchase.
##### 5.	Single customers spent more than married customers accounting for 59% of purchase.
##### 6.	The average purchase amount for high-value products is $14,513, this indicates that customers are willing to spend more for premium products, providing an opportunity for targeted marketing.
##### 7.	The longer a customer stays in their current city in years the less they spend on black Friday except customers who spend less than a year who spent the least and customers who spend exactly a year had the highest purchase. This indicates that the number of years a customer spends in their city plays an important role in purchase.
##### 8.	City B leads in both population and purchase, city C follows with a smaller population and spending, while city A had the least population and purchase.

## Recommendations
##### 1.	Age Group Segmented Campaigns: Tailor marketing campaigns to cater specifically to age groups that spend below the overall average. More analysis needs to be done to identify products and deals that resonate with their preferences.
##### 2.	Family-Centric Promotions to Boost Spending: Introduce family-centric promotions and deals to encourage increased spending among Married customers as it is a market segment with potential.  Highlight packages that cater to family needs and convenience. 
##### 3.	Loyalty Programs for Single Customers: Develop and promote loyalty programs to reward and retain single customers enhancing their overall shopping experience and encouraging repeat business.
##### 4.	Premium Products Promotion: Since customers are willing to spend more for premium products, intensify marketing efforts emphasizing their unique features and benefits. 
##### 5.	Residence Duration Incentives: Introduce incentives for customers with shorter residence durations, aiming to boost spending in this demographic. Consider loyalty programs that offer advantages for both short -term and long-term customers.
##### 6.	City-Specific Strategies: More data needs to be collected to determine how the distance from home to store in various cities to affects purchase. Develop marketing strategies to address the varying population sizes and spending patterns. Implement targeted promotions in areas with lower customer engagement to boost participation and sales. 


## Dashboard
![dashboard](https://github.com/AreJohn/Analyzing-Customer-Purchase-Behavior-on-Black-Friday/blob/main/assets/images/dashboard%20final.PNG) 


