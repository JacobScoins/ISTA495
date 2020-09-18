Write a SQL solution to output the 10 countries who have the highest land share.

SELECT name, area / population FROM world
ORDER BY area / population DESC
limit 10