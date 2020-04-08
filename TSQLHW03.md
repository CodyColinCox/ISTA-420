###TSQL03
##Cox, Cody C.

1. In general, why would you even want to join two (or more) tables together? This is a good time to
think about the nature of relational algebra.
- To pull together information that is related and display it in a table

1. Describe in your own words the output from an inner join.
- it selects records that match in both tables.

1. Describe in your own words the output from an outer join.
- It returns the values that do have matches and it returns the values don't. and returns null.

1. Describe in your own words the output from an cross join.
- you get each possible combination of data from the two tables.
- rows from first table are multiplied by rows in second table.

1. A convenient mnemonic for remembering the various joins is \Ohio." Why is this true?
- round on the ends and high in the middle

1. Give an example of a composite join.
- A composite join matches multiple attributes:
- From dbo.Table1 as T1
  Inner Join dbo.Table2 as T2
      ON T1.col1 = T2.col1
      AND T1.col2 = T2.col2

1. What is the difference between the following two queries? The business problem is How many orders
do we have from each customer?"
================first query===============
SELECT C.custid, COUNT(*) AS numorders
FROM Sales.Customers AS C
LEFT OUTER JOIN Sales.Orders AS O
ON C.custid = O.custid
GROUP BY C.custid;
================second query===============
SELECT C.custid, COUNT(O.orderid) AS numorders
FROM Sales.Customers AS C
LEFT OUTER JOIN Sales.Orders AS O
ON C.custid = O.custid
GROUP BY C.custid;
- In the first one, the COUNT( * ) will count all rows whether or not they actually have orders
- where as the second one COUNT(O.ORDERID) will count the orders for each customer

1. What might be one reason the following query does not return the column custID in this query?
SELECT C.custid, C.companyname, O.orderid, O.orderdate
FROM Sales.Customers AS C
LEFT OUTER JOIN Sales.Orders AS O
ON C.custid = O.custid
WHERE O.orderdate >= '20160101';
- Any value with a NULL value be discarded because of the >= sign.
