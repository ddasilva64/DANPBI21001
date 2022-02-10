# Data modeling

### Data modeling

**The BI Flow consists of**

* ETL
* Data Modeling
* Data Visualization

ETL is handled with Power Query, while Data Modeling is done with Power Pivot

**Data modeling**: Complex analyses between several tables connected by a common field

### Relations and filters

**Relationships between tables**

* **Primary keys**: Used to define the primary key of the table. Columns that have this profile cannot contain null values and cannot have duplicate values. That is, it must contain unique records
* **Foreign keys**: A foreign key is a column or set of columns, which contains a value that refers to a row of another table

**Relationship types**:

* **1:1 (from 1 to 1)**: Both tables are connected by their primary keys. It acts as an extension of these
* **1:n (from 1 to several)**: Occurs when a primary key is connected with the foreign key of another table
* **m:n (many-to-many)**: Occurs when both tables are related by their foreign keys (none of the columns have unique values). Avoid these kinds of relationships

**Conflicts to resolve**:

1. **Relationships m:n**: By means of the concatenation of key fields or by means of associative tables
2. **Inactive Relationships**:&#x20;
   1. Delete them because they are not necessary&#x20;
   2. They can be unresolved relationships m:n&#x20;
   3. The Model Documenter tool is very interesting

**Design of data models**:

* There are different types (star, snowflake, etc.)
* In **Power BI,** we focus on the **star schema** model, which is the most efficient

**Star model components**:

* **Fact tables**: Also known as **transactional tables** or (fact in English). They answer the question **of what do I want to obtain or look for?**
* **Dimension tables**: Also known as **lookup tables**. They respond to the level of **classification that interests us**, which can be **time or type of data**

![Fact and dimension](https://i.imgur.com/gTFNcvu.png)

**Data model engine**

* His name is **Vertipaq**
* Handles all data analysis operations (DAX)
* Uses in-memory technology that provides high storage and performance in the data query
* Allows short development cycles

### Fixing modeling issues

1. **Data Model Design**: The Star Schema Model is the most used in Power Bi because it is made up of a dimension table (Search) and a Fact table (transactional) where the integration of both excels the one-to-many relationship and thus avoids data redundancy
2. **Data Model Engine**: VERTIPAQ is in charge of data analysis operations (DAX) and uses technology (in-memory) that provides high performance to store and query data

**Need for data modeling**:

* If a single dashboard is loaded, it will have poor performance for large data volumes and with data redundancy
* Proper modeling avoids these problems

### DAX language

**DAX (Data Analysis Expression)**:

* Power BI Analytical Expression Language: **Uses analytical formulas and operational functions** that allow the calculation of one or more values
* Created **to manipulate a tabular data model**
* It is based on Excel; hence their similarity in terms of formulation structure. We can find this language in Power BI, SAS Tabular, and Excel in the Power Query plugin

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
