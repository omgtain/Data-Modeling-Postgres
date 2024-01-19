# Sparkify Background:
Sparkify is a startup company, they have a new music streaming app that collects data on songs and user activity. 

# Database Purpose:
The data that Sparkify collects is stored as .json files which aren't easily queried. The analytics team is interested in what users are listening to and would like a Postgres database that will allow for data to be queried and optimized for song play analysis. The databse (sparkifydb) will use an ETL pipeline for this analysis. 

# Files:
**data** - contains 2 folders, song_data & log_data
***song_data*** - (within data folder) this folder contains .json files that will fill the songs & artists tables
***log_data*** - (within data folder) this folder contains .json files that will fill the users, time, & songplays tables
**create_tables.py** - a python file that creates the database (sparkifydb) and tables for data storage
**etl.py** - a python file that that reads the song_data & log_data files, processes the files, and uses sql_queries.py to insert the data into sparkifydb.
**sql_queries.py** - a python file that stores SQL statements (drop table, insert, etc.)
**etl.ipynb** - a python jupyter notebook file to explore data & test the ETL process
**test.ipynb** - a python jupyter notebook file that contains test queries to ensure the database was created and filled with rows properly

# How to Run Python Scripts:
**1.** Open test.ipynb
**2.** At the top there are two %run lines, these will run the python files
**3.** Run create_tables.py - creates database and tables
**4.** Run etl.py - reads in .json files, processes and inserts them into sparkifydb
**5.** Run test.ipynb to ensure that records were successfully inserted into sparkifydb
