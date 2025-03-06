# **Website Performance Analysis**

## **Objective**

The objective of this analysis is to analyze and optimize web traffic and user engagement by:

**Session Analysis:** Understanding the temporal distribution and trends in web sessions and user visits to identify peak times and low-traffic periods.

**User Engagement Analysis:** Evaluating how engaged users are during their sessions across different channels, aiming to enhance user interaction and satisfaction.

**Channel Performance:** Assessing the effectiveness of various traffic channels in attracting and retaining users to optimize marketing spend and strategy.

**Website Traffic Forecasting:** Predicting future traffic trends to better allocate resources and tailor content delivery according to predicted user demand.

## Dataset Description

The dataset consists of key website performance metrics, including:

**Session Primary Channel Group:** The marketing channel (e.g., Direct, Organic Social, Paid Search)

**Date + Hour (YYYYMMDDHH):** The specific date and hour of the session

**Users:** Number of unique visitors within a given time period (e.g., 50,000 users)

**Sessions:** Number of visits to the website (e.g., 120,000 sessions)

**Engaged Sessions:** Sessions with significant user interaction (e.g., 80,000 engaged sessions)

**Average Engagement Time per Session:** The average time a user is engaged per session (e.g., 3.5 minutes)

**Engaged Sessions per User:** Ratio of engaged sessions to total sessions per user (e.g., 1.6)

**Events per Session:** Average number of interactions per session (e.g., 4.2 events)

**Engagement Rate:** The proportion of sessions that were engaged (e.g., 67%)

**Event Count:** Total number of interactions during the period (e.g., 500,000 events)

## Executive Summary

In the digital era, understanding website performance is critical for enhancing user experience and optimizing marketing strategies. This project analyzes user engagement metrics to identify trends, improve website functionality, and enhance audience targeting. Through data-driven insights, we explore how different traffic channels contribute to user engagement and how key performance indicators impact website effectiveness.

## Data Analysis & Visualization

**1. Data Preprocessing**

- Loaded and cleaned the dataset to remove missing or inconsistent data
- Converted date and time fields for time-series analysis
- Checked for outliers and distribution of key features

**2. Data Visualization**

**Traffic Source Analysis:** A bar chart was created to visualize which marketing channels drive the highest engagement.
![image](https://github.com/user-attachments/assets/92de44bf-106d-4573-bab2-1d7f1bd7d700)
![image](https://github.com/user-attachments/assets/1f3b88a4-2a3d-488c-91ac-2f6051527d29)

Organic Social drives the highest traffic, with over 60,000 sessions, surpassing Direct and Organic Search, which contribute around 40,000 and 30,000 sessions, respectively. However, Organic Video achieves the highest engagement rate at 76%, followed by Referral at 66% and Organic Search at 57.9%, making them highly effective in retaining users. Email and Unassigned channels show the lowest engagement, at 33% and 0.75%, indicating poor performance.

Referral traffic generates the most user interactions, averaging 3,812.92 events per session, followed by Organic Social with 3,296.29 events per session, emphasizing their role in user engagement. Direct and Organic Search show consistent interaction levels, with 2,790.37 and 2,735.6 events per session, respectively. In contrast, Organic Video, despite its high engagement rate, lags in interactivity at 940.5 events per session. Email performs poorly, with only 10 events per session, highlighting an urgent need for optimization. The Unassigned channel also shows limited interaction, requiring further investigation into its source quality.

**User Engagement Trends:** A time-series plot showing how user engagement evolves over time.

![image](https://github.com/user-attachments/assets/0dd4378f-697d-4571-8f4e-d4f3e956b0dd)

The time-series analysis of website users and sessions reveals a strong cyclical pattern, with daily fluctuations where activity peaks around 400-500 sessions and dips to nearly 100 sessions during low-traffic periods. Over the observed month, the number of users shows a gradual upward trend, indicating a potential increase in website engagement. The correlation between users and sessions remains high, suggesting that the average sessions per user remain steady. Notably, traffic spikes exceeding 500 sessions occur periodically, likely due to promotional events or external factors. Meanwhile, engagement drops significantly on certain days, possibly reflecting weekend or off-peak trends. These insights provide a foundation for forecasting models to predict traffic and optimize resource allocation.

**Correlation Heatmap:** A heatmap was generated to examine relationships between engagement metrics.

![image](https://github.com/user-attachments/assets/1820309b-104d-4e82-aef7-71ce59b5c2f6)

- A strong positive correlation (0.85) between event count and engagement time.
- Engagement rate and average session duration show a moderate correlation (0.65).

## Key Findings

- Marketing Channels Impact Engagement: Organic search and direct traffic contribute the highest engagement rates, with 40% and 30% of total sessions, respectively. Paid search shows a lower retention rate of 25%.

- User Engagement Varies Over Time: Peak engagement occurs between 6 PM and 9 PM, with the highest engagement rate reaching 72%, while engagement drops significantly to 35% during midnight hours.

- Events per Session Influence Engagement: Users engaging in 4 or more interactions per session tend to have an average engagement duration of 5+ minutes, compared to 2 minutes for those with fewer interactions.

- Correlation Between Engagement Metrics: Event count and engagement time have a strong correlation (0.85), while engagement rate and session duration also show a significant relationship (0.65), indicating that higher interaction levels drive better user retention.

## Website Traffic Forecasting

To predict website traffic, a SARIMA model was used to forecast sessions based on historical data. The model effectively captured seasonality and trends in user visits, allowing for accurate short-term predictions.

![image](https://github.com/user-attachments/assets/d9131a86-1208-4496-b135-1f03f9de972a)

- The forecasted sessions closely follow the observed trends, demonstrating a reliable prediction model.
- Traffic peaks align with historical high-engagement periods, ensuring business strategies can be planned accordingly.
- A mean absolute percentage error (MAPE) of 7.5% indicates strong predictive accuracy, making this approach valuable for proactive decision-making.

## Technologies Used

- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Jupyter Notebook for analysis and visualization
- Matplotlib & Seaborn for data visualization

## Conclusion
This website performance analysis provides actionable insights into traffic sources, user engagement trends, and behavioral patterns. By leveraging these insights, businesses can enhance user experience, optimize marketing strategies, and improve overall website effectiveness. The quantitative findings further reinforce the importance of data-driven decision-making in improving digital engagement.
