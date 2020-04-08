### TSQLHW05
## Cox, Cody C.

1.  What is a table expression? Can you give a technical deﬁnition of a table expression?
A named query expression that represents a valid relational table.

1.  In what SQL clause are derived tables (table valued subqueries) located?
Defined in the FROM clause of an outer query. Their scope of existence is the outer query. As soon as the outer query is finished, the derived table is gone.

1.  Why can you refer to column aliases in an outer query that you deﬁned in an inner table valued subquery?
because the select statement assigns the aliases in the subquery.

1. What SQL key word deﬁnes a common table expression?
WITH

1. When using common table expressions, can a subsequent derived table use a table alias declared in a preceding table expression
No, because derived table utilizes the from clause.

1. Can a main query refer to a previously deﬁned common table expression by multiple aliases?
Yes, because it has already been defined therefore can be pulled.

1. In SQL, is a view a durable object?
No, because the view has a material database within itself.

1. In a view, what does WITH CHECK OPTION do? Why is this important?
Prevents modification through the view that conflict with the filter.

1. In a view, what does SCHEMABINDING do? Why is this important?
 it binds the schema of referenced objects and columns to the schema of the referencing object. It indicates that referenced objects cannot be dropped and that referenced columns cannot be dropped or altered.

1. What is a table valued function?
Inline TVFs are reusable table expressions that support input parameters. A function that returns a table.

1. What does the APPLY operator do?
Acts as a JOIN table operator however, the APPLY operator does it worth within the logical-query phases.

1. What are the two forms of the APPLY operator? Give an example of each.
Cross APPLY: Implements one logical query processing phase. It applies the right table to each row from the left table and produces a result table with the unified result sets.
Outer Apply: Implements two logical query processing phase.
