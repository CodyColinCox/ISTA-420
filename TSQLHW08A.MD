## HW08A
## Cox, Cody C.

1. When using INSERT, is the list of columns necessary? Why or why not?
Specifying the target column names right after the table name is optional, but by doing so, you control the value-column associations instead of relying on the order of the columns in the CREATE TABLE statement.

1. When using INSERT SELECT, do you use a subquery (derived table)? Under what circumstances do you not use a subquery?
Yes,
1. What is the operand for the INSERT EXEC statement?
A stored procedure.

1. How would you use the INSERT INTO statement?
You select the tables you want to insert and put it into the dbo that you want to have it in.

1. What are the parameters to the BULK INSERT statement?
 the data file type (for example, char or native), the field terminator, the row terminator, and others—all of which are fully documented.

1. Does IDENTITY guarantee uniqueness? If not, how do you guarantee uniqueness?
No, Scope Identity

1. How do you create a SEQUENCE object?
CREATE SEQUENCE command.

1. How do you use a SEQUENCE object?
Guarantee uniqueness

1. How do you alter a SEQUENCE object?
To change the data type, drop and create the sequence object.


1. What is the diﬀerence between DELETE and TRUNCATE?
Delete will delete the identified parameters and truncate will delete all the rows in a table.

1. What is the diﬀerence between DELETE and DROP TABLE?
Delete will remove the data and drop table will remove the data and the table structure.
