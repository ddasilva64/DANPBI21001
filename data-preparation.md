# Data preparation

### What's ETL?

* **Extract**: From virtually any data source, from flat to complex files, databases, or cloud services&#x20;
* **Transform**: This allows us to modify or enrich the extracted information without modifying the source&#x20;
* **Load**: Once the transformation is done, it's responsible for loading the result to the data model

### Transform data with Power Query

**Power Query**

It's a data connection technology that enables us to discover, connect, combine, and refine disparate data sources to meet our analytics needs

**What does Power Query do?**

* **Extract**: From virtually any data source
* **Transform**: Merge, combine, clean or enrich the data
* **Load**: The data for further analysis in Power BI

**Points to consider**

* The **purpose** of **Power Query** is **to** **get** **data** from a variety of sources **and to** **get ready for further analysis**
* The **purpose** of this tool **isn't to analyze the data**&#x20;
* **Magic**: It's the **collection of steps** that are carried out **to reach a result**, it also **allows us to go back or forward these, without modifying the data source**. It's similar to the process that a macro performs in Excel

![Power Query](https://i.imgur.com/zIjUUnw.jpg)

### Data types

* Unlike other programs like Excel, where data types are very flexible, in Power BI we need to define them well before we can use them
* As in relational databases, **each column must have its type well-defined to avoid errors**
* Classes:
  * **Integer**: Represents a 64-bit integer value (**8 bytes**). Since it is an integer, it has no digits to the right of the decimal place. **Allows 19 digits**; positive or negative integers between – 9,223,372,036,854,775,807 **– ($2^{63}+1$)** and 9,223,372,036,854,775,806 (**$2^{63} – 2$** ). You can represent the largest possible precision of the various numeric data types. As with the Fixed Decimal Number type, the Integer type **can be useful in cases where we need to control rounding**
  * **Decimal**: Represents a 64-bit floating point number (**8 bytes**). It is the most common type of number. Although it is designed to handle numbers with fractional values, it also handles whole numbers. The Decimal Number type can handle negative values ​​from $$– 1.79E^{+308}$$ to $$– 2.23E^{308}$$, and positive values ​​from $$– 2.23E^{–308 }$$ to $$1.79E^{+308}$$. For example, numbers like 34, 34.01, and 34.000367063 are valid decimal numbers. **The largest precision that can be represented in a decimal number type is 15 digits**. The decimal separator can be placed anywhere in the number. The decimal number type corresponds to the way Excel stores its numbers. Note that a binary floating point number cannot represent all numbers within its supported range with 100% precision. Therefore, small differences in precision may occur when representing certain decimal numbers.
  * **Fixed decimal**: Also known as **currency type**, this data type **has a fixed location for the decimal separator**. **The decimal separator always has four digits to the right and allows 19 significant digits**. The largest value it can represent is 922,337,203,685,477.5807 (positive or negative). Unlike the decimal number, the fixed decimal number type is always precise and is therefore **useful in cases where the imprecision of the floating point notation could introduce errors**
  * **Text**: **String** of **Unicode** character data. They can be strings, numbers, or dates represented in a text format. The maximum string length is 268,435,456 Unicode characters (where each Unicode character is 2 bytes) or 536,870,912 bytes
  * **Date/time**: **Represents a date and time value**. The date and time values are stored as a type of decimal number, so you can convert from one to the other. The time part of a date is stored as a fraction in integer multiples of 1/300 seconds (3.33 ms). Dates between the years 1900 and 9999 are supported
  * **Time**: **Represents only the time (without date)**. When converted to the model, the time value is the same as the date/time value with no digits to the left of the decimal position
  * **Date/time/time zone**: **Represents a UTC date and time with a time zone offset**. Converts to date/time when loaded into the model
  * **Duration**: **Represents a period of time**, which is converted to a type of decimal number when loaded into the model. As a type of decimal number, it can be added to or subtracted from a date/time field with the correct results. Since it is a type of decimal number, you can easily use it in visualizations that show magnitude
  * **Boolean**: Boolean value of True or False
  * **Binary**: The binary data type can be used to represent **any other data in a binary format**
  * **Any**: The Any data type is the state given to a column that **does not have an explicit data type definition**. Any is the data type that sorts all values. It is recommended to always explicitly define column data types for queries from unstructured sources and avoid having columns with data type Any as query output

### Transformations

**Transform**: **Shape the data**&#x20;

**Common transformations**:

* Rename columns or tables
* Change the data type (convert text to numbers, for example)
* Remove rows
* Set the first row as header
* Add columns
* Split columns
* Replace values
* Filter data

### Combinations

**Combining**: Connecting to **two or more data sources**, **shaping** them as needed, **and then consolidating** them into a useful query

**Common combinations**:

* Append queries
* Combine queries
* Combine binaries

**Append**

* Allows us to join two or more tables
* It is recommended that both have the same structure, if not, the system adds the non-matching fields with null values to the final set
* It is similar to a standard SQL **UNION** operation
* Results can be a new query or added to an existing step
* Steps:
  * In Transform data (Power Query)
  * Menu Merge/Append queries

**Combine**

* It allows us to take two tables and cross them through one or more fields in common
* Usually used to complement the information in a table
* It is the closest equivalent to the **JOIN** function of the SQL standard

**Combine binaries**

* This functionality allows us to extract the tables from the files through an automated process
* It's usually used through the folder connector
* It's especially useful when the information source is too fragmented for the append operation
