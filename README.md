## Awesome Chocolate Sales Analytics Dashboard

### About the Project
The dashboard provides deep insights into the sales performance of "Awesome Chocolate," a fictional chocolate manufacturer. It analyzes key metrics such as sales, boxes shipped, costs, and profits, while also offering a specialized view into "Low Box Shipments" (shipments under 50 boxes) and month-on-month performance trends

### Built With
Power BI Desktop: The primary platform for data visualization and report creation.

Power Query: Used for data transformation, cleaning, and creating derived calendar columns.

DAX (Data Analysis Expressions): Utilized to build complex measures, time intelligence calculations,
and field parameters.

Excel: The source format for the sample data tables.

PowerPoint: Used for designing the dashboard wireframe and creating custom icons/logos.

### Data Preparation
The raw data was imported from an Excel workbook containing five distinct tables

During the transformation phase in Power Query, the following steps were taken:
Validated data types and performed necessary cleanup.

Enhanced the Calendar Table by adding columns for Year, Month Number, Month Name, Day of Week, and a "Start of Month" date for chronological sorting in visuals.

Created Box Bins in the shipment table to facilitate histogram analysis for shipment distribution.

### Data Modeling
The project utilizes a Star Schema data model for optimized performance:

Fact Table: Shipments (contains granular transaction data).

Dimension Tables: Salesperson, Product, Geography, and Calendar.

Relationships: Dimension tables are neatly connected to the fact table using unique keys such as salesperson name, product ID, geography, and date.

The Calendar table was marked as a "Date Table" to ensure accurate time intelligence calculations.

### DAX Measures
A dedicated measure table was created to house all calculations

Key measures include:
Basic KPIs: Total Sales, Total Boxes, and Total Shipments (calculated using SUM and COUNTROWS).

Profitability Analysis: Total Costs (calculated by multiplying boxes by the related product cost), Total Profit, and Profit Percentage.

Logic-Based Metrics: LBS Count and LBS % to identify shipments with fewer than 50 boxes.

Time Intelligence: Total Sales Previous Month and Month-on-Month Sales Change % to track growth trends.

Dynamic Labels: Latest Month Sales and Latest Month-on-Month Change to drive content in the KPI cards.

### Dashboard Features
KPI Header: Features the new Card Visual with reference labels, custom icons, and conditional formatting to highlight positive or negative month-on-month changes.

Dynamic Trend Chart: A line graph integrated with Field Parameters, allowing users to toggle the view between Sales, Boxes, Shipments, Costs, and Profit.

Interactive Histogram: Visualizes shipment density with a Zoom Slider for detailed exploration of box counts.

Dual-View Table with Bookmarks: An interactive section that uses Bookmarks to switch between "Salesperson Performance" and "Product Performance" details.

Advanced Formatting: Includes Data Bars for profit percentages and Traffic Light Icons (Red/Amber/Green) to indicate performance against targets.

Global Filters & Tooltips: A slick slicer panel for Category and Geography, paired with custom Tooltips that provide geographic breakdowns when hovering over data points.

### Insights
Profitability Variance: Analysis revealed significant profit margin differences between products; for example, Peanut Butter Cubes reached an 87% profit margin, while Baker's Choco Chip only achieved 17.4%.

Shipment Trends: The dashboard identified that 10.2% of total shipments were "Low Box" samples, with specific products like Milk Bar having a much higher LBS percentage (16.5%) than others like Raspberry Choco (5%).

Target Monitoring: Through the traffic light indicators, the business can quickly identify which salespersons are meeting the 60% profit target.

### Screenshots / Demos
The dashboard looks like.

Example:![Dashboard Preview](https://github.com/sithara-sreedharan/Chocolate-Sales-Dashboard/blob/main/Screenshot%20Chocolate%20Sales%20Dashboard.png) 


