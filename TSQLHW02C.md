###TSQLHW02C
##Cox, Cody C.

1. DATETIME AND SMALLDATETIME (LEGACY), DATE, TIME, DATEIME2, DATETIMEOFFSET.
1. T-SQL does not provide the means to express a date and time literal; instead you have to specify a literal of a different type that can be converted- explicitly or implicitly- to a date and time data type.
1. which determines how SQL Server interprets the literals you enter when they are converted from a character-string type to a date and time type.
1. SET LANGUAGE GERMAN; SELECT CAST('02/12/2016' AS DATE);
1. Cast- interpreted exactly how it is written. Convert, change how the layout is set up. Parse, 1. Cast- interpreted exactly how it is written. Convert, change how the layout is set up. Parse, By using this function, you can parse a value as a requested type and indicate the culture.
1. GETDATE
1. SELECT DATEADD(YEAR, 1, "20200127"), SELECT DATEADD(MONTH,1, "20200127"), SELECT DATEADD(WEEK,1, "20200127"), SELECT DATEADD(DAY,1, "20200127"),
1. SELECT DATEDIFF(year, '1994/07/04', '2020/01/27') AS DateDiff;
1. ISDATE
1. Gives the last day of the month, when payments are due.
1. SELECT DAY(EOMONTH('2020-01-27')) days;
1. SELECT DATEDIFF(day, getdate(), '2020/06/08') AS DateDiff;
