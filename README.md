# Hotel-booking-cancellation-analysis
Hotel booking cancellation analysis and interactive dashboard using Microsoft Excel
# Hotel Booking Cancellation Analysis Using Excel

## Project Overview

This is my first Data Analytics project, developed using Microsoft Excel. The main objective of this project is to analyze hotel booking cancellations and explore cancellation patterns across different categories, including guest type, hotel type, month, room assignment status, and arrival year.

The project involves data categorization using Excel formulas, PivotTable analysis, data visualization, and an interactive dashboard with a Year Slicer.

## Project Objectives

* Analyze hotel booking and cancellation patterns.
* Compare cancellations across different guest categories.
* Explore cancellations by hotel type and month.
* Investigate cancellation patterns for desired and undesired room assignments.
* Compare cancellations across arrival years.
* Present key metrics and insights through an interactive dashboard.

## Tools and Skills

* **Microsoft Excel**
* IF and AND functions
* Data preparation and categorization
* PivotTables
* Charts and data visualization
* KPI cards
* Slicers and interactive dashboards

## Dataset

**Source:** Kaggle — Hotel Booking Demand Dataset

Dataset link: https://www.kaggle.com/datasets/saadharoon27/hotel-booking-dataset
The dataset contains hotel booking information, including booking status, hotel type, arrival dates, guest details, and reserved and assigned room types.

## Project Workflow

### 1. Data Preparation and Categorization

After exploring the dataset, I created two additional columns based on the requirements of my analysis.

#### A. Room Status

**Purpose:** To identify whether the assigned room type matches the reserved room type.

**Excel Formula:**
=IF([@[reserved_room_type]]=[@[assigned_room_type]],"Desired","Undesired")

**Logic:**

* **Desired:** If the reserved room type matches the assigned room type.
* **Undesired:** If the reserved room type does not match the assigned room type.

This classification helps explore cancellation patterns according to room assignment status.

#### B. Guest Type

**Purpose:** To categorize bookings into Couples, Single, and Family based on the number of adults, children, and babies.

**Excel Formula:**
=IF(AND([@adults]=2,[@children]=0,[@babies]=0),"Couples",IF(AND([@adults]=1,[@children]=0,[@babies]=0),"Single","Family"))


**Logic:**

* **Couples:** Exactly 2 adults, 0 children, and 0 babies.
* **Single:** Exactly 1 adult, 0 children, and 0 babies.
* **Family:** All other combinations, including bookings with children or babies, one adult with children or babies, and bookings with more than two adults.

This categorization helps compare cancellation patterns across different guest groups.

### 2. PivotTable Analysis

I created six PivotTables to summarize and analyze booking and cancellation data.

The analysis covers:

* **Guest Type Analysis:** Total guests/bookings and cancelled bookings across Couples, Family, and Single categories.
* **Hotel Type Analysis:** Cancellation counts for Resort Hotels and City Hotels.
* **Room Status Analysis:** Total bookings and cancellations for Desired and Undesired room assignments.
* **Monthly Analysis:** Booking and cancellation patterns across the months of the year.
* **Year-wise Analysis:** Cancellation counts for 2015, 2016, and 2017.
* **Overall Booking Summary:** Total bookings and total cancellations for key performance metrics.

These summaries form the basis of the dashboard visualizations.

### 3. Interactive Dashboard

I designed an Excel dashboard to present the analysis in a clear and visual format.

**Dashboard components:**

* Total Bookings KPI
* Total Cancellations KPI
* Cancellation Rate KPI
* Cancellations by Guest Type chart
* Cancellation by Hotel Type chart
* Year-wise Cancellation chart
* Cancellation by Month chart
* Cancellation by Room Status chart
* Year Slicer for interactive filtering

#### Year Slicer Functionality

The dashboard includes a Year Slicer with three options: 2015, 2016, and 2017.

Selecting a year filters the connected PivotTables and charts to display the corresponding year's cancellation data. This allows users to explore year-specific patterns without manually changing the filters in each chart.

The Excel workbook is included in this repository so that users can explore the dashboard and interact with the slicer themselves.

## Key Metric

**Overall Cancellation Rate: Approximately 37.04%**

The cancellation rate is calculated as:

Cancellation Rate = (Total Cancelled Bookings / Total Bookings) × 100

The metric represents the proportion of bookings that were cancelled in the overall dataset.

## Key Learning Outcomes

Through this project, I gained practical experience in:

* Preparing and categorizing data using Excel formulas.
* Applying IF and AND functions to create custom categories.
* Summarizing data using PivotTables.
* Creating charts to compare cancellation patterns.
* Designing KPI cards and an interactive dashboard.
* Using slicers to explore data by year.
* Communicating analytical findings through visualizations.

## Acknowledgment

Thanks to the original dataset contributor on Kaggle for making the Hotel Booking Demand dataset available for analysis.

This project is an important first step in my Data Analytics learning journey.

