1. Download and install PostgreSQL database (it is available at https://www.postgresql.org)
2. Create a database and name it as ISTA495.practicum
3. Ctreat the following table:
  - table name: world
  - table columns: id, name, continent, area, population, migrants,fertility,medianage,urbanpopulation (id is a number and it is the primary key, name and continent are strings, area and population are numbers)
4. Populate the world table using the csv file included in this folder

create temporary table t (id,country text,population text,yearlychange text,netchange text,area text,migrants text,fertility text,medianage text,urbanpopulation text);

copy t (id,country,population,yearlychange,netchange,area,migrants,fertility,medianage,urbanpopulation)

from 'C:\Program Files (x86)\CSVfile\world.csv'

with (format csv);

insert into world (id, country, population, area, migrants, fertility, medianage, urbanpopulation)

select id, country, population, area, migrants, fertility, medianage, urbanpopulation

from t;

drop table t
