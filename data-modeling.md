# Data modeling

### Data modeling

**The BI Flow consists of**

* ETL
* Data Modeling
* Data Visualization

ETL is handled with Power Query, while Data Modeling is done with Power Pivot

Data Modeling in Power BI focuses on performing complex analysis across multiple tables connected by a common field

### Relations and filters

The data model can be done in two ways; one is the star model and the other is called a snowflake or something similar to a waterfall

**For this, it is necessary to know two key aspects**

**Facts**: Answer the question "What do I want to obtain or seek"

**Dimensions**: Responds to the level or classification that I am interested in, which can be time or type of data

![Fact and dimension](https://i.imgur.com/gTFNcvu.png)

### Fixing modeling issues

1. **Data Model Design**: The Star Schema Model is the most used in Power Bi because it is made up of a dimension table (Search) and a Fact table (transactional) where the integration of both excels the one-to-many relationship and thus avoids data redundancy
2. **Data Model Engine**: VERTIPAQ is in charge of data analysis operations (DAX) and uses technology (in-memory) that provides high performance to store and query data
