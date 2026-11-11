🚲 Where Are the Bikes?

Smart City Bike Sharing – An Interactive Power BI Analysis

A city can have thousands of bike stations. But does that mean people can actually find a bike when they need one?

That is the question behind this project.

I built this Power BI dashboard to investigate the availability of bikes and empty docking spaces across a smart city bike-sharing network. Rather than just counting stations, I wanted to understand how the network is distributed, where operational imbalances may exist, and which areas deserve closer attention.

🎯 The Mission

The objective was to transform raw bike station data into an interactive business intelligence report that helps answer five questions:

How many bike stations are operating across different contracts?

Where are the available bikes concentrated?

Which stations have zero available bikes?

Which contracts have higher or lower station occupancy?

What operational areas should be investigated further?

📊 Inside the Dataset

The analysis covers:

Dataset information

Details

Total station records

2,856

Unique stations

2,856

Operating contracts

25

Original source columns

12

Date dimension records

183

The dataset contains station information, geographical coordinates, contract details, bike capacity, available bikes, available docking spaces, station status and last-update timestamps.

🛠️ My Analytics Workflow

I approached this project as an end-to-end Data Analyst assignment.

01 — Data Preparation

Using Power BI Power Query, I:

Corrected data types.

Split geographical coordinates into Latitude and Longitude.

Created a unique StationKey using Contract Name and station number.

Created a separate date dimension.

Prepared fact and dimension tables.

02 — Data Modelling

Designed a star schema with four tables:

Fact_BikeStations

Dim_Station

Dim_Contract

Dim_Date

Established three active one-to-many relationships to support consistent filtering and analysis.

03 — DAX Measures

Created measures to calculate:

Total Available Bikes

Total Bike Capacity

Total Available Stands

Total Occupied Stands

Occupancy Percentage

Availability Percentage

Total Stations

Station Occupancy %

04 — Dashboard Development

Created KPI cards, contract comparison charts, operational condition charts and a station-level detail table.

Added an interactive Contract slicer covering all 25 contracts.

🔍 What Did the Numbers Reveal?

This is where the project becomes interesting.

Key finding

Result

Total stations analysed

2,856

Overall occupancy

43.85%

Overall availability

56.15%

Stations with zero available bikes

705

Stations with zero available stands

335

🏙️ Contract-level discoveries

Vilnius: Highest occupancy at 77.92%, with only 22.08% availability.

Cergy-Pontoise: Lowest occupancy at 7.09%, with 92.91% availability.

Bruxelles-Capitale: Highest available bike count at 3,532.

Marseille: Highest absolute count of stations with zero available bikes (123).

These findings highlight differences between contracts and identify areas for further operational investigation.

🧠 Four Types of Analysis

I used the four fundamental types of data analytics to interpret the results.

Analysis

How I applied it

Descriptive

What is happening? Analysed station counts, bike availability, capacity and occupancy.

Diagnostic

What needs investigation? Identified contracts with high or low occupancy and stations with zero availability.

Predictive

What might happen next? Identified the need for historical station-level records before building reliable forecasts.

Prescriptive

What should be considered? Recommended investigating operational imbalances and evaluating possible bike redistribution.

💡 Business Recommendations

Based on the findings, the following actions could be considered:

Investigate the 705 stations reporting zero available bikes.

Review the 335 stations with zero available docking spaces.

Prioritise an operational review of Marseille due to its high absolute count of zero-bike stations.

Examine the availability differences between Vilnius and Cergy-Pontoise.

Collect repeated time-based station data to support future demand forecasting.

These are investigation priorities, not proof of customer demand or confirmed causes. Contract sizes and usage patterns should be considered before comparing operational performance.

⚠️ An Important Data Limitation

Each station appears only once in the fact table. The Last Update field represents the timestamp of that station record.

Therefore, monthly totals represent the distribution of station records by update month, not repeated historical network-wide availability snapshots.

The current dataset is suitable for station-level and contract-level analysis, but it does not support reliable historical demand forecasting.

🧰 Tools & Technologies

Power BI Desktop – Data modelling and dashboard development

Power Query – Data cleaning and transformation

DAX – Measures and calculations

Star Schema – Data modelling approach

📌 What I Learned

This project helped me understand that building a dashboard is only one part of data analytics.

I learned how to:

Transform raw data into structured analytical tables.

Create fact and dimension tables.

Establish relationships using unique keys.

Write DAX measures for business KPIs.

Build interactive dashboards using slicers.

Interpret business findings rather than simply display numbers.

Recognise data limitations before making conclusions.

🏁 Final Takeaway

The goal was not just to count bikes. It was to understand how effectively a bike-sharing network makes its resources available across the city.

This project represents my practical learning journey in Power BI, data modelling and business-focused data analytics.

Built with curiosity, Power BI, and a question worth investigating. 🚲📊
