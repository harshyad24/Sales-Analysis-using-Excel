# Work Sales Analysis - Excel Dashboard

A comprehensive sales analytics solution built in Excel with Power BI integration, providing detailed insights into business performance across multiple dimensions including time, geography, and profitability.

## 📊 Dashboard Overview

This analysis provides a complete view of sales performance with the following key metrics:
- **Total Revenue**: $307.09M
- **Total Profit**: $126.29M
- **Profit Margin**: 41.1%
- **Total Transactions**: 60.4K
- **Total Quantity**: 606 units

 ## 🏗️ Data Architecture
 ![🏗️ Data Architecture](https://github.com/harshyad24/Sales-Analysis-using-Excel/blob/main/Screenshot%202025-07-09%20023116.png)

### Data Model Structure
The analysis is built on a star schema with the following dimension and fact tables:

#### Dimension Tables
- **DimDate**: Complete date hierarchy with Year, Month, Day attributes
- **DimProduct**: Product catalog with ProductKey, Product name, and Color
- **DimCustomer**: Customer information including Geography, Full Name, and BirthDate
- **DimGeography**: Geographic hierarchy with Country, City, and SalesTerritory mapping
- **DimSalesTerritory**: Sales territory definitions and groupings

#### Fact Table
- **FactInternetSales**: Central transaction table containing:
  - Sales metrics (OrderQuantity, UnitPrice, Total Revenue, Cost of Goods Sold, Total Profit)
  - Date keys (OrderDate, DueDate, ShipDate)
  - Dimension keys (Product, Customer, SalesTerritory, Geography)

## 📈 Key Performance Indicators

### Financial Metrics
- **Revenue Growth**: Tracking year-over-year performance (2005-2008)
- **Profit Margins**: Consistent 41.1% margin across periods
- **Cost Management**: $180.80M in total COGS

### Operational Metrics
- **Transaction Volume**: 60.4K total transactions
- **Seasonal Patterns**: Monthly profit distribution showing peak performance
- **Geographic Performance**: Multi-country analysis across 6 regions

## 🎯 Analysis Capabilities

### Time-Based Analysis
- **Multi-year Comparison**: 2005-2008 performance trending
- **Seasonal Analysis**: Monthly profit patterns with May, June, December highlighting
- **Weekday Performance**: 72.01% of profits generated on weekdays vs 28% weekends
- **Daily Distribution**: Weekday contribution analysis (Mon-Fri performance)

### Geographic Segmentation
- **Country Performance**: Australia, Canada, France, Germany, United Kingdom, United States
- **Revenue Distribution**: Country-wise revenue contribution analysis
- **Territory Mapping**: Sales territory performance tracking

### Quarterly Performance
- **Q1**: $4.41M - $23.46M (14.33% - 25.80% of annual)
- **Q2**: $5.12M - $27.81M (16.65% - 30.58% of annual) 
- **Q3**: $8.45M - $17.50M (27.44% - 19.25% of annual)
- **Q4**: $12.80M - $22.16M (41.58% - 24.37% of annual)

## 🔍 Dashboard Features

### Interactive Elements
- **Year Selection**: Toggle between 2005-2008 data views
- **Month Filtering**: Detailed monthly performance analysis
- **Geographic Drill-down**: Country and territory-level insights
- **Profit/Revenue Toggle**: Switch between different KPI views

### Visualization Types
- **KPI Cards**: High-level metric summary
- **Trend Lines**: Monthly performance tracking
- **Bar Charts**: Weekday vs Weekend comparison
- **Heat Maps**: Monthly and quarterly performance
- **Geographic Tiles**: Country-wise performance grid

## 🛠️ Technical Implementation

### Excel Features Used
- **Power Query**: Data transformation and modeling
- **Power Pivot**: Relationships and calculated measures
- **Conditional Formatting**: Dynamic KPI highlighting
- **Interactive Charts**: Drill-down capabilities
- **Slicers/Filters**: Dynamic filtering options

### Key Formulas and Measures
```excel
Profit Margin = Total Profit / Total Revenue
YoY Growth = (Current Year - Previous Year) / Previous Year
Weekday Percentage = Weekday Profit / Total Profit
```

## 📋 Usage Instructions

### Getting Started
1. Open the Excel workbook with Power BI integration enabled
2. Refresh data connections to ensure latest information
3. Use the year selector to choose analysis period
4. Apply filters for specific geographic or time-based analysis

### Navigation
- **Main Dashboard**: Overview of all key metrics
- **Time Analysis**: Detailed temporal performance
- **Geographic View**: Regional performance breakdown
- **Quarterly Summary**: Seasonal pattern analysis

### Filtering Options
- **Year Filter**: 2005, 2006, 2007, 2008
- **Month Selection**: Individual month deep-dive
- **Country Filter**: Geographic performance isolation
- **Metric Toggle**: Revenue vs Profit vs Transaction views

## 📊 Data Quality Notes

- **Coverage Period**: Complete 4-year dataset (2005-2008)
- **Geographic Scope**: 6 countries with full territory mapping
- **Transaction Level**: Individual sale records with complete attribution
- **Data Refresh**: Connected to source systems for regular updates

## 🎯 Business Insights

### Key Findings
- Strong profit margins maintained at 41.1% across all periods
- Weekdays drive majority of business (72% of profits)
- Q4 consistently strongest quarter (41.58% in 2007)
- Geographic diversification across 6 major markets
- Seasonal patterns show May, June, December as peak months

### Recommended Actions
- Focus marketing efforts on weekday business drivers
- Leverage Q4 seasonal strength for annual planning
- Investigate weekend performance improvement opportunities
- Analyze geographic expansion potential in high-performing regions

---

## 🔄 Dashboard Development Process

### Data Pipeline Workflow

The Work Sales Analysis dashboard follows a systematic development process that transforms raw business data into actionable insights through multiple stages:

#### 1. Data Extraction & Integration
- **Source Systems**: Multiple business databases containing sales transactions, customer information, product catalogs, and geographic data
- **Data Consolidation**: Raw data from various sources is consolidated into a unified data warehouse structure
- **Quality Assurance**: Data validation checks ensure completeness and accuracy before processing

#### 2. Data Modeling & Transformation
- **Star Schema Design**: Implementation of dimensional modeling with fact and dimension tables optimized for analytical queries
- **Relationship Mapping**: Establishment of proper foreign key relationships between FactInternetSales and dimension tables (DimDate, DimProduct, DimCustomer, DimGeography, DimSalesTerritory)
- **Calculated Fields**: Creation of business logic for profit margins, growth rates, and performance indicators
- **Data Cleansing**: Standardization of geographic names, date formats, and product classifications

#### 3. Dashboard Construction
- **Layout Design**: Strategic placement of KPI cards, trend charts, and interactive filters for optimal user experience
- **Visualization Selection**: Choice of appropriate chart types (line charts for trends, bar charts for comparisons, heat maps for patterns)
- **Interactivity Implementation**: Development of drill-down capabilities, cross-filtering, and dynamic updates
- **Performance Optimization**: Query optimization and data compression to ensure responsive dashboard performance

#### 4. Business Logic Implementation
- **KPI Calculations**: Implementation of critical business metrics including profit margins (41.1%), growth rates, and performance ratios
- **Time Intelligence**: Development of year-over-year comparisons, seasonal analysis, and period-to-date calculations
- **Geographic Analysis**: Country-wise performance tracking and territory comparison logic
- **Segmentation Rules**: Weekday vs weekend analysis, quarterly performance distribution, and customer behavior patterns

#### 5. User Experience Design
- **Navigation Flow**: Intuitive user journey from high-level overview to detailed drill-downs
- **Filter Interactions**: Seamless filtering across years (2005-2008), months, countries, and business metrics
- **Visual Consistency**: Standardized color schemes, fonts, and chart formatting across all dashboard components
- **Responsive Design**: Adaptation for different screen sizes and viewing contexts


### Process Benefits

This structured approach delivers several key advantages:

- **Scalability**: The dimensional model supports easy addition of new data sources, metrics, and time periods
- **Performance**: Optimized data structure ensures fast query response times even with large datasets (60.4K transactions)
- **Accuracy**: Multiple validation steps guarantee data integrity and reliable business insights
- **Usability**: User-centered design process creates intuitive navigation and meaningful visualizations
- **Maintainability**: Clear documentation and standardized processes enable efficient ongoing support and enhancements

The end result is a comprehensive analytics solution that transforms complex business data into clear, actionable insights, enabling data-driven decision making across all levels of the organization.
