# Project: Data Modeling with Postgres
## Introduction
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app. <br>
Creating a Postgres database with tables designed to optimize queries on song play analysis. Creating a database schema and ETL pipeline for this analysis and test the database and ETL pipeline by running queries given to you by the analytics team from Sparkify and compare the results with their expected results.
## Project Description
Data modeling with Postgres, define fact and dimension tables for a star schema for a particular analytic focus.<br>
Building an ETL pipeline using Python, transfers data from JSON files in two local directories into these tables in Postgres using Python and SQL.
## Project Datasets
### Song Dataset
Each file is in JSON format and contains metadata# about a song and the artist of that song. The files are partitioned by the first three letters of each song's track ID. For example, here are filepaths to two files in this dataset. (# Metadata is data that provides information about other data.For example, in a database, metadata could describe the schema (table names, column names, data types)
```
song_data/A/B/C/TRABCEI128F424C983.json
song_data/A/A/B/TRAABJL12903CDCF1A.json
```
And below is an example of what a single song file, TRAABJL12903CDCF1A.json, looks like.
``` JSON
{
  "num_songs": 1,
  "artist_id": "ARJIE2Y1187B994AB7",
  "artist_latitude": null,
  "artist_longitude": null,
  "artist_location": "",
  "artist_name": "Line Renaud",
  "song_id": "SOUPIRU12A6D4FA1E1",
  "title": "Der Kleine Dompfaff",
  "duration": 152.92036,
  "year": 0
}
```
### Log Dataset
The log files are from a music streaming app based on specified configurations. For example, here are filepaths to two files in this dataset.<br>
```
log_data/2018/11/2018-11-12-events.json
log_data/2018/11/2018-11-13-events.json
```
```JSON
{
  "artist": "Pavement",
  "auth": "Logged In",
  "firstName": "Sylvie",
  "gender": "F",
  "itemInSession": 0,
  "lastName": "Cruz",
  "length": 99.16036,
  "level": "free",
  "location": "Washington-Arlington-Alexandria, DC-VA-MD-WV",
  "method": "PUT",
  "page": "NextSong",
  "registration": 1540266185796.0,
  "sessionId": 345,
  "song": "Mercy:The Laundromat",
  "status": 200,
  "ts": 1541990258796,
  "userAgent": "\"Mozilla/5.0 (Macintosh; Intel Mac OS X 10_9_4) AppleWebKit/537.77.4 (KHTML, like Gecko) Version/7.0.5 Safari/537.77.4\"",
  "userId": "10"
}
```
## Data Modeling
Using the Star Schema: one fact table consist of the measures associated with each event songplays, and referencing four dimensional tables songs, artists, users and time, each with a primary key that is being referenced from the fact table.<br>
![image](https://github.com/MengyaCao/Data-Modeling-with-Postgres/blob/main/ER_Diagram_DM.JPG)
## Project Template
The data files, the project includes seven files:<br>
`create_tables.py`: drops and creates your tables. You run this file to reset your tables before each time you run your ETL scripts.<br>
`etl.ipynb`: reads and processes a single file from song_data and log_data and loads the data into your tables. This notebook contains detailed instructions on the ETL process for each of the tables.<br>
`etl.py`: reads and processes files from song_data and log_data and loads them into your tables. You can fill this out based on your work in the ETL notebook.<br>
`README.md`: provides discussion on this project.<br>
`ER_Diagram.png`: ERD for star schema of this project<br>
`sql_queries.py`: contains all your sql queries, and is imported into the first three files above.<br>
`test.ipynb`: displays the first few rows of each table to let us check on the database.
## How to Run
Run `create_tables.py` to create the database and tables.<br>
Run `etl.py` to build ETL pipeline for loading, extracting and inserting the data.<br>
Run `test.ipynb` to confirm the creation of database and columns.
