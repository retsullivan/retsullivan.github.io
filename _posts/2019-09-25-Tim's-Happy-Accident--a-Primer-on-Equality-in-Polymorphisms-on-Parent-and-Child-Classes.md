---
layout: post
title: Tim's Happy Accident - A Primer on Equality in Polymorphisms on Parent and Child Classes
---

*This tangental explanation during freeform Q&A this morning was extremely helpful for me. It cleared up a lot of questions and misconceptions I had about polymorphisms in Java, so I decided to package up the concepts so they can be easily revisited. Enjoy!*

**When are two objects equal?**

Suppose you have a class named Person that has two properties: a first and a last name.

```java
Class Person{
String firstName;
String lastName;

//firstName and LastName getters & setters elided for clarity
```
Meanwhile, elsewhere in the code, we declare and initialize two new People: p and t.  

```java
Person p = new Person;
Person t = new Person;

p.hashCode()== t.hashCode(); //False - they are not the same object 
p.setFirstName(“Tim”);
p.setLastName(“Rayburn”);
t.setFirstName(“Tim);
t.setLastName(“Rayburn”);

t.equals(p);  //as written, this would be False
```
Why are these comparison’s false?
After all, t and p are both named “Tim Rayburn”...

The issue is that, in OOP, the question “Are they the same object ?” is a different question than “Do they contain the same value?”. We want the “t.equals(p);” to be true since they are, by-value, the same. We’re getting a false because we haven’t redefined .equals() on the Person class. By default, we’re currently getting Object’s original version of.equals(). 

So, we need to define a Person’s .equals() like this:

```java
Class Person{
Private String firstName;
Private String lastName;

@Override
Public int hashCode{
    Return super.hashCode();
}
@Override
Public boolean equals(Object obj){
  if (obj instanceof Person){ //this is a polymorphism check
        Person p = (Person)pObj; //hard casts pObj to a person
        Return pObj.getFirstname().equals(this.getFirstName)&&
               Return pObj.getLastname().equals(this.getLastName);
     }
  Else return false;
}
```

Then, we can check to see if the two Person objects contain the same name.

```java
Person p = new Person;
Person t = ner Person;

System.out.println(p.hashCode());  
System.out.println(t.hashCode());
System.out.println(p.hashCode() == t.haschCode); //this will still be false
System.out.println(p.equals(t)));  //this will now be true
```

When we work in Java, we can be “in charge” of equal. We can define what it means for any two members of a class to equal each other. This is a powerful tool of OOP, and is part of why subclasses are able to have methods and properties in addition to their original properties.

Any time you extend or implement, you have created a polymorphic relationship between two types. If we create a class MiddleNamePerson that extends Person, it is a polymorphically equivalent child class of Person.

```java
Class middleNamedPerson extends Person{
Private String middleName;

//getters and setters elided for clarity

If we do this, p&t are still equal.

Person p = new Person;
Person t = new middleNamedPerson;

Return p.equals(t); // will work
Return t.equals(p); //will work
```


But, if we @Override the equals function in MiddleNamedPerson, this can cause the result of equals(); to change.

```java
Class MiddleNamedPerson extends Person{
Private String middleName;

//other code and getters and setters elided for clarity

@Override
Public boolean equals(Object obj){
  if (obj instanceof MiddleNamedPerson){ //this is a polymorphism check
        Person p = (MiddleNamedPerson)pObj; //hard casts pObj to a person
        Return pObj.getFirstName().equals(this.getFirstName)&&
             Return pObj.getLastName().equals(this.getLastName&&
                    Return pObj.getMiddleName().equals(this.getMiddleName);
     }
     Return super.equals(obj);
}
//getters and setters elided for clarity
```


*Note: There is no type “var”. It can only be used when it’s initializing a variable and the correct type is clear.*

With the addition of the @Override “.equals()” in the middleNamedPersonClass, there is now a possible mismatch of results from the two “.equals()” functions below. This is because one of them is being called on a Person with only two names, and the other is being called on a middleNamedPerson.

```java
Person p = new Person;
Person t = new MiddleNamedPerson;

Return p.equals(t); // will work
Return t.equals(p); //will NOT work if t has a middle named entered
```


Below is an example of a scenario where the two equals functions do **NOT** yield the same result. 

```java
Person p = new Person;
Person t = new MiddleNamedPerson;

p.setFirstName(Tim);
p.setLastName(Rayburn);
t.setFirstName(Tim);
t.setMiddleName(John);
t.setLastName(Rayburn);


Return p.equals(t); // is still TRUE
Return t.equals(p); //is FALSE since t has a middle name
```

In this final example, p.equals(t) is true because the “.equals()” method is associated with Person p. This means that it only checks for equality between the first and last names. In contrast, t.equals(p) uses the “.equals()” method associated with the MiddleNamedPerson class. It checks to see if the first, last, AND middle names are all the same, which is why it is FALSE.

I'm so glad that Tim went off on this tangent today (he started off talking about what a hashcode was, and ended up here).  It was a very happy accident.

![](http://www.quickmeme.com/img/35/35b1ea54c14c130724fe26fe4bfe40a2e4dabad565a472e30fabddd7f7097b46.jpg)

Posted by Rachel Turek Sullivan
