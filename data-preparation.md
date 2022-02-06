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
* The purpose of this tool is not to analyze the data&#x20;
* Magic: It's the collection of steps that are carried out to reach a result, it also allows you to go back or forward these, without modifying the data source. It is similar to the process that a macro performs in Excel

![Power Query](https://i.imgur.com/zIjUUnw.jpg)

### Transformations

### Combinations

**Append**

* Allows joining two or more tables
* It's recommended that both have the same structure, if this isn't the case, the system adds the fields of all others with null values to the final set
* It's similar to a standard SQL **UNION** operation
* The results can be a new query or added to an existing step

**To combine**

* The functionality of combining queries. It allows us to take two tables and cross them using a common column
* It's usually used to complement the information in a table
* It's the closest equivalent to the **JOIN** function of the SQL standard

**Combine binaries**

* This functionality allows us to extract the tables from the files through an automated process
* It's usually used through the folder connector
* It's especially useful when the information source is too fragmented for the append operation
