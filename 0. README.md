## **A SIMPLE SQL PROJECT** (0. README)
---
### 0.0 tl;dr

Simple SQL project using Python, Colab and other tools to perform queries and display relational-database knowledge, all the way from database architecture to select statements.
___
### 0.1 PROJECT PURPOSE AND CONCEPTION

The main purpose of this project is to show SQL knowledge. Syntax, concepts and manipulation, in general. Additionally, during the project, as per discussed below, other skills are also displayed. Finally, this serves as a general guide for daily SQL use.

Initially, to fulfill the purpose, only the author's streaming history on Spotify was going to be used - one can ask one's own streaming history from Spotify directly from the platform. Their response was a .zip folder with a main file called "StreamingHistory0" in JSON format. Sadly, however having extreme amounts of data from tracks and artists, on said file the platform only put together only a few pieces of information from each listening instance: "track name", "artist", "msplayed" (or track total time played) and "endtime". This created a new necessity, as well as an opportunity: to have a more interesting dataset, an API was used to supplement the data.

___
### 0.2 DATA AND TOOLS USED
1. Author's streaming history on Spotify from March to May 2022;
2. Supplemental music data, collected from an API called "TheAudioDB";
3. Google Colab;
4. DB Browser for SQLite
---
### 0.3 SKILLS SHOWN
1. General SQL usage and concepts;
2. General Python coding;
3. DataFrame manipulation (pandas);
4. Integration with JSON format;
5. API requests;
6. Data visualizations.
___

### 0.4 PREMISES
1. SQL SCHEMA: in order to really take advantage of the computational optimization given by SQL, some "relational-database architecture" concepts were assumed from the beginning. 
+ Little to no text repetition;
+ Splitting the data into fact and dimension tables for organization;
+ Connection between tables were to be made using primaries and foreign keys;
+ Autoincrement capacities and type restraints were to be used to further validate data.

<img width="1295" alt="SQL SCHEMA" src="https://user-images.githubusercontent.com/108877184/177785522-ba643b57-2da8-401a-b1bb-79c7407a491c.png">

2. DROPNA: values the API could not return (like song durations or album it did not have on its own dataset) were considered to be unhelpful. On a different project, this would be dealt fairly differently, but since for the project at hand these values would have no impact (positive or negative) they were later dropped.

3. SQLite: it might not be considered the most sophisticated RDMS for production, however, it is notably simple to set up and all the SQL syntax used on the project can be either applied directly or easily adapted. 
___

### 0.5 PIPELINE (PROJECT PHASES)

<img width="1680" alt="PROJECT PIPELINE" src="https://user-images.githubusercontent.com/108877184/177795696-949542d9-d961-4516-a555-6295c299b67e.png">

___

### 0.6 FURTHER DEVELOPMENT SUGGESTIONS

Some notes and ideas to build on this project and make it even more interesting.

1. Use a different API: it is possible to see a good amount of the data from Latin music could not be retrieved. Besides, a few categories absent here could have been nice to explore, such as retrieving tracks (or albums) release dates and ranking decades by most instances on the dataset;
2. Get a larger sample: while the study was valid, having more data usually means better. Therefore, following the streaming history for a few years might be subject to catch momentary catch songs and changes on music taste;
3. Attribute (or collect) ratings for each of the songs and build a recommender system on top of it. Other features can also be used, such as track volume, rhythm, lyrics content and pace.
