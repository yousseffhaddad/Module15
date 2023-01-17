# Des Moines - Bike Sharing Project
## Overview of Project

## Download Tableau Public
First, go to the [`Tableau website`](https://public.tableau.com/en-us/s/) and enter your email. You will also be required to enter some contact information, but you can always unsubscribe from communications.

## Install Tableau Public
Once you have downloaded Tableau Public, we can start the process of installing Tableau Public. The process of installing Tableau Public is very similar to installing most other programs.

# Deliverable 1:  
## Change Trip Duration to a Datetime Format
### Deliverable Requirements:
Using Python and Pandas functions, you’ll convert the "tripduration" column from an integer to a datetime datatype to get the time in hours, minutes, and seconds (00:00:00). After you convert the "tripduration" column to a datetime dataytpe, you’ll export the DataFrame as a CSV file to use for the trip analysis in Deliverable 2.

Your final results should look similar to the following image:

![name-of-you-image](Resources/Images/s5.png?raw=true)



1. The data in the "tripduration" column is converted to a datetime datatype and has the correct time format.
2. The DataFrame is exported as a new file without the index column.

 
### Results with detail analysis:

1. **The data in the "tripduration" column is converted to a datetime datatype and has the correct time format.**


> Image with `Jupyter Notebook` & `Tableau` Code below.

**Code and Image**


````py

import pandas as pd

# 1. Create a DataFrame for the 201908-citibike-tripdata data. 
citibike_data = "201908-citibike-tripdata.csv"
citibike_df = pd.read_csv(citibike_data)

# 2. Check the datatypes of your columns. 
citibike_df.info()

# 3. Convert the 'tripduration' column to datetime datatype.
citibike_df['tripdur_orig'] = citibike_df['tripduration']
citibike_df['tripduration'] = pd.to_datetime(citibike_df['tripduration'], unit='m')
citibike_df.head()

# 4. Check the datatypes of your columns. 
citibike_df.info()
````
2. **The DataFrame is exported as a new file without the index column.**


> Image with `Jupyter Notebook` & `Tableau` Code below.

**Code and Image**


````py
# 5. Export the Dataframe as a new CSV file without the index.
citibike_df.to_csv('citibike_201908_updt.csv', index=False)

````

# Deliverable 2:  
## Create Visualizations for the Trip Analysis
### Deliverable Requirements:
Using Tableau, create visualizations that show:

  - How long bikes are checked out for all riders and genders.
  - How many trips are taken by the hour for each day of the week, for all riders and genders.
  - A breakdown of what days of the week a user might be more likely to check out a bike, by type of user and gender.

### Create the Checkout Times for Users Viz
In this visualization, you’ll graph the length of time that bikes are checked out for all riders.


### Create the Checkout Times by Gender Viz
In this visualization, you’ll graph the length of time that bikes are checked out for each gender.

### Create the Trips by Weekday for Each Hour Viz
In this visualization, you’ll graph the number of bike trips by weekday for each hour of the day as a heatmap.

### Create the Trips by Gender (Weekday per Hour) Viz
In this visualization, you’ll graph the number of bike trips by gender for each hour of each day of the week as a heatmap.

### Create the User Trips by Gender by Weekday Viz
In this visualization, you’ll graph the number of bike trips by gender for each hour for each day of the week as a heatmap.

### Deliverable 2 Requirements:

1. There is a line graph displaying the number of bikes checked out by duration for all users, and the graph can be filtered by the hour.
2. There is a line graph displaying the number of bikes that are checked out by duration for each gender by the hour, and the graph can be filtered by the hour and gender.
3. A heatmap is created showing the number of bike trips for each hour of each day of the week.
4. A heatmap is created showing the number of bike trips by gender for each hour of each day of the week, and the heatmap can be filtered by gender.
5. A heatmap is created showing the number of bike trips for each type of user and gender for each day of the week, and you can only filter by user and gender.

 
### Results with detail analysis:

1. **There is a line graph displaying the number of bikes checked out by duration for all users, and the graph can be filtered by the hour.**


> Image with `Jupyter Notebook` & `Tableau` Code below.


![name-of-you-image](Resources/Images/2.1.JPG?raw=true)



2. **There is a line graph displaying the number of bikes that are checked out by duration for each gender by the hour, and the graph can be filtered by the hour and gender.**


> Image with `Jupyter Notebook` & `Tableau` Code below.


![name-of-you-image](Resources/Images/2.2.JPG?raw=true)



3. **A heatmap is created showing the number of bike trips for each hour of each day of the week.**


> Image with `Jupyter Notebook` & `Tableau` Code below.


![name-of-you-image](Resources/Images/2.3.JPG?raw=true)

![name-of-you-image](Resources/Images/2.3.1.JPG?raw=true)



4. **A heatmap is created showing the number of bike trips by gender for each hour of each day of the week, and the heatmap can be filtered by gender.**


> Image with `Jupyter Notebook` & `Tableau` Code below.

![name-of-you-image](Resources/Images/2.4.JPG?raw=true)

![name-of-you-image](Resources/Images/2.4.1.JPG?raw=true)




5. **A heatmap is created showing the number of bike trips for each type of user and gender for each day of the week, and you can only filter by user and gender.**


> Image with `Jupyter Notebook` & `Tableau` Code below.

![name-of-you-image](Resources/Images/2.5.JPG?raw=true)

![name-of-you-image](Resources/Images/2.5.1.JPG?raw=true)




# Deliverable 3:  
## Create a Story and Report for the Final Presentation
### Deliverable Requirements:
For this part of the Challenge, you’ll create a story in Tableau and write a report that describes the key outcomes of the NYC Citibike analysis you did in the module and in Deliverable 2.

Follow the instructions below to complete Deliverable 2.

In Tableau, create a new Story using visualizations that will support the key findings you want to show.

1. You must use the five visualizations that you created in Deliverable 2.

> TABLEAU DASHBOARDS:

![name-of-you-image](Resources/Images/3.1.1.JPG?raw=true)

![name-of-you-image](Resources/Images/3.1.2.JPG?raw=true)

![name-of-you-image](Resources/Images/3.1.3.JPG?raw=true)

![name-of-you-image](Resources/Images/3.1.4.JPG?raw=true)

![name-of-you-image](Resources/Images/3.1.5.JPG?raw=true)


>TABLEAU PUBLIC URL:

 [`Final Data Analysis - Aug 2019`](https://public.tableau.com/views/Des-Moines-Bike-Sharing/FINALSTORYREPORT?:language=en&:display_count=y&publish=yes&:origin=viz_share_link). 

2. You must use at least two visualizations that you created in this module.

> TABLEAU WORKSHEET:

![name-of-you-image](Resources/Images/3.2.1.JPG?raw=true)

![name-of-you-image](Resources/Images/3.2.2.JPG?raw=true)

![name-of-you-image](Resources/Images/3.2.3.JPG?raw=true)



3. In your README markdown file, include the following:
  **Overview of the analysis:**, **Results:** & **Summary:** 
  
  - CitiBike Analysis tells that more than 80% are Subscribers, with an ~19% or regular non-subscribers, that data creates a new need, such better user experiance interaction in the future.

  ![name-of-you-image](Resources/Images/3.3.1.JPG?raw=true)


  - Total of 65% General Male use, 25% General Female with an Unknown gender that relies on non-subscribers users. In addition, Peak by Gener spike on same time frame, and Top 10 Start and Ending locations are on same zone (that's really good!)

  ![name-of-you-image](Resources/Images/3.3.2.JPG?raw=true)

  ![name-of-you-image](Resources/Images/3.3.3.JPG?raw=true)


  - Inventory Use and Maintenance may be an issue in the future, locations are different time to time.

    ![name-of-you-image](Resources/Images/3.3.4.JPG?raw=true)

    ![name-of-you-image](Resources/Images/3.3.5.JPG?raw=true)

>TABLEAU PUBLIC URL:

 [`Final Data Analysis - Aug 2019`](https://public.tableau.com/views/Des-Moines-Bike-Sharing/FINALSTORYREPORT?:language=en&:display_count=y&publish=yes&:origin=viz_share_link). 
