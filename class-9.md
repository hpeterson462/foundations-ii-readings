# Articles

## *Database Normalization*

* Database normalization is a process used to organize a database into tables and columns
* A table should be about a specific topic and only supporting topics included
    * Reduce duplicate data
*  3 reasons for normalized database:
    * minimize data duplication
    * avoid data modifications
    * simplify queries
* Update Anomaly
    * if we don't update all rows, then inconsistencies appear
* Deletion Anomaly
    * causes removal of more than one set of facts
* Eliminate or reduce these anomalies by separating the data into different tables
    * tables serving a single purpose
* Forms are progressive
    * To qualify for 3rd normal form - a table must first satisfy the rules for 2nd normal form, and 2nd normal form must adhere to those for 1st normal form

## *Visual Representation of SL Joins*

* Inner Join
    * `A -- B`
    * return all records in table A that have matching record in table B
    * `SELECT <select_list> 
FROM Table_A A
INNER JOIN Table_B B
ON A.Key = B.Key`
* Left Join
    * `A-- B`
    * return all of the records in table A regardless if any of those records have a match in table B
    * `SELECT <select_list>
FROM Table_A A
LEFT JOIN Table_B B
ON A.Key = B.Key`
* Right Join
    * `A --B`
    *  return all of the records in table B regardless if any of those records have match in table A
    * `SELECT <select_list>
FROM Table_A A
RIGHT JOIN Table_B B
ON A.Key = B.Key`
* Outer Join (Full Outer Join or Full Join)
    * `A--B`
    * return all of the records from both tables
    * `SELECT <select_list>
FROM Table_A A
FULL OUTER JOIN Table_B B
ON A.Key = B.Key`
* Left Excluding Join
    * `A- B`
    * l return all of the records in table A that don't match records in table B
    * `SELECT <select_list> 
FROM Table_A A
LEFT JOIN Table_B B
ON A.Key = B.Key
WHERE B.Key IS NULL`
* Right Excluding JOIN
    * `A -B`
    *  return all of the records in table B that don't match any records in table A
    * `SELECT <select_list>
FROM Table_A A
RIGHT JOIN Table_B B
ON A.Key = B.Key
WHERE A.Key IS NULL`
* Outer Excluding JOIN
    * `A- -B`
    *  return all of the records in table A and all records in table B that don't match
    * `SELECT <select_list>
FROM Table_A A
FULL OUTER JOIN Table_B B
ON A.Key = B.Key
WHERE A.Key IS NULL OR B.Key IS NULL`
