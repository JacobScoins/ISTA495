Wite a SQL solution to output the population share (population of the country divided by the population of the world) of the countires.

SELECT name, population / (SELECT SUM(population) FROM world) as population FROM world 

