---
layout: post
title: Fantastic Boolean Operators and Where to Find Them
---

By Rachel "Scamander" Sullivan

## Boolean Logic

Boolean logic is a simple but powerful concept that is the foundation of many mathematical and scientific fields.  It is fundamental to software programming, because it is able to help developers breakdown complex statements into easy to digest logical formulas. 

Boolean logic uses bools (true and false values) to organize information. Bools are typically denoted as T or 1 for true and F or 0 for false.  A Boolean operator in Java programming is an operator that returns a Boolean result that’s based on the Boolean result of one or two other expressions. Boolean variables can have two values - “true” or “false”.

## Using Boolean Logic on a single element

The negation operator is written as “~” for primitives and “!” for variables. The term “~a” is read as “not a”. When applied to bools, we can create a truth table to list all the possible logical outcomes.

## Truth Table for Negation

<style type="text/css">
	table.tableizer-table {
		font-size: 14px;
		border: 1px solid #CCC; 
		font-family: Verdana, Geneva, sans-serif;
	} 
	.tableizer-table td {
		padding: 4px;
		margin: 3px;
		border: 1px solid #CCC;
	}
	.tableizer-table th {
		background-color: #000000; 
		color: #FFF;
		font-weight: bold;
	}
</style>
<table class="tableizer-table">
<thead><tr class="tableizer-firstrow"><th>A</th><th>!A</th></tr></thead><tbody>
 <tr><td>T</td><td>F</td></tr>
 <tr><td>F</td><td>T</td></tr>
</tbody></table>

When considering a single variable boolean, we see that if a bool (a) is true than its opposite (!a) is false.  Likewise if a bool (a) is false, it’s opposite (!a) must be true. In Java, the ! operator returns true if the operand to the right evaluates to false.  It returns false if the operand to the right is true.

## Using Boolean Logic on two elements

Two more important Boolean operators are “And” and “Or”.  In Java, the comparison operator “And” is written “&&”, and "Or" is written as  two vertical lines.  Truth tables with two boolean elements are more complicated because we have to compare two bools to create our final true or false declaration.

## Truth Table for Or 

<style type="text/css">
	table.tableizer-table {
		font-size: 14px;
		border: 1px solid #CCC; 
		font-family: Arial, Helvetica, sans-serif;
	} 
	.tableizer-table td {
		padding: 4px;
		margin: 3px;
		border: 1px solid #CCC;
	}
	.tableizer-table th {
		background-color: #000000; 
		color: #FFF;
		font-weight: bold;
	}
</style>
<table class="tableizer-table">
<thead><tr class="tableizer-firstrow"><th>A</th><th>B</th><th>A or B</th></tr></thead><tbody>
 <tr><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
 <tr><td>T</td><td>T</td><td>T</td></tr>
 <tr><td>F</td><td>T</td><td>T</td></tr>
 <tr><td>T</td><td>T</td><td>T</td></tr>
 <tr><td>F</td><td>F</td><td>F</td></tr>
</tbody></table>


## Truth Table for And "&&"

<style type="text/css">
	table.tableizer-table {
		font-size: 14px;
		border: 1px solid #CCC; 
		font-family: Verdana, Geneva, sans-serif;
	} 
	.tableizer-table td {
		padding: 4px;
		margin: 3px;
		border: 1px solid #CCC;
	}
	.tableizer-table th {
		background-color: #000000; 
		color: #FFF;
		font-weight: bold;
	}
</style>
<table class="tableizer-table">
<thead><tr class="tableizer-firstrow"><th>A</th><th>B</th><th>A && B</th></tr></thead><tbody>
 <tr><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
 <tr><td>T</td><td>T</td><td>T</td></tr>
 <tr><td>F</td><td>T</td><td>F</td></tr>
 <tr><td>T</td><td>F</td><td>F</td></tr>
 <tr><td>F</td><td>F</td><td>F</td></tr>
 <tr><td></td></tr>
</tbody></table>

Included in the table below is a concept called “exclusive or”.  This is a logical concept that does not have a character exclusive operator in Java.  However, we can construct the logic behind it through a bit of code (seen in the table below) that combines the or and && operators. In simple language, exclusive or mean “this or that, but not both’.

## Truth Table for Exclusive Or

<style type="text/css">
	table.tableizer-table {
		font-size: 14px;
		border: 1px solid #CCC; 
		font-family: Verdana, Geneva, sans-serif;
	} 
	.tableizer-table td {
		padding: 4px;
		margin: 3px;
		border: 1px solid #CCC;
	}
	.tableizer-table th {
		background-color: #000000; 
		color: #FFF;
		font-weight: bold;
	}
