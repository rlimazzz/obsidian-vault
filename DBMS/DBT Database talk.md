Important: Sql is based on bags(duplicates) not sets(no duplicates).

Aggregates : functions that return a single value from a bag of tuples : AVG(col), MIN(col), MAX(col), SUM(col), COUNT(col).

Group By: Project tuples into subsets and calculate aggregates against each subset.

Grouping Sets: Specify multiple groupings in a single query instead of using UNION ALL to combine the results of several individual GROUP BY queries.