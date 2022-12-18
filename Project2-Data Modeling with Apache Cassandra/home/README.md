# Project: Data Modeling with Cassandra

## Introduction
A startup called `Sparkify` wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analysis team is particularly interested in understanding what songs users are listening to. Currently, there is no easy way to query the data to generate the results, since the data reside in a directory of CSV files on user activity on the app.
They'd like a data engineer to create an Apache Cassandra database which can create queries on song play data to answer the questions, and wish to bring us on the project. our role is to create a database for this analysis. we'll be able to test our database by running queries given to is by the analytics team from Sparkify to create the results.

## Project Overview
In this project, we'll apply what we've learned on data modeling with Apache Cassandra and complete an ETL pipeline using Python. To complete the project, we will need to model our data by creating tables in Apache Cassandra to run queries. we are provided with part of the ETL pipeline that transfers data from a set of CSV files within a directory to create a streamlined CSV file to model and insert data into Apache Cassandra tables.
We have provided a project that takes care of all the imports and provides a structure for ETL pipeline we'd need to process this data.

## Datasets
For this project, we'll be working with one dataset: `event_data`. The directory of CSV files partitioned by date. Here are examples of filepaths to two files in the dataset:
+ `event_data/2018-11-08-events.csv`
+ `event_data/2018-11-09-events.csv`


## To get started with the project:
The project directory includes one Jupyter Notebook file, in which:
1. we will process the event_datafile_new.csv dataset to create a denormalized dataset
2. we will model the data tables keeping in mind the queries we need to run
3. we have been provided queries that we will need to model our data tables for
4. we will load the data into tables we create in Apache Cassandra and run our queries

## Modeling NoSQL database or Apache Cassandra database
+ Design tables to answer the queries outlined in the project file
+ Write Apache Cassandra `CREATE KEYSPACE` and `SET KEYSPACE` statements
+ Develop your `CREATE` statement for each of the tables to address each question
+ Load the data with `INSERT` statement for each of the tables
+ Include `IF NOT EXISTS` clauses in our `CREATE` statements to create tables only if the tables do not already exist. We recommend also include DROP TABLE statement for each table, this way we can run drop and create tables whenever we want to reset our database and test our ETL pipeline
+ Test by running the proper select statements with the correct `WHERE` clause

## Build ETL Pipeline
1. Implement the logic in section Part I of the notebook file to iterate through each event file in `event_data` to process and create a new CSV file in Python
2. Make necessary edits to Part II of the notebook file to include Apache Cassandra `CREATE` and `INSERT` statements to load processed records into relevant tables in our data model
3. Test by running `SELECT` statements after running the queries on our database
