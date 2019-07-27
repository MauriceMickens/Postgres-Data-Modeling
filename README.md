# Data Modeling with Postgres

This project builds an ETL pipeline and database for a fictional startup called Sparkify.

*Databse Modeling Purpose
- This project aims to model music streaming data as a service provided by Sparkify
- Final model will help analytical team to query and visualize the data for specific reports 

## Database schema design and ETL process
The database utilizes a star schema design. 
Pros
- Denormalization
- Simplified queries
- Fast aggregations.

 We perform ETL on the first dataset of json files, song_data, to create the songs and artists dimensional tables. Then we run ETL on the second dataset, log_data, to create the time and users dimensional tables, as well as the songplays fact table.

Fact Table
- songplays - records in log data associated with song plays i.e. records with page NextSong

Dimension Tables
- users - users in the app
- songs - songs in music database
- artists - artists in music database
- time - timestamps of records in songplays broken down into specific units

## Usage Example
From your project directory, run below command to create tables:
`python create_tables.py`

Now run the following, to populate your tables from the json files:
`python etl.py`

## Credits
[Udacity Data Engineering Course](https://www.udacity.com/course/data-engineer-nanodegree--nd027)