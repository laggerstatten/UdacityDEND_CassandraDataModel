# BACKGROUND

## Fictional
Sparkify is an online music streaming service, in which users can select songs to listen to and play them. The company records these listening events and has demographic information about their users. Additionally they have information about the music in their collection. The Sparkify team wants to combine information from their listening events log with their song information in order to gain insight into user behavior. This database exists in order to synthesize data from two separate data sets, a log of customer listening events and information describing songs in the library.

## Real
Sparkify is a model of an online music streaming service, similar to Spotify or Pandora. The dataset for the songs comes from the [Million Song Dataset] (http://millionsongdataset.com/) and the dataset for the user behavior was generated using the [Eventsim event simulator] (http://millionsongdataset.com/). The database is implemented using Python and Cassandra.


# STRUCTURE & ETL PIPELINE

The ETL process is designed around the queries which will be run against the finished database. These include:

1. Query artist, song title, and song length, given session ID and Item in Session
2. Query artist, song, and user name, given user ID and session ID
3. Query user name, given song title

Data about songs and song play events are found in a CSV file. This CSV file contains more data than is used for the Sparkify project, so during the ETL process, only the relevant columns are preserved. These are the fields present in the select, where, or order by clauses of the CQL statement.


# INSTRUCTIONS

This process is run from the Jupyter notebook **Project_1B_Project_Template.ipynb**


