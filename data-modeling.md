# Data modeling

### Data modeling

**The BI Flow consists of**

* ETL
* Data Modeling
* Data Visualization

ETL is handled with Power Query, while Data Modeling is done with Power Pivot

**Data modeling**: Complex analyses between several tables connected by a common field

### Relations and filters

The data model can be done in two ways; one is the star model and the other is called a snowflake or something similar to a waterfall

**For this, it is necessary to know two key aspects**

**Facts**: Answer the question "What do I want to obtain or seek"

**Dimensions**: Responds to the level or classification that I am interested in, which can be time or type of data

![Fact and dimension](https://i.imgur.com/gTFNcvu.png)

### Fixing modeling issues

1. **Data Model Design**: The Star Schema Model is the most used in Power Bi because it is made up of a dimension table (Search) and a Fact table (transactional) where the integration of both excels the one-to-many relationship and thus avoids data redundancy
2. **Data Model Engine**: VERTIPAQ is in charge of data analysis operations (DAX) and uses technology (in-memory) that provides high performance to store and query data

### DAX language

It's an expression language where it uses analytical formulas and operational functions that allow the calculation of one or more values, created to manipulate a tabular data model and is based on Excel; hence their similarity in terms of formulation structure. We can find this language in Power BI, SAS Tabular, and Excel in the Power Query plugin

**Why DAX?**

* Navigation Relations
* Calculation of Dimensions
* Management of Time Dimensions (Time Intelligence)

**What can we create?**

* **Calculated Columns**: This allows methods to connect tables with multiple key columns and create new columns in the data model
* **Calculated Tables**: creates a table derived from another table
* **Measurement**: Supports time intelligence and creates dynamic calculations, which is the most used in Power BI

**Language Conventions (General Format)**

* 'table name'\[column name]\
  Example: 'table products'\[Price]

The table name can be omitted when used in calculated columns but it isn't recommended to do so

### Use CALCULATE

### Time intelligence

It refers to the techniques, tools, and methodologies that allow us to analyze our measurements thoroughly through the concept of "time", that is, it is present in all business intelligence solutions as a starting point to explore the information:

* From analyzing the evolution of our measurements in time, a new dimension (tables) Dates and calendar is used continuously without missing a single day between the dates, this works in our model
* Monitor growth or decrement in detail
* Make projections

### Iterators X
