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
**Author**: Robert Jackson

Ported from the ds-lesson-starters repository [here](https://github.com/learn-co-curriculum/ds-lessons-starter/tree/master/lesson-plans-by-mod/Module-2/sql-to-pandas).


***

## Lesson Summary:

#### Topic:
Using SQL and SQL syntax with pandas
#### Learn.co material:
https://docs.google.com/presentation/d/1u6PaCJTzxipFO63MoHlj_kB_ywBqFe1PPmRSx5ZXyy0/edit?usp=sharing

#### Prerequisite knowledge/ Prework:
- Pandas dataframes
#### Learning goals for this lesson:

Construct SQL queries
- SELECT data from table
- INSERT data into tables
- Create tables

Use JOIN to merge tables along logical columns
- Create JOIN statements along INNER and OUTER joins
- Create ONE-to-MANY and MANY-to-MANY joins

Grouping Data with SQL
- Write queries with aggregate functions
- Use GROUP BY to sort data

Query data from pandas dataframes using SQL
- Import and utilize the 'sqlite3' library
- Utilize SQL syntax in a Python envrionment to duplicate standard SQL queries

#### Misconceptions:
SQL and Python have to be used seperately.

#### Materials
- (Learn.co Link)
- Slides
- Jupyter notebooks

***

terms schema, dimensions, facts, primary key, foreign key,

- In general, databases store sets of data that can be queried for use in other applications. A database management system supports the development, administration and use of database platforms
- The most basic RDBMS functions are related to create, read, update and delete operations, collectively known as CRUD.
- 
- An realtionsal database management system (RDBMS) is a type of DBMS with a row-based table structure that connects related data elements and includes functions that maintain the security, accuracy, integrity and consistency of the data.

## Lesson Outline:

**Step**: Introduction to SQL <br/>
**Time**: 2 hours

_Goal/Scenario:_<br/>
You are a data analyst for a large company that is doing research on economic properties of various countries. The data you need to access is in a SQL database. YOu need to be able to query for the data in a database!

_Learning Goals in sequence:_<br/>
What are the objectives, or steps students will need to do in order to achieve the goal or solve the problem?

SQLite¶
SQLite is a popular open source SQL database.
It can store an entire database in a single file.
It is 'lite' because it is not server based.
Does not have many features of server-based RDBMS like users and permissions.
Great to get up and running quick, not good for complex projects.

**Step**: Activation <br/>
**Time**: 5 min

Before we can do any sort of modeling of the data, we need to retrieve it from a database. While there are many formats for databases, most moden examples utilize some flavor of SQL. As we continue through this lesson, consider:

- What does it mean when we say SQL is 'declarative'?
- Does anyone know what SQL is? How about what a relational database system is?
- What is a 'query' language?


**Step**: Learning Goal 1: Be able to construct SQL queries  <br/>
**Time**: 15 min

_Demonstrate_: <br/>
- Create an example SQL query.
- Discuss the structure of a SQL query's was 
- Discuss what a relational database system is.

_Application_: <br/>
- Students constuct queries to retrieve specified information
- Edit existing tables by deleting, changing, and adding information to tables
- Studetns create SQL tables and populate them


_Informal assessment_: <br/>
Kahoot Poll - Multiple choice
- Convert English queries into SQL queries

**Step**: Learning Goal 2: Use JOIN to merge tables along logical columns  <br/>
**Time**: 20 min

_Demonstrate_: <br/>
- Use JOIN to merge the results of two or more tables
- Explain the struct of a JOIN clause
- Explain the difference between ONE-to-MANY and MANY-to-MANY

_Application_: <br/>
- Students construct queries that join tables along logical columns
- Students use Inner and Outer jois to join same tables
- Create MANY-to-MANY joins


_Informal assessment_: <br/>
Coding Exercise - Students attempt to JOIN several tables into single format


**Step**: Learning Goal 3: Grouping Data  <br/>
**Time**: 20 min

_Demonstrate_: <br/>
- Create example queries with aggreagate functions (MIN, MAX, etc.)
- Show example of grouping data (using GROUP BY clause) in queries

_Application_: <br/>
- Students construct queries that join tables along logical columns
- Students use Inner and Outer jois to join same tables
- Create MANY-to-MANY joins


_Informal assessment_: <br/>
Coding Exercise - Students attempt to JOIN several tables into single format
- Use the test.db data from SQL


**Step**: Learning Goal 4: Utilize SQL syntax with Python  <br/>
**Time**: 30 min

_Demonstrate_: <br/>
- Overview the sqlit3 library
- Demonstrate the creation of a table using the 'sqlite3' library
- Overview the pandasql libary
- Create SQL queries in Python
- Demonstarte SQL syntax in action using the pandasql

_Application_: <br/>
- Students connect to tables in sql using importeed packages
- Students create tables in pandasql
- Discuss the consequences of using SQL in a python environment


_Informal assessment_: <br/>
Kahoot poll - choose proper syntax for queries in python:
- Multiple choice poll conducted anonomously 


**Step**: Assessment:  <br/>
**Time**: 30 min

In pairs of two, students will import data from SQLite using the sqlite3 library for Python. The data they'll be pulling will be the world.db data set, containin tables on the info of various countries. Students will use this data, in conjunction with pandasql, to query the data and craete visualizations in matplotlib on any aspect of the data the wish.

**Step**: Reflection:  <br/>
**Time**: [ ] min

