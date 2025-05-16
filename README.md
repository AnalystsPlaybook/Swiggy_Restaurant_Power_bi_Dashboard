# Swiggy_Restaurant_Power_bi_Dashboard
An interactive Power BI dashboard analyzing Swiggy restaurant performance metrics like orders, ratings, revenue, and delivery trends.

  First : 
🛠 Tools Used
Power BI Desktop – For data modeling and dashboard creation

Power Query – For data cleaning and transformation

DAX – For calculated columns and measures

Excel/CSV – As initial data source(s)

   Second :
Key KPIs (Main Metrics) : 
KPI Name	:       Formula / Basis	Insight it Gives
Total Restaurants	
Count of unique Restaurant  :   How many restaurants are listed
Average Price	
Average of Price  :   Typical cost of a meal
Average Rating	
Average of Avg ratings	:   Quality score from customers
Total Ratings Count	
Sum of Total ratings	:   Total feedback volume
Average Delivery Time	
Average of Delivery time  :    Efficiency of delivery across areas or restaurants
Top-Rated Restaurants	
Based on Avg ratings	:   Best performers
Most Rated Restaurants	
Based on Total ratings	:     Popular or frequently ordered from
Most Expensive Restaurants	
Based on Price	:   Premium-priced food outlets
Food Type Distribution	
Count by Food type   :      Cuisine spread (e.g., Indian, Chinese, etc.)

  Third : 
Visuals for Dashboard : 
Visual Type   ||  What to Show	 ||   Based On
Bar Chart	|| Top 10 restaurants by avg rating ||	Restaurant, Avg ratings
Column Chart	|| Total ratings per city	|| City, Total ratings
Map	||  Restaurants per area with average rating ||	Address / Area
Donut/Pie Chart	 ||  Food type distribution  ||  Food type
Line Chart	||  Average delivery time per area ||  Area, Delivery time
Table/Matrix	||  List of restaurants with price, rating, time ||  Restaurant, Price, Avg ratings, Delivery time

   And the last The "Slicers" & "Filters" : 
Advanced Insights:
Top Restaurants per City  ||	Use City as a slicer and show top 5 restaurants by rating or orders.
Delivery Time Heatmap ||  Show which areas are slower/faster for delivery.
Price vs Rating Correlation  ||  Scatter chart to see if higher prices relate to better ratings.

📌 Measures Needed for KPIs in Swiggy Restaurant Power BI Dashboard:
1. Total Restaurants
Measure Needed: Count of distinct restaurants
DAX Formula: Total Restaurants = DISTINCTCOUNT('Table'[Restaurant])

2. Average Price
Measure Needed: Average of the price column

DAX Formula: Average Price = AVERAGE('Table'[Price])

3. Average Rating
Measure Needed: Average of average ratings

DAX Formula: Average Rating = AVERAGE('Table'[AvgRating])

4. Total Ratings Count
Measure Needed: Sum of all ratings

DAX Formula: Total Ratings = SUM('Table'[TotalRatings])

5. Average Delivery Time
Measure Needed: Average of delivery time

DAX Formula: Avg Delivery Time = AVERAGE('Table'[DeliveryTime])

6. Top-Rated Restaurants
Measure Needed: Based on Average Rating measure

Implementation Tip:
Use a TopN visual filter on the Average Rating measure to highlight top-rated restaurants.

7. Most Rated Restaurants
Measure Needed: Based on Total Ratings measure

Implementation Tip:
Use a TopN visual filter on the Total Ratings measure to identify restaurants with the most reviews.

8. Most Expensive Restaurants
Measure Needed: Based on Average Price measure

Implementation Tip:
Use a TopN visual filter on the Average Price to showcase the priciest restaurants.

9. Food Type Distribution
Measure Needed: Count by food category

DAX Formula: Food Count = COUNT('Table'[Restaurant])

Visualization Tip:
Place Food Type in the visual axis (e.g., Pie or Bar Chart) to show distribution.
