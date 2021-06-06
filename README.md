# Project: Data Modeling with Postgres
## Introduction
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app. <br>
Create a Postgres database with tables designed to optimize queries on song play analysis. Create a database schema and ETL pipeline for this analysis and test the database and ETL pipeline by running queries given to you by the analytics team from Sparkify and compare the results with their expected results.
## Project Description
Data modeling with Postgres, define fact and dimension tables for a star schema for a particular analytic focus.<br>
Build an ETL pipeline using Python, transfers data from JSON files in two local directories into these tables in Postgres using Python and SQL.
## Project Datasets
### Song Dataset
Each file is in JSON format and contains metadata about a song and the artist of that song. The files are partitioned by the first three letters of each song's track ID. For example, here are filepaths to two files in this dataset.
![image](https://user-images.githubusercontent.com/55506640/120908817-3dec8d80-c623-11eb-808a-7112a7f9e4ed.png)
<br>And below is an example of what a single song file, TRAABJL12903CDCF1A.json, looks like.
![image](https://user-images.githubusercontent.com/55506640/120908837-6a080e80-c623-11eb-8ded-6a7b10352526.png)
### Log Dataset
The log files are from a music streaming app based on specified configurations. For example, here are filepaths to two files in this dataset.
![image](https://user-images.githubusercontent.com/55506640/120908960-9708f100-c624-11eb-98b3-f13b572e95e1.png)
