Write a SQL solution to output the 10 most dense countries.

SELECT name, population / area FROM world

ORDER BY population / area DESC

limit 5
