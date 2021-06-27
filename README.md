# Data Visualization Project - Flight Dataset
## by Priyanka Krishnan

## Project Details:
> This project is divided into two major parts. 
>
>In the first part, you will conduct an exploratory data analysis on the flight dataset. You will use Python data science and data visualization libraries to explore the dataset’s variables and understand the data’s structure, oddities, patterns and relationships. The analysis in this part should be structured, going from simple univariate relationships up through multivariate relationships, but it does not need to be clean or perfect. 
>
>In the second part, you will take your main findings from your exploration and convey them to others through an explanatory analysis. To this end, you will create a slide deck that leverages polished, explanatory visualizations to communicate your results. 

## Dataset

>The dataset is from the Bureau of Transportation Statistics and can be downloaded directly from https://community.amstat.org/jointscsg-section/dataexpo/dataexpo2009.

>The downloaded files were in zip format ('bz2'). This dataset consists of flight related details like month, day of week, carriers, arrival & departure delays, and reasons for delays. For the purpose of this project I have used data from years 2006-2008 (last three years in the dataset). 

> Wrangling steps performed on the dataset:
>   
>   o Gathering data - Read CSV files that were zipped (.bz2 format) for years 2006 to 2008 into dataframes 
>   
>   o Assessing data ‐ quality & tidiness 
>
>       The few columns had different dtype across different years dataset
>
>       CarrierDelay, WeatherDelay, NASDelay, SecurityDelay and LateAircraftDelay in dataset 2008 has NaN
>       
>       Delay columns should be melted into two colums - Delay and DelayTime.
>
>   o Cleaning data
>   
>       Merging the 2006 to 2008 fixed the dtype issue
>   
>       Filled in 0's for all NaN values in 2008 dataset.
>       Melted Delay columns into Delay Type and Avg Delay for a subset of data to help plot a graph.


## Summary of Findings

#### Univariate Exploration:
>
> As part of Univariate exploration, I looked at cancellation codes, carrier codes , day of week, cancellation by month, distribution of flight departure time and arrival & departure delays distribution.
>
> It was observed that Carrier and Weather are the top two reasons of cancellation, whereas Security was the least likely reason for cancellation. 
>
>People travel most on Mondays and Fridays which seems right, to utilize the weekend. Saturday has the least number of flights booked.
>
>Top 5 months with flights scheduled are Jul, Aug, Mar, May and Jun (in the same order). The least number of flights scheduled are in Feb. This could be due to weather.
>
>Maximum flight departure happens between 6 AM to 8 PM.
>
>Most arrival delays and departure delays are between 0 to 50 minutes.

#### Bivariate Exploration:
>
>Top 5 aircraft carriers which performed worst in terms of cancellation are: MQ - Envoy Air Inc., AA - American Airlines Inc., OO - SkyWest Airlines, UA - United Airlines, Inc. and , WN - Southwest Airlines Co. The same set of 5 aircraft carriers also performed worst in arrival delays as well as departure delays (Not in the order).
>
>UA (United Airlines Inc) has the highest cancellation due to code 'A' which stands for Carriers. 
>MQ (Envoy Air Inc) has the highest cancellation due to code 'B' and 'C' which stands for Extreme Weather and NAS respectively.
>XE (Delux Public Charter LLC dba JSX Air) has the highest cancellation due to code 'D' which stands for Security
>
>Dec, Feb, Jan, Mar and Jun are the top 5 months with most cancellations.
>
>There was a positive correlation between departure and arrival delay.
>
>There seems to be no significant increase or decrease in average arrival delay as the distance between airports increases.
>
>TZ (ATA Airlines d/b/a ATA) has the worst percentage of carrier performance followed by NW (Northwest Airlines Inc). The best performance is for HA (Hawaiian Airlines Inc).

#### Multivariate Exploration:
>
>Weather, late aircraft and Carrier related delays contribute most to overall delays as compared to others. Security is the least probable cause of delay.
>
>The average arrival delay is between 0 to 50 minutes
>
>It doesn't look like the number of flights to a destination has any effect on average arrival delay.


## Key Insights for Presentation

>The plots shown in the presentation were chosen to tell a story on delays and cancellations. Perfomance of carriers can be inferred with these two parameters, therefore they have been explored and highlighed in the presentation. 

#### Conclusion:
>
>Cancellations are mostly due to Carrier and Weather related reasons.
>
>Top 5 worst performing aircraft carriers in terms of cancellations and delays are: MQ - Envoy Air Inc., AA - American Airlines Inc., OO - SkyWest Airlines, UA - United Airlines, Inc. and , WN - Southwest Airlines Co.
>
>UA (United Airlines Inc) has the highest cancellation due to 'Carriers'. MQ (Envoy Air Inc) has the highest cancellation due to 'Extreme Weather' and 'National Aviation System' respectively. XE (Delux Public Charter LLC dba JSX Air) has the highest cancellation due to 'Security' reasons.
>
>TZ (ATA Airlines d/b/a ATA) and NW (Northwest Airlines Inc) had the most percentage of flights delayed in years 2006 to 2008. HA (Hawaiian Airlines Inc) has the least percentage of flights delayed in years 2006 to 2008.
>
>Most of the arrival delays are in the range of 0 to 50 minutes.
>
>Weather, Late Aircraft and Carrier related delays were more significant than the other delays namely NAS and Security.
