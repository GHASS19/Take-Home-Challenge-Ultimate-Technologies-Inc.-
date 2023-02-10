# Take-Home-Challenge-Ultimate-Technologies-Inc.

Part 1. Exploratory Data Analysis

The attached logins.json file contains (simulated) timestamps of user logins in a particular geographic location. Aggregate these login counts based on 15minute time intervals, and visualize and describe the resulting time series of login counts in ways that best characterize the underlying patterns of the demand. Please report/illustrate important features of the demand, such as daily cycles. If there are data quality issues, please report them.


![image](https://user-images.githubusercontent.com/86930309/218026384-08458b14-e8b1-4576-83c6-833a6ea3225b.png)

This graph shows us that usage is highest in 22nd hour/10pm. The logins are high in the early morning from the 0-4 hour/12-4am. Then declines in the morning from 5-8am. It increase gradually from 9-11am then declines from 11am-5pm. It starts to rise from 5pm to 10pm. Peak hours are late at night and very early in the morning as well as midday.

![image](https://user-images.githubusercontent.com/86930309/218025974-3fd99884-02bc-4a5d-a208-3d5caef53312.png)

Here we can see that logins increase as the week goes on. There is a small drop off on Sundays.




Part 2. Experiment and Metrics Design

The neighboring cities of Gotham and Metropolis have complementary circadian rhythms: on weekdays, Ultimate Gotham is most active at night, and Ultimate Metropolis is most active during the day. On weekends, there is reasonable activity in both cities.

However, a toll bridge, with a two way toll, between the two cities causes driver partners to tend to be exclusive to each city. The Ultimate managers of city operations for the two cities have proposed an experiment to encourage driver partners to be available in both cities, by reimbursing all toll costs.

What would you choose as the key measure of success of this experiment in encouraging driver partners to serve both cities, and why would you choose this metric?
==> I want to investigate if the "encouraging driver partners (by reimbursing all toll costs)" is effective in servicing both cities.
The most important key measure of success will be the revenue increase for the Ultimate Inc. The higher the increased revenue, the experiment "encouraging driver partners to serve in both cities" can be considered to be more successful. Please note that the metrics are measured on before and after encouraging driver partners then the difference as the success indicator is obtained. - increased revenue: revenue (costs of toll reimbursement should be deducted)

In the aspects of the servicing both cities, we can measure the following metrics that can be regarded to as successful indicators.

increased number of available drivers: average number of available drivers when calling for the pickup,
decreased wait time: average wait time when calling for the pickup, and
increased number of trips: number of trips across the bridges.
Describe a practical experiment you would design to compare the effectiveness of the proposed change in relation to the key measure of success. Please provide details on:
a. how you will implement the experiment
==> To investigate the effectiveness of the proposed change, I would compare two groups of drivers with/without reimbursements and measure the key measures mentioned above. I would recommend dividing the drivers at random by 50% and 50% for each group, one for the drivers offered reimbursement and the other for remaining drivers continuing to operate without being reimbursed for tolls.

b. what statistical test(s) you will conduct to verify the significance of the observation

==> To verify the significance of the observation, I perform the A/B test on those two groups. I perform the t-test with a confidence level of 95%, where the null hypothesis is the reimbursing drivers for tolls does not have a statistically significant impact on Ultimate's net profits.

c. how you would interpret the results and provide recommendations to the city operations team along with any caveats.

==> If the increased revenue is positive, then it is effective to encourage driver partners by reimbursing toll costs. If the increased revenue is negative, they should not adopt the toll cost reimbursement. Even it is revealed the increased revenue is positive, the drivers have randomly chosen, and it may not be effective in all cases. We need more rigorous experiments by different variables (e.g., selecting other drivers, differnt portions, different days, etc.)

Part 3. Predictive Modeling
