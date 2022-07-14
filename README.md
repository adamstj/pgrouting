# pgrouting
## Create a road network database (pgrouting) using open-source data and software on Windows
In this tutorial we will set up a fully functional, fully open source, road network database. The database could for example be used for shortest path analysis (Dijkstra’s) or to create drive-time areas (Isochrones).

##### Example of a drive-time analysis conducted using pgrouting (5 min and 10 min walking distance):
![5 min and 5 min drive-time polygons](img/isochrone_300_600.JPG?raw=true "Title")

This tutorial does not intend to give an extensive guide to install and setup each software as there are many flavours to that and much better tutorials existing (some of which are linked to in this tutorial). Instead, it aims to fill the gap of going from A to B of enabling analysis on road data in a fully open-source way, available for anyone.

### Setup
#### Start by installing PostgreSQL and pgAdmin (if you don’t have it already).
Tutorials for installing PostgreSQL and pgAdmin can for example be found [here](https://www.postgresqltutorial.com/install-postgresql/).

#### Create your database using psql terminal
When you have installed PostgreSQL it is time to set up your database with its required extensions for road data. Pgrouting is the extension which enables setting up a road network database (you can read more about this [here](https://pgrouting.org/)). In turn Pgrouting makes use of another extension called PostGIS. PostGIS is an extension for PostgreSQL for spatial data structures (you can read more about this [here](https://postgis.net/)).

In psql terminal: \
```console
CREATE DATABASE city_routing; ^
connect city_routing;
CREATE EXTENSION pgrouting CASCADE;
```



```sql
select * from hej
```
