<!-- PROJECT LOGO -->
<br />

<p align="center">
     <a href="https://github.com/Abanoub-20180003/Data-Modeling-with-Apache-Cassandr">
      <img src="./images/cassandralogo.png" alt="Logo" width="200" height="200">
     </a>
      <h3 align="center">Data Modeling ETL with Apache Cassandra</h3>
  

</p>

> apache, cassandra, nosql, data engineering, ETL, data modeling

## About The Project
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. 
the data reside in a directory of CSV files on user activity on the app.They'd like a data engineer to create a Apache Cassandra database which can create queries on song play data to 
answer the questions and make meaningful insights. The role of this project is to create a database schema and ETL pipeline for this analysis. 

### Project Description 
In this project, we will model the data with Apache Cassandra and build an ETL pipeline using Python. 
The ETL pipeline transfers data from a set of CSV files within a directory to create a streamlined CSV file to model and insert data into Apache Cassandra tables.
We will create separate denormalized tables for answering specific queries, 
properly using partition keys and clustering columns.

### Built With

* python
* Apache Cassandra
* iPython notebooks

### Dataset

#### Event Dataset

Event dataset is a collection of CSV files containing the information of user activity across a period of time.  Each file in the dataset contains the information regarding the song played, user information and other attributes . 

List of available data columns :

```
artist, auth, firstName, gender, itemInSession, lastName, length, level, location, method, page, registration, sessionId, song, status, ts, userId
```



The keyspace design is shown in the image below. Each table is modeled to answer a specific known query. This model enables to query the database schema containing huge amounts of data. Relational databases are not suitable in this scenario due to the magnitude of data. 

![database](./images/keyspace.png)

## Project structure

Files in this repository:

|     File / Folder      |                         Description                          |
| :--------------------: | :----------------------------------------------------------: |
|       event_data       | Folder at the root of the project, where all user activity CSVs reside |
|         images         |  Folder at the root of the project, where images are stored  |
| event_datafile_new.csv | Contains the data after merging the CSV files at `event_data` |
|    Project 2.ipynb     | iPython notebook containing the ETL pipeline including data extraction, modeling and loading into the keyspace tables. |
|         README         |                         Readme file                          |


## Getting Started

Clone the repository into a local machine using

```sh
git clone https://github.com/Abanoub-20180003/Data-Modeling-with-Apache-Cassandr.git
```

### Prerequisites

These are the prerequisites to run the program.

* python 3.7
* Apache Cassandra
* cassandra python library

### How to run

Follow the steps to extract and load the data into the data model.

1. Run `ETL.ipynb` iPython notebook
2. Run Part 1 to create `event_datafile_new.csv` 
3. Run Part 2 to initiate the ETL process and load data into tables 
4. Check whether the data has been loaded into database by executing `SELECT` queries

## Contact

Abanoub Kamal - abanoubkamalattia@gmail

Project Link: [https://github.com/Abanoub-20180003/Data-Modeling-with-Apache-Cassandr](https://github.com/Abanoub-20180003/Data-Modeling-with-Apache-Cassandr)


