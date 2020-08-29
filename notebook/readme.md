# (Ford GoBike System Data Exploration)
## by (Mohamed Sayed Elaraby)


## Dataset

> GoBike Data is a dataset for bike trips happened on Febraury 2018, Each trip is anonymized and includes:-
- Trip Duration (seconds).
- Start Time and Date.
- End Time and Date
- Start Station ID.
- Start Station Name.
- Start Station Latitude.
- Start Station Longitude.
- End Station ID.
- End Station Name.
- End Station Latitude.
- End Station Longitude.
- Bike ID.
- User Type (Subscriber or Customer – “Subscriber” = Member or “Customer” = Casual).

> data source: https://www.lyft.com/bikes/bay-wheels/system-data

> befor we start our exploration we made some data wrangling:-
- convert start_time, end_time from object to pandas Datetime.
- convert user_type from object to category.
- extract month, dayofweek and hour from the start_time and save them in separate columns.

## Summary of Findings

> during my exploration of the dataset I found that:-
- the duration (seconds) distribution seems to be normally after using 'log' scale 
and the most common values almost in the range of 200:2K seconds.
- the subscriber type is the most common user type.
- all data has been recorded at Febraury, 2018.
- bikers prefer to bike at these days of week Tuesday, Thursday, Wednesday.
- bikers prefer to bike at 8 AM, 5 PM hours of the day.
- although the number of subscriber is greater than number of customer, the average customer duration of biking is higher than subscriber.
- Saturday and Sunday have the highest average duration of biking compared to other days of week.
- Saturday has the most bikers in customer type.
- Tuesday, Wedensday, Thursday has the most bikers in subscriber type.
- 12 PM, 3 PM, 4 PM, 5 PM has the most bikers in customer type.
- 8 AM and 5 PM has the most bikers in subscriber type.
- for customer type 3 AM, 4 AM the duration of biking is longer than any hour.
- for subscriber type 2 AM, 3 AM the duration of biking is longer than any hour.
- during all days of week the median (duration) of customer type is higher than the median (duration) of subscriber type.

## Key Insights for Presentation

- the distribution of duration (seconds) seems to be  normally distributed.
- the median duration of cutomer type is higher than median duration of subscriber type.
- Tuesday, Thursday, Wedensday have the most bikers in the week (you should provide enough number of bikes in these days).
- 8 AM and 5 PM is the most hours have bikers in the day (you should provide enough number of bikes in these hours).

## Resources

- https://docs.python.org/2/library/datetime.html#strftime-strptime-behavior
- https://intellipaat.com/community/5151/how-do-i-extract-the-date-year-month-from-pandas-dataframe 
- https://matplotlib.org/tutorials/intermediate/constrainedlayout_guide.html#sphx-glr-tutorials-intermediate-constrainedlayout-guide-py 