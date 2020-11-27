# Sparkify ETL Pipeline


##  1.Goal of the project 
---
This project is created in the course of a Udacity training on Data Engineering.
The fictional startup Sprkify wants to analyze data they have been collection on their new streaming app.
The main goal of this project is to bring the given data from JSON fromat into a given SQL schema in order to make it easy to query the data.



## 2. Files
---
The program cosits of the following files:

1. Data
Here the JSON files holding the data that is used in ETL process is stored. The folder is named *data*. 

2. create_tables.py 
    * This script creates first drops all potential previous version of the database tables.
    * Secondly the DDL statements that create the databse schema are created. 
    * Third the insert statements used in the etl.py script are defined.
    

3.  sql_queries
    * The sql_queries contains drop table statements in oder to delete old versions of the data & to make sure that the data can be created without collision. 
    * It also prvides the DDL statements and the DML statemtes that are needed to create the needed tabels and to fill them with the right data types. 
    
4. etl.py 
In this script the data is loaded from the JSON files if needed transformed into the needed foramt and then loaded into the database. 

    
5. etl.ipynb 
    * This file is not needed for the actuall programm but provides an overview on the development of the *etl.py* script and can be used for further          development 
    
6. test.ipynb
    * This file is also not needed in oder to perform the actuall ETL task but it provides an overview and tets if the data was transfromed and loaded as desired.
  


---
## 3. Structure 

The database schema holds the following tabels: 

    1. songplay - records in log data associated with song plays i.e. records with page NextSong
        - songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agen
        
    2. user - users in the app
        - user_id, first_name, last_name, gender, level
        
    3. song - songs in music database
        - song_id, title, artist_id, year, duration
        
    4. artist - artists in music database
        - artist_id, name, location, latitude, longitude
        
    5. time - timestamps of records in songplays broken down into specific units
        - start_time, hour, day, week, month, year, weekday

---
## 4. How to use

    1. Run the create_database.py from the console skript in order to create the needed structure on the database
    2. Run the etl.py also from the console scrip in order to fill the schema with the given data 
    
---

## 5. Required Installations

In order to run this program a python 3.7 installation is needed. Furthermore one must have accesss to a PostgreSQL database.
In order to connect the pythn environment with the PostgreSQL database the *psycopg2* package needs to be installed. 


## 6. 
    


