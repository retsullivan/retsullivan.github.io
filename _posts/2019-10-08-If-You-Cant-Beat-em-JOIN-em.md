---
layout: post
title: If You Can't Beat em, JOIN em
---

## Visualizing the JOIN command in SQL

Many websites I visited when trying to figure out how JOIN commands work in SQL had Venn Diagrams to illustrate how they worked:

![](https://www.got-it.ai/solutions/sqlquerychat/wp-content/uploads/2019/05/Screen-Shot-2019-05-26-at-8.44.39-AM.png)

Since I found it challenging to understand exactly what is happening when you JOIN tables in SQL, I made some diagrams of what the different types of JOIN commands do to the tables based on my notes from today. 

**Inner Join**

This type is like an *intersection* in a venn diagram.

Here is my example using psedo tables:

![](https://raw.githubusercontent.com/retsullivan/retsullivan.github.io/master/images/JOIN%20tables_Inner%20Join.jpg)

You can see that an inner join only returns the stuff the two tables have in common.

**Full Join**

This type is like a *union* in a venn diagram.

Here is my example using psedo tables:
![](https://raw.githubusercontent.com/retsullivan/retsullivan.github.io/master/images/JOIN%20tables_FUll%20Join.jpg)

You can see that a full join returns all the unique columns from both tables.  

**Left Join & Right Join**

A **left join** will give you everything in the first table, plus the data connected to the column(s) that you a joining on. Here is my example using psedo tables:

![](https://raw.githubusercontent.com/retsullivan/retsullivan.github.io/master/images/JOIN%20tables_Left%20Join.jpg)

A **right join** will give you everything in the second table, plus the data connected to the column(s) that you a joining on. Here is my example using psedo tables:

![](https://raw.githubusercontent.com/retsullivan/retsullivan.github.io/master/images/JOIN%20tables_Right%20Join.jpg)

You can see here that the order than you join tables is important (the right and left join of the two tables gave us very different shapes). 

**Cross Join**

This type of join doesn't translate well into a venn diagram picture.  It is a new table that contains every possible combination of the elements in the tables that are being joined. Here is my example using psedo tables:

![](https://raw.githubusercontent.com/retsullivan/retsullivan.github.io/master/images/JOIN%20tables_Cross%20Join.jpg)

These examples don't cover edge cases, but hopefully it's a good way to think about the big picture.
