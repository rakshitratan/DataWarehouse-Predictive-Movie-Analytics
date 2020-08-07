# DataWarehouse-Predictive-Movie-Analytics
<h2> Developing the data warehouse and validate the facts.</h2>

<h3> 1.	Introduction: </h3>
The movie industry is multi trillion Euro industry, and it is one of the most influential mediums around the globe. It is the riskiest business to get into and being an investor or producer of a movie comes with high risk.
There are various external and internal factor involved for a movie to be a success. If we talk about risks a person going for a movie keep track of attributes like: “Director of the Movie”, “Actor”, “Language”, “Category” and etc before watching a movie and it is also associated with the geographical location where it is being launched.
Different movies depending on the “Category” it belonged attracts distinct crowd and as well as the Country in which it was launched cherishes the movie if the “Ticket price” is right.
In this project, we will use the IMDB-Movie rank data as well as the movie data from “rottentomato”, developing the data warehouse and validate the facts and will try to answer questions as an analyst for an Investment firm who wishes to invest in movies on the following criteria: <br>
•	Does the success of movie depend on the “Director” and “Actor”? <br>
•	Which type of movie category is mostly liked? <br>
•	Which county movie industry is profitable? <br>
•	Does success of the movie depend on its release date or month? <br>

<h3>2.	Data Sources: </h3>

•	Relational Dataset Repository - https://relational.fit.cvut.cz/ <br>
•	IMDB Rating website - https://www.imdb.com/chart/top/ <br>
•	List of Countries by Continent - http://statisticstimes.com/geography/countries-by-continents.php <br>

<h3> 3.	Data Model:</h3>

The objective of a data warehouse design is to create a schema that is optimized for decision support processing. The relational model is used in systems where many transactions are executed, most of them concurrently. A transaction inserts, updates or in any other way processes data in a database. In many occasions a transaction is an integral part of the business process. A Relational Database is a set of database tables that are related using keys from other database tables. 

![Alt Text](https://github.com/rakshitratan/DataWarehouse-Predictive-Movie-Analytics/blob/master/IMG-20200423-WA0016.jpg)
<center> Fig. ENTITY RELATIONSHIP DIAGRAM </center>

Each point of data in each data base can be split into two basic entities, namely attributes and measures. Dimensions or attributes are descriptive details about various objects allowing for their detailed analysis, measures are those that can be added across all dimensions. Measures are called facts. Facts are the reporting unit of any data warehouse, i.e. those are the ones that are manipulated, measured, and reported for analysis. Dimensions are those against which these facts are reported. So, it can be said that dimensions give extra information regarding the facts. A star schema consists of a central fact table which is linked directly to each of the dimension tables via a “one to one” OR “one to many” relationships.

![Alt Text](https://github.com/rakshitratan/DataWarehouse-Predictive-Movie-Analytics/blob/master/IMG-20200423-WA0022.jpg)
<center>Fig. STAR SCHEMA </center>

<h3>4.	Dimensions Tables:</h3>
•	Sale Dimension Table/SaleDim: The Sale dimension table consists of five attributes having Sales key as Primary Key, SalesId, No of Tickets sold, LocationId <br>
•	Date Dimension Table/DateDim: The data dimension table has 6 attributes with DateKey being the Primary Key<br>
•	Cast Dimension Table/CastDim: The cast dimension table has 10 distinct attributes with CastKey being the Primary Key<br>
•	Location Dimension Table/LocationDim: The location dimension table has 5 attributes with Locationkey being the Primary key<br>
•	Movie Dimension Table/MovieDim: The Movie dimension table has 8 attributes with MovieKey being the Primary Key.<br>

<h3> 5.	ETL Process:</h3>

An ETL process is defined for stage-wise loading of different data sources into raw data tables, generating dimensions and facts, and deploying the cube for further BI analysis. This ETL process is configured in Visual Studio(SSIS) tool for integration and different components are used to perform the process. The following 5 steps are configured in a sequential manner and triggered on successful completion of the prior task.

#To continue readig please click on the link: https://github.com/rakshitratan/DataWarehouse-Predictive-Movie-Analytics/blob/master/Rakshit%20Ratan-%20DataStorageAssignmentCA.docx


