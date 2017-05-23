![GitHub Logo](https://s3.ap-south-1.amazonaws.com/greyatom-social/GreyAtom-logo.png)

# FULL JOINS

The SQL FULL JOIN combines the results of both left and right outer joins.

The joined table will contain all records from both the tables and fill in NULLs for missing matches on either side.

### Syntax

The basic syntax of a FULL JOIN is as follows −

        SELECT table1.column1, table2.column2...
        FROM table1
        FULL JOIN table2
        ON table1.common_field = table2.common_field;

Here, the given condition could be any given expression based on your requirement.

### Example

Now, let us join these two tables using the FULL JOIN as follows.

        SELECT  Customers.CustomerID, Customers.CustomerName, ORDERS.OrderDate
            FROM Customers
            FULL JOIN ORDERS
            ON Customers.CustomerID = ORDERS.CustomerID;

This would produce the following result −

| CustomerID | CustomerName | OrderDate |
| ---------- | --------- | --------- |
| 51 | Bottom-Dollar Marketse	| 2017-03-20 |
| 71 | Split Rail Beer & Ale | 2016-11-21 |
| 72 | Princesa Isabel Vinhoss	| 2016-12-29 |
| 73 | Folk och fä HB	| 2017-01-04 |
| 74 | Consolidated Holdings	| 2017-03-28 |

If your Database does not support FULL JOIN (MySQL does not support FULL JOIN), then you can use UNION ALL clause to combine these two JOINS as shown below.