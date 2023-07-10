## Practical Application Assignment 5.1

### Will the Customer Accept the Coupon?

In this exercise, we analyze data/coupons.csv (from the UCI Machine Learning repository) which contains data collected from a survey
on Amazon's Mechanical Turk.  

The survey describes different driving scenarios, including the destination, current time, weather, passenger, etc, and then asks people 
whether they will accept the coupon if they are the driver. 

Answers given that the users will drive there “right away” or “later before the coupon expires” are labeled as “Y = 1”, 
and answers “no, I do not want the coupon” are labeled as “Y = 0”. 

There are five different types of coupons—less expensive restaurants (under $20), coffee houses, carry out and take away, bars,
and more expensive restaurants ($20–$50).

Details [Notebook](./Mauricio_prompt.ipynb)

### Summary of Exploratory Analysis 

- Checked the dataset for null columns and found 6 columns. Decide to dropped the car column because it had over 99 percent of nulls data. 
  The other 5 columns had less than 1.5 percent which consider to keep it. 

- For the cases when there are missing values, decide to represent those as 'never' to fill those gaps. Hopefully is the right call here, since is very low percentage

- Temperature might be one of variable that effect some acceptance of the coupon since will depends how comfortable the driver is to be outside. 
  This can be note in the histogram from temperature going from 80 the most common, then 50 and finally 30

- Found out that from the total population of coupons, the 56 % decide to accept the coupons in comparison with 43.2 % 

- The most common type of coupons in order of volume are the followings: "Coffee House", "Restaurant < 20", "Carry Out & Take Away", "Bar", "Restaurant (20 - 50)"

- The proportion of Bar coupon accepted ratio was about 41 percent

- The proportion of Bar coupon accepted for people than went there 3 or less visits was 37.1 percent versus 76.9 percent with those who went more than 3 times.

- Acceptance rate between drivers who go to a bar more than once a month and are over the age of 25 to the all others, 
  for those the the difference between 69.5 % and 41 % between the acceptance rate of the coupon is significant, 
  which means that the age of the customer is a factor in the acceptance of the coupon.

- Customer acceptance coupon for going to the bar with more than one per month and did not have any kids and not widowed is 71.3 %

- Customer acceptance coupon for going to the bar with more than once and below 30 years old is similar trend to 72 %

- Customer acceptance coupon for going to cheap restaurants more than 4 times and incomes less than 50 k is 69 %
    
- Customer prefer cheaper restaurants and normally goes from 1 to 8 times.

- Bars is also very common for people that is younger than 30 years old and also do not have kids, which in reality seems to be a valid case

### Independent Investigation

- Customer accepted coffee house coupons in the morning at 10AM and also in the afternoon at 2PM.

- Customer accepted restaurant coupons for < $20 at 2PM and 6PM.

- Customer accepted mostly carry out at 7AM and 10PM which were the earliest and latest times outside of traditional dine in hours

- Mostly drivers accepted coupons that were for carry out and restaurants(< $20)

- Low to middle income earners were more likely to accept coupons

- Younger adults are more likely to accept coupons.