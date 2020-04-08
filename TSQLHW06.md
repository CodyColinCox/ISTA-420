### TSQLHW06
## Cox, Cody C.

1. What does a set operator do?

Set operator compares complete rows between the results of two input queries involved.**

1. What are the general requirements of a set operator

The typically requirements for a set operator are input from two input query.**

1. What is a Venn Diagram? This is not in the book.

A Diagram that shows all the possible logical relations between a collections of different sets.**

1. Draw a Venn Diagram of the UNION operator. What does it do?

SELECT country, region, city from HR.employees
      UNION
      SELECT country, region city from Sales.Customers**

      **It returns results from both tables but eliminates duplicates.**

1. Draw a Venn Diagram of the UNION ALL operator. What does it do

    SELECT country, region, city FROM HR.employees
    UNION ALL
    SELECT country, region, city FROM Sales.Customers**

    Union all unifies the two input query results without attempting to remove duplicates from the results.**

1. Draw a Venn Diagram of the INTERSECT operator. What does it do?

    SELECT country, region, city FROM HR.employees
    INTERSECT
    SELECT country, region, city FROM Sales.Customers**

     **This operator only returns rows that are common to results of the two input queries.**


1. If SQL Server supported the INTERSECT ALL operator, what would it do?

   duplicates of the intersects will not be removed.**

1. Draw a Venn Diagram of the EXCEPT operator. What does it do?

     SELECT country, region, city FROM HR.Employees
     EXPECT
     SELECT country, region, city FROM Sales.Customers**

     Returns only distinct rows that appear in the first set but not the second. In other words, a row is returned once the outputs as long as it appears at least once in the fist input multiset and zero times in the second.**

1. If SQL Server supported the EXCEPT ALL operator, what would it do?

    It will only return occurrences of a row from the first multiset that do not have a corresponding occurrence in the second.**


1. What is the precedence of the set operators?

    Intersect comes first. UNION and EXPECT depends on order of precedence.**

1. The symmetric difference of two sets A and B is all elements in A that are also not in A and B, and all elements of B that are also not in A and B. For example, if set A consisted of all integers between 1 and 100 that are divisible by 2, and set B consisted of all integers between 1 and 100 that are divisible by 3, the symmetric difference of A and B would include all integers in A and B *except* integers divisible by both 2 and 3, e.g., 6, 12, 18, etc. Write a SQL query that computes the symmetric difference of two tables A and B.

    Select all integers / 2 from tables A
    Expect
    Select all integers / 3 from tables B;
