# Take-Home-Challenge-Ultimate-Technologies-Inc.

# Part 1. Exploratory Data Analysis

The attached logins.json file contains (simulated) timestamps of user logins in a particular geographic location. Aggregate these login counts based on 15minute time intervals, and visualize and describe the resulting time series of login counts in ways that best characterize the underlying patterns of the demand. Please report/illustrate important features of the demand, such as daily cycles. If there are data quality issues, please report them.


![image](https://user-images.githubusercontent.com/86930309/218026384-08458b14-e8b1-4576-83c6-833a6ea3225b.png)

This graph shows us that usage is highest in 22nd hour/10pm. The logins are high in the early morning from the 0-4 hour/12-4am. Then declines in the morning from 5-8am. It increase gradually from 9-11am then declines from 11am-5pm. It starts to rise from 5pm to 10pm. Peak hours are late at night and very early in the morning as well as midday.

![image](https://user-images.githubusercontent.com/86930309/218025974-3fd99884-02bc-4a5d-a208-3d5caef53312.png)

Here we can see that logins increase as the week goes on. There is a small drop off on Sundays.

# Part 2. Experiment and Metrics Design

The neighboring cities of Gotham and Metropolis have complementary circadian rhythms: on weekdays, Ultimate Gotham is most active at night, and Ultimate Metropolis is most active during the day. On weekends, there is reasonable activity in both cities.

However, a toll bridge, with a two way toll, between the two cities causes driver partners to tend to be exclusive to each city. The Ultimate managers of city operations for the two cities have proposed an experiment to encourage driver partners to be available in both cities, by reimbursing all toll costs.

**A. What would you choose as the key measure of success of this experiment in encouraging driver partners to serve both cities, and why would you choose this metric?**

The key measurement of success would be to see if it is beneficial to customers and drivers to serve both cities. I would measure three variables to see if the experiment is worth it:

- If it reduces wait times for customer
- Increases profit for the drivers
- Is it worth it for the city to reimburse the drivers for the toll

These three variables are the most valuable aspects of the experiment. The most important element to customers is convenience of obtaining a ride and the city wants happy customers and less congestion on their roads. The drivers are potentially interested in making more money by spending time in a different city. The city wants to know if it is worth it to pay the tolls by sending drivers across the bridge.

**B. Describe a practical experiment you would design to compare the effectiveness of the proposed change in relation to the key measure of success. Please provide details on how you will implement the experiment**

We would implement this by conducting an A/B test. We would collect data from drivers, tolls, and customers from before and after the experiment and compare them. We would compare average wait times before and after the change. Also to compare profits as well before and after the experiment. Lastly, we could look at the data on the tolls each city paid for the drivers and compare it to reduced traffic during peak hours and customer ratings before and after.

**C. What statistical test(s) you will conduct to verify the significance of the observation:**

We would do a null hypothesis test on the three variables to verify the significance of the observation. Our null hypothesis would be that nothing has changed by paying for the drivers tolls by serving both cities. This would indicate that each individual variable all had the same mean before and after the experiment. For example the mean of profits for all drivers is the same before and after. We could do a trail of 12 months for seasonal adjustments. Here we could compare the data for every month before and after. Now we would test our null hypothesis on each variable.

- For wait times: The p-value would be that a customer waited 60 seconds less not in the experiment. This is the probability that a customer waited less before the experiment. If this happened less than 5% of the time then we can reject the null hypothesis and it is highly unlikely to happen. Then the experiment of paying for tolls and having drivers go to opposite cities is worth paying for the tolls. This is statistically significant.

- Profits: The p-value would be that the drivers made 20% more not in the experiment. This is the probability that a driver made more money before the experiment. If this happened less than 5% of the time then we can reject the null hypothesis and it is highly unlikely to happen. Then the experiment is a success and is statistically significant.

- Toll Payment: The p-value would be that the city had higher customer ratings and less traffic not in the experiment. This is the probability that customers were happier and had less wait times in traffic before the experiment. If this happened less than 5% of the time then we can reject the null hypothesis and it is highly unlikely to happen. Then the experiment is a success and is statistically significant.
- 
**D. how you would interpret the results and provide recommendations to the city operations team along with any caveats.**

If we reject each of these null hypothesis then we know that the city should continue the program. If the numbers from the data do not express an improvement they should go back to the drivers staying in their individual cities. The caveats are the quality and length of the experiment. Issues like will the drivers actually go to the opposite cities and increased traffic at certain times are a few of the issues that might come from the experiment. The city would need to work out these different issues by implementing the project as they arise.

# Part 3. Predictive Modeling

Ultimate is interested in predicting rider retention. To help explore this question, we have provided a sample dataset of a cohort of users who signed up for an Ultimate account in January 2014. The data was pulled several months later; we consider a user retained if they were “active” (i.e. took a trip) in the preceding 30 days.

We would like you to use this data set to help understand what factors are the best predictors for retention, and offer suggestions to operationalize those insights to help Ultimate. The data is in the attached file ultimate_data_challenge.json. See below for a detailed description of the dataset. Please include any code you wrote for the analysis and delete the dataset when you have finished with the challenge.
