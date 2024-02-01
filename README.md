# Housing Rental Analysis for San Francisco
# Instructions
Use the san_francisco_housing.ipynb notebook to visualize and analyze the real-estate data.

Note that this assignment requires you to create a visualization by using hvPlot and GeoViews. Additionally, you need to read the sfo_neighborhoods_census_data.csv file from the Resources folder into the notebook and create the DataFrame that you’ll use in the analysis.

The main task in this Challenge is to visualize and analyze the real-estate data in your Jupyter notebook. Use the san_francisco_housing.ipynb notebook to complete the following tasks:

* Calculate and plot the housing units per year.

* Calculate and plot the average prices per square foot.

* Compare the average prices by neighborhood.

* Build an interactive neighborhood map.

* Compose your data story.

# Calculate and Plot the Housing Units per Year
1. Use the groupby function to group the data by year. Aggregate the results by the mean of the groups.

2. Use the hvplot function to plot the housing_units_by_year DataFrame as a bar chart. Make the x-axis represent the year and the y-axis represent the housing_units.

3. Style and format the line plot to ensure a professionally styled visualization.

4. Answer the following question:
* Question: What is the overall trend in housing_units over the period being analyzed?
* Answer: Housing_units steadly increased between 2010 and 2016 at a rate of 1900 to 2000 per year

# Calculate and Plot the Average Sale Prices per Square Foot
1. Group the data by year, and then average the results. What’s the lowest gross rent that’s reported for the years that the DataFrame includes?

2. Create a new DataFrame named prices_square_foot_by_year by filtering out the “housing_units” column. The new DataFrame should include the averages per year for only the sale price per square foot and the gross rent.

3. Use hvPlot to plot the prices_square_foot_by_year DataFrame as a line plot.
Hint This single plot will include lines for both sale_price_sqr_foot and gross_rent.

4. Answer the following questions:
* Question 1: Did any year experience a drop in the average sale price per square foot compared to the previous year?
* Answer 1: There was a small drop in average sale price per square foot from 2010-2011.
* Question 2: If so, did the gross rent increase or decrease during that year?
* Answer 2: Gross rent increased from 2010-2011.

# Compare the Average Sale Prices by Neighborhood
1. Create a new DataFrame that groups the original DataFrame by year and neighborhood. Aggregate the results by the mean of the groups.

2. Filter out the “housing_units” column to create a DataFrame that includes only the sale_price_sqr_foot and gross_rent averages per year.

3. Create an interactive line plot with hvPlot that visualizes both sale_price_sqr_foot and gross_rent. Set the x-axis parameter to the year (x="year"). Use the groupby parameter to create an interactive widget for neighborhood.

4. Answer the following question:
* Question: For the Anza Vista neighborhood, is the average sale price per square foot for 2016 more or less than the price that’s listed for 2012?
* Answer: The average sale price per square foot in 2016 is about $256 less, compared 2012.

# Build an Interactive Neighborhood Map
1. Read the neighborhood_coordinates.csv file from the Resources folder into the notebook, and create a DataFrame named neighborhood_locations_df. Be sure to set the index_col of the DataFrame as “Neighborhood”.

2. Using the original sfo_data_df Dataframe, create a DataFrame named all_neighborhood_info_df that groups the data by neighborhood. Aggregate the results by the mean of the group.

3. Review the two code cells that concatenate the neighborhood_locations_df DataFrame with the all_neighborhood_info_df DataFrame. Note that the first cell uses the Pandas concat function to create a DataFrame named all_neighborhoods_df. The second cell cleans the data and sets the “Neighborhood” column. Be sure to run these cells to create the all_neighborhoods_df DataFrame, which you’ll need to create the geospatial visualization.

4. Using hvPlot with GeoViews enabled, create a points plot for the all_neighborhoods_df DataFrame. Be sure to do the following:
* Set the geo parameter to True.
* Set the size parameter to “sale_price_sqr_foot”.
* Set the color parameter to “gross_rent”.
* Set the frame_width parameter to 700.
* Set the frame_height parameter to 500.
* Include a descriptive title.

5. Answer the following questions:
* Question 1: How does the trend in rental income growth compare to the trend in sales prices? Does this same trend hold true for all the neighborhoods across San Francisco?
* Answer 1: The tred is that rental income has increased while sales price has remained somewhat stagnant with minimal inscreases. There are some neighborhoods that have seen slight drcreases in sales price but they are exceptions. For example, Union Square does show a higher growth of sales prices in comparison to other neighborhoods and rental income growth.
* Question 2: What insights can you share with your company about the potential one-click, buy-and-rent strategy that they're pursuing? Do neighborhoods exist that you would suggest for investment, and why?
* Answer 2: The one-click & buy-and-rent strategy will be successful in San Francisco. I would reccomend investing in areas that don't have recent decreases in either metric. However, this data is not considering Covid-19 in which these predictions does not consider the potential housing market coming to a hault in 2020.

# Compose Your Data Story
Based on the visualizations that you have created, compose a data story that synthesizes your analysis by answering the following questions:

Question 1: How does the trend in rental income growth compare to the trend in sales prices? Does this same trend hold true for all the neighborhoods across San Francisco?
Answer 1: The tred is that rental income has increased while sales price has remained somewhat stagnant with minimal inscreases. There are some neighborhoods that have seen slight drcreases in sales price but they are exceptions. For example, Union Square does show a higher growth of sales prices in comparison to other neighborhoods and rental income growth.

Question 2: What insights can you share with your company about the potential one-click, buy-and-rent strategy that they're pursuing? Do neighborhoods exist that you would suggest for investment, and why?
Answer 2: The one-click & buy-and-rent strategy will be successful in San Francisco. I would reccomend investing in areas that don't have recent decreases in either metric. However, this data is not considering Covid-19 in which these predictions does not consider the potential housing market coming to a hault in 2020.

# Resources 
## In Class Activites 
* https://git.bootcampcontent.com/University-of-California---Berkeley/UCB-VIRT-FIN-PT-12-2023-U-LOLC/-/blob/main/05-APIs/Class_2_Activities/04-Ins_Alpaca_Demo/Solved/alpaca-demo.ipynb?ref_type=heads
* https://git.bootcampcontent.com/University-of-California---Berkeley/UCB-VIRT-FIN-PT-12-2023-U-LOLC/-/blob/main/05-APIs/Class_2_Activities/05-Stu_Investment_Value/Solved/investment-value.ipynb?ref_type=heads

## Tutors & Peers 
### Tutor Meetings through FINTECH Bootcamp:
* Vijaya
- Tuesday 1/23/2024
- Wednesday 1/31/2024

### Tutor Meetings External Resources:
* Edward R.
* Website: https://www.edwardrees.info
- Sunday 1/28/2024
 
### Study Partner taking FINTECH Bootcamp (Same Class):
* German Romero
- Helped eachother fix code errors
- Cross Referenced work to help eachother understand why we are using a specific code and understand what the question is asking us for