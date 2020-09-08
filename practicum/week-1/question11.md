Write a SQL solution to output the 10 countries who have the lowest land share.


SELECT name, area / population FROM world

ORDER BY area / population ASC

limit 10
