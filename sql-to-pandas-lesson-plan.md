---
title: SQL/Pandas
layout: post
weight: 10
hidden: true
---


Lesson Plan Template:
===


**Course**: DS   <br/>
**Mod**: Mod 2                    <br/>
**Topic**:  SQL and Pandas   <br/>
**Amount of time**: 2  hours <br/>
**Author**: Alison Peebles Madigan


***

## Lesson Summary:

#### Topic:
A beginner's guide to databases, SQL, & using them with pandas
#### Learn.co material:
Section 9

#### Prerequisite knowledge/ Prework:
- Pandas dataframes
- 
#### Learning goals for this lesson:

- Goal 1: Summarize the use case for sql in the data science skill set
- Goal 2: Define key sql terminology
- Goal 3: Get information about DB schema and table structure
- Goal 4: Use basic SQL commands:
  - Construct SQL queries
  - Use JOIN to merge tables along logical columns
  - Grouping Data with SQL
- Goal 5: Query data from pandas dataframes using SQL
- Goal 6: Convert SQL to pandas

#### Misconceptions:
SQL and Python have to be used seperately.
SQL has nothing to do with the data science tool kit.
SQL is really complicated.

#### Materials
- react.js Slides
- Jupyter notebook for students
- Chinook and airlines databases
- a million pics 

***


## Lesson Outline:

**Step**: Activation <br/>
**Time**: 5 min


You are a data analyst for the Homeland Security, trying to create reports on the active airports world wide. The data you need to access is in a SQL database. YOu need to be able to query for the data in a database!

- Who has used sql?
- "structures query language"

_Learning Goals in sequence:_<br/>
What are the objectives, or steps students will need to do in order to achieve the goal or solve the problem?


- Goal 1: Summarize the use case for sql in the data science skill set
- Goal 2: Define key sql terminology
- Goal 3: Get information about DB schema and table structure
- Goal 4: Use basic SQL commands:
  - Construct SQL queries
  - Use JOIN to merge tables along logical columns
  - Grouping Data with SQL
- Goal 5: Query data from pandas dataframes using SQL
- Goal 6: Convert SQL to pandas df



**Step**: Goal 1: Summarize the use case for sql in the data science skill set <br/>
**Time**: 

_Demonstrate_: <br>

**Different Data Roles**

- Review netflix slide
- Review where sql is

**Hierarchy of AI slide** 

- Before we can do any sort of modeling of the data, we need to retrieve it from a database. While there are many formats for databases, most modern examples utilize some flavor of SQL. 
- we need the engineers to make the data available
- Or, how to get the data into our system

**ETL side** 

 - Databases are built on SQL 
 - ETL in the background transforms varied data sources to one data warehouse that then powers our analysis
 - When it's on a server, it can be automated, and "batches" are run, and there are "Triggers" - to keep the data fresh and accurate.

**Schema view**

- A relational database management system (RDBMS) is a type of DBMS with a row-based table structure that connects related data elements and includes functions that maintain the security, accuracy, integrity and consistency of the data.
- In general, databases store sets of data that can be queried for use in other applications. A database management system supports the development, administration and use of database platforms
- The most basic RDBMS functions are related to create, read, update and delete operations, collectively known as CRUD.

_Application_:  

- Remember Greg from the cross validation lesson?
- It's been taking a while for the datawarehouse people to send over the datasets for his analysis. You recommend that he write a sql query to connect to the database directly.
- He tells you that as a data scientist he doesn't need to know sql and that we should focus more on the data engineering deparatment getting their timeline together rather than ask him to learn sql

What do you tell Greg?


**Step**: Learning Goal 2: Define key sql terminology  <br/>
**Time**:  min

Review two slides and point out the key terms:

- Schema -> diagram of how tables fit together, how many tables, etc
- Primary Key -> the main id associated with that table
- Foreign Key -> primary keys from other tables you have in a different table to merge
- Structured queries -> the language of sql
- Views -> what we get from a query, and when it is stored and can see that query regularly


**Step**: Learning Goal 3: Get information about DB schema and table structure  <br>
**Time**:  min

Introduce Sqlite:<br>

- SQLite is a popular open source SQL database.
- It can store an entire database in a single file.
- It is 'lite' because it is not server based.
- Does not have many features of server-based RDBMS like users and permissions.
- Great to get up and running quick, not good for complex projects.

_Demonstrate_: <br>

- What do we first do when we get a dataframe with pandas? Yes, we explore it and get its summary information
- There a separate functions we can use to get database information

`connect` and `cursor` to access a database

use `sqlite_master` to get schema information

get information about a table using `.describe` and `Pragma`

_Application_: <br>

- Have them practice getting the information for the other tables in the db using `Pragma`

**Step**: Learning Goal 4: Utilize SQL syntax with Python  <br>
**Time**:  min

**Construct SQL queries**<br>
_Demonstrate_: <br>
 
- Discuss the structure of a SQL query
- Discuss key terms and options
- Create an example SQL query
- Explain how sql can show a single aggregate
- Translate a question into sql

_Application_: <br>
- Students constuct queries to retrieve specified information


**Use JOIN** to merge tables along logical columns<br>
_Demonstrate_: <br>

- Review purpose of joins
- OUTER joins not possible in sqlite

_Application_: <br>

- Students construct queries that join tables along logical columns
- Students use Inner and Outer jois to join same tables
- Create MANY-to-MANY joins


_Informal assessment_: <br/>
Coding Exercise - Students attempt to JOIN several tables into single format

- Use the relevent airlines db data from SQL

 
 **Grouping Data** with SQL<br>
 
- Create example queries with aggreagate functions (MIN, MAX, etc.)
- Show example of grouping data (using GROUP BY clause) in queries
 

**Step**: Learning Goal 5: Query data from pandas dataframes using SQL  <br>
**Time**:  min

_Demonstrate_: <br>

- discuss `.query()` and its documentation
- clarify that it works only to filer data
- needs to take a string
- demo it with the animal shelter dataset
- point out it works most easily with no spaces in column names

_Application_: <br>

- have them use `.query()` on the animal shelter dataset to subset the data by a filter

**Step**: Learning Goal 6: Convert SQL to pandas df  <br/>
**Time**:  min

_Demonstrate_: <br>

- easiest way to convert the results of a sql query using `sqlite` to a pandas dataframe. 
- `pd.read_sql_query`

_Application_: <br>
Have them re-use a query from earlier and store it as a pandas dataframe.


**Step**: Integration - Chinook media sales  <br/>
**Time**: 30 min

_Review_: <br/>

- Review all the skills they learned


_Synthesis_: <br>

- Review questions they are now expected to answer about database
- Students connect to tables in sql using importeed packages


**Step**: Assessment:  <br/>
**Time**: 5 min (outside of lecture)

- Poll questions at end of day

**Step**: Reflection:  <br/>
**Time**: [ ] min
- Discuss the consequences of using SQL in a python environment. 

