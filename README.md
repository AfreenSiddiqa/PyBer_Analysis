# PyBer_Analysis

The analysis should contain the following:

##Overview of the analysis:
The purpose of our analysis is to create a summary dataframe that will show ride sharing data by city type(Rural,Urban & Suburban). Once we find our data we are going to create a multiple line graph that shows total weekly fares by each city type. How we first pulled our data is by using the Pandas groupby() function with the count() and sum() methods on PyBer DataFrame columns, get the total number of rides, total number of drivers, and the total fares for each city type. Then, calculate the average fare per ride and average fare per driver for each city type. Finally, we add this data to a new DataFrame, then format the columns.Using the Pandas skills and two new functions, pivot() andresample(), we created a multiple-line graph that shows the total fares for each week by city type between the months of January & April of 2019.


Deliverable 1

 using the groupby() function we created a Series of data that has the type of city as the index, then we applied the count() method to the "ride_id" column.
 using the groupby() function we created a Series of data that has the type of city as the index, then we applied the sum() method to the "driver_count" column.
 using the groupby() function we created a Series of data that has the type of city as the index, then we applied the sum() method to the "fare" column.
 we calculated the average fare per ride by city type by dividing the sum of all the fares by the total rides.
 we calculated the average fare per driver by city type by dividing the sum of all the fares by the total drivers.
 we created a PyBer summary DataFrame with all the data gathered from Steps 1-5, using the column names shown below:.
 
we created a new DataFrame with multiple indices using the groupby() function on the "type" and "date" columns of the pyber_data_df DataFrame, then apply the sum() method on the "fare" column to show the total fare amount for each date.
![image](https://user-images.githubusercontent.com/93686963/145728124-935c32ba-bd33-4d85-972b-c291d8977594.png)

Deliverable 2

Using the Pandas skills and two new functions, pivot() andresample(), create a multiple-line graph that shows the total fares for each week by city type
using the provided code snippet to reset the index. This is needed to use the pivot() function in the next step (Step 3).

 using the pivot() function to convert the DataFrame from the previous step so that the index is the "date," each column is a city "type," and the values are the "fare."

After this step, you’ll see that each cell has the total fare for the date and time, as shown in the following image.
Note: In cells where there is no fare to be summed for that row, the cell will be filled with NaNs.

![image](https://user-images.githubusercontent.com/93686963/145728251-5afb9481-cf12-4e5c-90c1-6c07c98e0979.png)


We created a new DataFrame by using the loc method on the following date range: 2019-01-01 through 2019-04-28.
using the provided code snippet to reset the index of the DataFrame from the previous step (Step 4) to a datetime data type. This is necessary to use the resample() method.
using the provided code snippet, df.info(), to check that the "date" is a datetime data type.
We created a new DataFrame by applying the resample() function to the DataFrame you modified in the previoussteps. Resample the data in weekly bins, then apply the sum() method to get the total fares for each week.
Finally, we graph the resampled DataFrame using the object-oriented interface method and the df.plot() method, as well as the Matplotlib "fivethirtyeight" graph style code snippet provided in the starter code. Annotate the y-axis label and the title, then use the appropriate code to save the figure as PyBer_fare_summary.png in our "analysis" folder. 

![PyBer_fare_summary](https://user-images.githubusercontent.com/93686963/145727816-3af80036-8ce5-4c3c-b473-02b46a5c5cac.png)

##Results: Using images from the summary DataFrame and multiple-line chart, describe the differences in ride-sharing data among the different city types.
Rural cities has the least amount of drivers, rides and total fares.
Urban cities have the most amount of drivers, rides and total fares.
Suburban cities are in the middle having the 2nd most drivers, rides and total fares.
Although Rural cities see the least amount of drivers,rides & fares the have the highest average of fare per ride and fare per driver.
Although the Urban cities command the most drivers, rides and fares they have the lowest average of fare per ride and fare per driver.

![image](https://user-images.githubusercontent.com/93686963/145728124-935c32ba-bd33-4d85-972b-c291d8977594.png)

![PyBer_fare_summary](https://user-images.githubusercontent.com/93686963/145727816-3af80036-8ce5-4c3c-b473-02b46a5c5cac.png)



Summary: Based on the results, provide three business recommendations to the CEO for addressing any disparities among the city types.
1. Hiring more drivers in rural and suburban cities or cutting down the number of drivers in urban cities This would help even out the total number of drivers and the average fare per driver in each type of city.
2. Target marketing towards rural and suburban cities. By increasing the amount of users in these areas, the total fares and the total number of rides would increase thereby      alleviating the disparity.
3.Make small charge increases or descreases based off of how many riders there are in the city during certain months

