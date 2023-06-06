# capital_bike_share_analysis
collaberative project regarding use of bike share data and conducive analysis 

Introduction
This project is designed to analyze usage of Capital Bikeshare during the initial recovery period from the restrictions set by Washington, DC in response to the COVID-19 pandemic. Specifically, looking into ridership across 2021 and 2022 to see what user behavior looks like and to visualize what has changed when it comes to ridership during this recovery timeframe. 

We were keenly interested to review what impact, if any, that continued work from home has had on user behavior during 2021 and 2022:

Has ridership increased or decreased during this post pandemic timeframe?
Was ridership primarily for commuting to and from work or casual after work and on weekends?
What are the differences between members and non-members when it comes to overall usage?
Does the time of year (season) have an impact on ridership?
What are the popular areas where rides begin and end?

What is Bike Sharing?

The first bike sharing projects were initiated by various sources, such as local community organizations, charitable projects intended for the disadvantaged, as a way to promote bicycles as a non-polluting form of transportation – and bike-lease businesses.

The earliest well-known community bicycle program was started in the summer of 1965 in Amsterdam. Fifty bicycles were painted white and placed unlocked around Amsterdam for everyone to freely use for one trip and then to be left for the next rider.  Within a month, most of the bikes had been stolen and the rest were found in nearby canals.

The concept of bike sharing systems is simple enough: it is a shared micro mobility service for short term bike rentals where users typically pay a small fee to unlock a bike either located at a designated docking station or is securely locked to a designated bicycle post. Additionally, with modern bike share systems there are now dockless bikes which do not require a docking station or to be locked to a permanent structure, as they are self-locking. 

While it took time to develop the current modern version of bike share, mostly due to the need for better technology to develop that allows for the wide range of docked and dockless bikes. Also, with the advancement of technology has allowed the introduction of electric or e-assist bikes to bike share fleets.

About our Data

In order to develop our analysis, we sourced usage data directly from Capital Bikeshare via their publicly available ride data for calendar years 2021 and 2022. We sourced weather data from weathermap.org to look at how it may impact ridership. Also, Google Maps API was used to determine the geographic locations of rides start and end points.

For the data from Capital Bikeshare, we merged 12 files each fro 2021 and 2022 into match datasets. From there we were able to pull out specific data points to work through this analysis.


Analysis of Questions

After some cleaning of the data to allow for us to extract the needed data points we proceeded to develop the needed visualizations to review our data.

Has ridership increased or decreased during this post pandemic timeframe?
Analysis was performed to view what lingering impact, if any, on bikeshare usage existed in 2021 and into 2022. Specific interest in how the lifting of restrictions in Q2 2021, coupled with the availability of the COVID-19 vaccines impacted usage.  Based on a review of the data provided by Capital Bikeshare overall there were 2.75 million unique rides in 2021 vs. 3.48 million unique rides in 2022, which is a 26% increase year over year.  This would suggest that the restrictions along with vaccine availability may have played a role in lowering the number of riders, prior to the said restrictions being lifted and vaccine availability being opened to those outside of high risk groups, both of which started in May 2021.

Was ridership primarily for commuting (9am to 5pm Monday-Friday) or casual (outside of business hours and on weekends)?  What, if any, impact does membership with Capital Bikeshare have vs. non-members?
Analysis was performed to determine if COVID 19 protocols being removed halfway through 2021 affected the shift of bikeshare usage during weekday work hours between 2021 and 2022. Based on our analysis, ridership was primarily for commuting during weekdays in the time range of 6:00 AM to 6:00 PM. Rides by casual (non member) riders were much longer on average than those taken by members during these days and times. From this it can be inferred that members are mostly using the bikeshare to commute to and from work, while casual riders are using the bikeshare more for leisure. Casual membership actually increased 2% in 2022, but overall there was not a major shift in bike usage from year to year. In order to account for the fact that most businesses were fully open in late 2021, calculations were made to determine if there were less member rides from January-April 2021 (the COVID vaccine was made available to everyone in May 2021). There also was very little difference between the percentage of casual rides to member rides when 2021 was split based on vaccine availability. There are a few different conclusions that can be made from this. The work from home structure could have potentially been a culture shift that stuck in 2022 after COVID protocols were removed. Another idea could be that the demographic of people who used the bikeshare to commute to work might have been those whose jobs were not remote at any point in 2021. Most likely, a combination of both hypotheses can be used to explain the lack of difference in bike usage between 2021 and 2022 during work hours.

Where do rides begin and where do they end?
To answer the question which stations were most popular, a filter of weekdays was set and another a range of time 6-6pm to see whether working from home perhaps changed the ridership. From our large csv data file I got the counts of start and ending stations for both 2021 and 2021. I created a new DF that included what I needed, such as starting and ending latitude and long, starting station address ending station address.I got the max and min counts of the counts for each station then placed the counts into bins per station. In 2021 there were 55 starting stations that had above 10K hits in popularity. In 2021 there were 58 ending stations that had above 10K hits in popularity. In 2022 there were 13 starting stations that had above 10k hits in popularity. In 2022 there were  30 ending stations that had above 10K hits in popularity. Our findings conclude that ridership has changed from 2021 to 2022. In 2021 employers did try to bring employees back to work, however with the hiring spree, it's likely an incentive was to work from home which can explain the trend in 2022.

Does the weather have an impact on ridership?
People are most likely to ride their bikes in sunny weather, for longer periods of time.
People are still likely to ride their bikes in cloudy weather, but for shorter periods of time.
People are least likely to ride their bikes in rainy weather, for the shortest periods of time.
These findings could be used to inform decisions about how to promote bike share usage. For example, bike share programs could focus on marketing their services to people who live in areas with sunny weather. Additionally, bike share programs could consider offering discounts or incentives to people who ride their bikes in rainy weather                                                                                                                                                                   

*The number of bike rides in 2021 was significantly affected by weather conditions. There were more rides on sunny days than on cloudy or rainy days. The number of rides was highest on clear days, with an average of 100 rides per day. The number of rides was lowest on rainy days, with an average of 50 rides per day.


Data Sources & Resources:
Capital Bikeshare Ride Data: https://s3.amazonaws.com/capitalbikeshare-data/index.html
Weather Data: http://weathermap.org/
Google Maps API: https://mapsplatform.google.com/maps-products/?_gl=1*wgsu3n*_ga*Mjk2MzMyMTY2LjE2ODYwMTYxODY.*_ga_NRWSTWS78N*MTY4NjAxNjE4Ni4xLjAuMTY4NjAxNjE5MC4wLjAuMA
Historical info of Bikeshare systmes: https://en.wikipedia.org/wiki/Bicycle-sharing_system
For Code Troubleshooting: https://www.useblackbox.io/
For Code Troubleshooting: Python for Data Analysis: Data Wrangling with pandas, NumPy & Jupyter 3rd Edition (https://wesmckinney.com/book/)


