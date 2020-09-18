Write a SQL solution to output the 10 least dense countries.


SELECT name, population / area FROM world
ORDER BY population / area ASC
limit 5
