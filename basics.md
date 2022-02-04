# Basics

### Business Intelligence with Power BI

**Business Intelligence**: It's the ability to transform data and information, and in turn, this information into knowledge, to speed up time in terms of decision-making

![Knowledge pyramid](https://i.imgur.com/cn72R3p.jpg)

**BI Flow**

* **ETL**
  * Data **extraction** from data sources
  * Data **transformation** (source consolidation, cleaning and transformation of data)
  * Data **load** into Power BI data warehouse
  * Tools: PowerCenter, SQL Server Integration Services (SSIS), Oracle Data Integrator (ODI), Power Query (in Power BI)

![ETL in Power BI](https://i.imgur.com/OONplWt.png)

* **Modeling**
  * Relationships
  * KPI's
  * Optimization (to answer all business questions)
  * Tools: Erwin Data Modeler, PowerDesigner (SAP modeling tool), Power Pivot (in Power BI)
    * **Data Warehouse**: Usually serves as the central database of a company or, in other words, the database where all the useful data of an organization is stocked
    * **Data Mart**: Stores concise and specific data sets used for analysis for a specific department or line of business, such as the sales department

![Modelling in Power BI](https://i.imgur.com/g6tBXTY.png)

* **Reporting (putting into operation)**:
  * Data visualization
  * Reports
  * Dashboards
  * Storytelling
  * Tools: Power BI, Qlik, Tableau, and so on
    * **Dashboard**: A data dashboard is a businesses tool used to help track, analyze, and display data, usually to gain deeper insight into the overall wellbeing of the organization, a department, or even a specific process. _**In Power BI, it corresponds to the report**_
    * **Balanced scorecard**: It's a tool for monitoring the strategic decisions taken by the company based on indicators previously established and that should often permeate through at least four aspects – financial, customer, internal processes, and learning & growth -. _**In Power BI, it corresponds to the dashboard**_

**Power BI**: It's an **integral** and comprehensive **Business Intelligence solution** that provides a detailed view of the most critical data within an organization

**Business Suite**

* **Power BI Desktop**: Desktop tool **oriented to the development environment**, which allows us to connect to various data sources and create reports
* **Power BI Service**: Service in the cloud that allows us to establish the **entire collaborative environment**
* **Power BI Mobile**: Mobile application that allows us **to view and interact with a report from any mobile device (Android & Apple)**

**Power BI components**

* **Power Query ETL**: Extraction, transformation, and loading of data
* **Power Pivot (DAX) Modeling**: Answer all business questions

### Power BI architecture

**Power BI Free architecture**

* Includes 1 GB of storage
* Isn't possible to collaborate with other users simultaneously (reports, dashboards, and dataset), but it's possible to publish on websites (without security)
* Report sharing is only possible in public mode (without security)

**Power BI PRO architecture**

* Includes 10 GB of storage
* Can be shared with internal users as long as they also have a PRO license
* Optional gateway
* Can actualize data up to 8 times per day
* The creator (on Desktop), and user (on Service) must have got, each one, a license

**Power BI PREMIUM architecture**

* Includes 100 TB of storage
* Can be shared with internal users without requiring them to have Power BI PRO
* Greater scalability and performance than shared capacity in Power BI Service
* Can actualize data up to 48 times per day
* The creator (on Desktop), and user (on Service) must have got, each one, a license

**Notice**: None of this can be started with a personal email account, but only with a business or with an educational email account

![Power BI architecture](https://i.imgur.com/x4S1XfN.png)

### Connection types

**Connection types**

Power BI allows us to connect to a wide variety of data sources, from Excel files, SQL Server databases, websites, and so on

**Connection types**

* **Live Connection or Dynamic**: Read from SSAS or from a Power BI Service dataset, in other words, the data is stored outside Power BI (like Direct Query)
* **Direct Query**: The data isn't copied since each interaction requests a query to the database
* **Import**: The data is copied locally within the Power BI model (this is the most common type)
* **Composite Models**: Combines Import and Direct Query technologies. It also allows us to use multiple datasets
