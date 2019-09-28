---
layout: post
title: Sign Up TODAY, And Get A Free Delimited Data Plan
---

In today's lesson, we learned about Data Structures. The table below shows the 4 basic delimitation patterns used to seperate data. 

<table>
    <tr>
        <td>Delimitation Pattern</td>
        <td>Syntax</td>
    </tr>
    <tr>
        <td>Postfix</td>
        <td>a\|b\|c\|</td>
    </tr>
    <tr>
        <td>Prefix</td>
        <td>\|a\|b\|c</td>
    </tr>
    <tr>
        <td>Infix</td>
        <td>a\|b\|c</td>
    </tr>
    <tr>
        <td>Outfix</td>
        <td>\|a\|b\|c\|</td>
    </tr>
</table>


Many languages have been develoiped to work with data structures. For today's homework, we were asked to convert the following information into JSON and XML:

*  First Name : Tim 
*  Last Name : Rayburn 
*  Address Line 1 : 5445 Legacy Drive 
*  Address Line 2 : Suite 100
*  City : Plano 
*  State : TX 
*  Zip : 75024
 

**XML**

Here is the homework data expressed in XML:


```xml
<?xml version="1.0" encoding="UTF-8" ?>
<root>
    <row><Element>First Name</Element><Name>Tim</Name></row>
    <row><Element>Last Name</Element><Name>Rayburn</Name></row>
    <row><Element>Address Line 1</Element><Name>5445 Legacy Drive</Name></row>
    <row><Element>Address Line 2</Element><Name>Suite 100</Name></row>
    <row><Element>City</Element><Name>Plano</Name></row>
    <row><Element>State</Element><Name>Zip</Name></row>
    <row><Element>Zip</Element><Name>75024</Name></row>
</root>
```

**Important takeaways about XML (Extensible Markup Language):**




<table>
        <tr>
        <td>elements</td>
        <td>Everything from (including) the element's start tag to (including) the element's end tag. An element can have an attribute(s) associated with it.</td>
    </tr>
    <tr>
        <td>attributes</td>
        <td>Attributes are part of XML elements. Atributes define properties of elements. An XML attribute is always a name-value pair.</td>
    </tr>
    <tr>
        <td>schema</td>
        <td>An XML schema represents the interrelationship between the attributes and elements of an XML object</td>
    </tr>
    <tr>
        <td>data types</td>
        <td>Elements in XML can only contain text, but the text can describe many different types. It can be one of the types included in the XML Schema definition (boolean, string, date, etc.), or customized.</td>
    </tr>
</table>


**JSON - JavaScript Object Notation**

Here is the homework data expressed in JSON:

```json
[
    {"Element": "First Name", "Name": "Tim"},
    {"Element": "Last Name", "Name": "Rayburn"},
    {"Element": "Address Line 1", "Name": "5445 Legacy Drive"},
    {"Element": "Address Line 2", "Name": "Suite 100"},
    {"Element": "City", "Name": "Plano"},
    {"Element": "State", "Name": "Zip"},
    {"Element": "Zip", "Name": "75024"}
]
```

**JSON Notation Explaination**

```json
{
Starts a new file in JSON


“name”:”Tim Rayburn”, 
 “hitPoints”: 100,
  “Tags”: [“mean”,”good”] 
“Location”: {
  “name”:”The Deathly Hallows”,
  “Description”:“Haunting vibe”
}
}
```

Note that:
* {  } are outfix (and can be nested for objects inside objects)
* Colon is infixed
* Infixed Comma after the data to indicate next property
* 100 is not in quotes since it’s a number
* Fullfixed square brackets [  ] for arrays
                 

**Only 4 Data Types in JSON**

Unlike most modern programing langues, JSON only has 4 data types. 

<table>
    <tr>
        <td>Delimeter</td>
        <td>Syntax</td>
    </tr>
    <tr>
        <td>Object</td>
        <td>{  } </td>
    </tr>
    <tr>
        <td>String</td>
        <td>“     "</td>
    </tr>
    <tr>
        <td>Number</td>
        <td>no syecial characters</td>
    </tr>
    <tr>
        <td>array</td>
        <td>[    }</td>
    </tr>
</table>



Also of note: JSON files can start in different ways, depending on what you want to send out for another thing to consume
* Object Files start with {
* String files start with "
* Number files start with the first digit of the number
* array files start with [


It is interesting to see the similaries and differnces in syntax between the two data structures, and it was an excercise in patience to type it all out. Thankfully, this sort of tedious conversion is not something programmers have to do manually anymore - it's fairly easly to automatically convert data from a delimited list into a table or desired language.


**Buy 2 Structures, Get 2 Free**

A quick google search lead me to https://tableconvert.com - a no frills website that you can paste a deliated list into, chose the language you want to convert it to, and it will instantly give you the code. I've used similar html tools before in my role as Webmaster for my local Destination Imagination region, but it is cool to be able to instantly see how the different languages parse the data.

**Markdown Example**


```markdown
| Element        | Name              |
|----------------|-------------------|
| First Name     | Tim               |
| Last Name      | Rayburn           |
| Address Line 1 | 5445 Legacy Drive |
| Address Line 2 | Suite 100         |
| City           | Plano             |
| State          | Zip               |
| Zip            | 75024             |
```


**html Example**

```html
<table>
    <tr>        
        <td>Element</td> <td>Name</td>
    </tr>
    <tr>
        <td>First Name</td> <td>Tim</td>
    </tr>
    <tr>
        <td>Last Name</td> <td>Rayburn</td>
    </tr>
    <tr>
        <td>Address Line 1</td> <td>5445 Legacy Drive</td>
    </tr>
    <tr>
        <td>Address Line 2</td> <td>Suite 100</td>
    </tr>
    <tr>
        <td>City</td> <td>Plano</td>
    </tr>
    <tr>
        <td>State</td> <td>Zip</td>
    </tr>
    <tr>
        <td>Zip</td> <td>75024</td>
    </tr>
</table>
```