</style>
<table class="tableizer-table">
<thead><tr class="tableizer-firstrow"><th>A</th><th>B</th><th>A XOR B</th></tr></thead><tbody>
 <tr><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
 <tr><td>T</td><td>T</td><td>F</td></tr>
 <tr><td>F</td><td>T</td><td>T</td></tr>
 <tr><td>T</td><td>F</td><td>T</td></tr>
 <tr><td>F</td><td>F</td><td>F</td></tr>
</tbody></table>

Boolean operators are used in loops to determine if the program should enter a loop, or continue to pass through a loop.  The table below contains some pseudocode examples and brief explanations.

<style type="text/css">
	table.tableizer-table {
		font-size: 12px;
		border: 1px solid #CCC; 
		font-family: Arial, Helvetica, sans-serif;
	} 
	.tableizer-table td {
		padding: 4px;
		margin: 3px;
		border: 1px solid #CCC;
	}
	.tableizer-table th {
		background-color: #000000; 
		color: #FFF;
		font-weight: bold;
	}
</style>
<table class="tableizer-table">
<thead><tr class="tableizer-firstrow"><th>Operator</th><th>Code</th><th>Explanation</th></tr></thead><tbody>
 <tr><td>!</td><td>if( !a){ //do code}</td><td>This will execute only if A is not true</td></tr>
 <tr><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
 <tr><td>||</td><td>if (a||b){ //do code }</td><td>This will execute as long as ONE of the elements is TRUE</td></tr>
 <tr><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
 <tr><td>&&</td><td>if (a&&b){ //docode}</td><td>This will execute ONLY if BOTH a and b are TRUE</td></tr>
 <tr><td>&nbsp;</td><td>&nbsp;</td><td>&nbsp;</td></tr>
 <tr><td>XOR</td><td>public static boolean logicalXOR(boolean x, boolean y) {  return ( ( x || y ) && ! ( x && y ) ); }</td><td>There is no character exclusive or operator in java.  However, one can create the logic though combining the || and && operators.  This will only execute if the truth values don't match. (One must be true and one must be false)</td></tr>
</tbody></table>

The examples above are all conditional boolean operators.  Java also has bitwise boolean operators with similar properties.  

## Bitwise Negation Truth Table

<style type="text/css">
	table.tableizer-table {
		font-size: 14px;
		border: 1px solid #CCC; 
		font-family: Verdana, Geneva, sans-serif;
	} 
	.tableizer-table td {
		padding: 4px;
		margin: 3px;
		border: 1px solid #CCC;
	}
	.tableizer-table th {
		background-color: #000000; 
		color: #FFF;
		font-weight: bold;
	}
</style>
<table class="tableizer-table">
<thead><tr class="tableizer-firstrow"><th>A</th><th>~A</th></tr></thead><tbody>
 <tr><td>T</td><td>F</td></tr>
 <tr><td>F</td><td>T</td></tr>
</tbody></table>
## Bitwise Or, And, and Exclusive Or Truth Table


<style type="text/css">
	table.tableizer-table {
		font-size: 14px;
		border: 1px solid #CCC; 
		font-family: Verdana, Geneva, sans-serif;
	} 
	.tableizer-table td {
		padding: 4px;
		margin: 3px;
		border: 1px solid #CCC;
	}
	.tableizer-table th {
		background-color: #000000; 
		color: #FFF;
		font-weight: bold;
	}
</style>
<table class="tableizer-table">
<thead><tr class="tableizer-firstrow"><th>a</th><th>b</th><th>a|b </th><th>a&b</th><th>a^b</th></tr></thead><tbody>
 <tr><td>0</td><td>1</td><td>1</td><td>0</td><td>1</td></tr>
 <tr><td>1</td><td>1</td><td>1</td><td>1</td><td>0</td></tr>
 <tr><td>0</td><td>0</td><td>0</td><td>0</td><td>0</td></tr>
 <tr><td>1</td><td>0</td><td>1</td><td>0</td><td>1</td></tr>
</tbody></table>

## Be careful!

When using boolean operators in Java, you have to be careful. There are fundamental differences between “&” and “&&”  and “|” and “||”. The single & and | REQUIRE the compiler to look at both conditions.  In contrast, as soon as the compiler sees that && and or has reached inevitability, it stops comparing and doesn’t validate the rest of the statement is true. 

## Keep Looking

You may have noticed that, despite the title of this post, you only spotted 8 boolean logical operators. What are the other 8 operators you ask?  Despite consulting with multiple expert programmers, the author was unable to identify the additional 8 rumored to be used in programming.  There was some speculation among the experts polled that comparison statements like !=, <, >, <=, >=, could be considered conditional boolean expressions.  In the search for the elusive 8 operators, even = and == were considered. However, no consensus could be reached in the time allotted since the expert programmers had to go to bed early. One can hope that, in the future, exciting new research will merit follow up post detailing the mysterious additional boolean operators.
