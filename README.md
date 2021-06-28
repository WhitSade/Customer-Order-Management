# Customer Order Management

This project demonstrates SQL join functions ( Inner, Left, Right, Cross, & Union) based on a database around a bookstore customer order management system.

Use bookstore;

SELECT o.itemid, c.customername
FROM orderinfo as o
Inner Join customer as c ON o.customerid=c.customerid;

SELECT i.booktitle, a.authorname
FROM item as i
Inner Join author as a On i.authorid=a.authorid;

SELECT i.booktitle, a.authorname
FROM item as i
LEFT JOIN author as a ON i.authorid=a.authorid
ORDER BY i.booktitle;

SELECT C.CUSTOMERNAME, O.ITEMID
FROM customer as c
LEFT JOIN orderinfo as o ON c.customerid=o.customerid
ORDER BY c.customername;

SELECT o.itemid, c.customername
FROM orderinfo as o
RIGHT JOIN customer as c ON o.customerid=c.customerid
ORDER BY c.customername;

SELECT a.authorname, i.booktitle
FROM author as a
RIGHT JOIN item as i on a.authorid=i.authorid
ORDER BY a.authorname;

SELECT e.firstname as EmployeeName, em.firstname AS ManagerName
FROM employees e
Inner Join employees em
On e.employeeid=em.employeeid;

SELECT *
FROM item
CROSS JOIN author;

SELECT a.authorname, i.booktitle
FROM author as a
INNER JOIN item as i On a.authorid=i.authorid;

SELECT * FROM supplier;

SELECT city From customer
UNION
SELECT city From supplier
ORDER BY city;

SELECT city From customer
UNION ALL
SELECT city From supplier
ORDER BY city;

SELECT customername FROM customer
UNION
SELECT firstname from employees
ORDER BY customername;
