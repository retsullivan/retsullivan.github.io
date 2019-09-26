---
layout: post
title: Click the Subscribe Button to Observe
---

You're 10 years old, and you can't get enough of your favorite YouTuber. You never want to miss a video, and look forward with avid intensity to each new drop. But since, **gasp**, your mom won't let you be on your phone all the time, how will you know when a new video is posted?  Subscribe, of course! 

![](https://media1.tenor.com/images/030643feae2c2c4bef5429d45f9605b7/tenor.gif)

In Java, objects sometimes need to be alerted when something they are contain or connected to is modified. The **Observer** design pattern is the framework we can use to keep track of changes on our objects.  In our Bootcamp, we're using the robust <a href="https://spring.io/" target="_blank">Spring framework</a> as our Observer on the Text Action Game (TAG) project. 

The behavior protocol for Observer described in the <a href="https://retsullivan.github.io/Almost-Famous-the-Fab-4-of-Design-Patterns/" target="_blank">Gang of Four</a>'s famous book on Design Patterns states: define a one-to-many dependency between objects so that when one object changes state, all its dependents are notified and updated automatically. 

**Subscibe Now!**

So, *how* are the dependents notified and updated about the change? Like the avid YouTube fan, dependants get notifications from their **subscription**. This subscription allows all the objects affected by the change to get update information automatically every time something is changed in the object to which the dependants are subscribed.

**Structure**

I found this flowchart from <a href="https://refactoring.guru/" target="_blank">Refactoring Guru</a> very helpful in picturing the different interactions between elements of the Observer pattern.
![](https://refactoring.guru/images/patterns/diagrams/observer/structure-indexed-2x.png)

In it, you can see the Observer pattern described in 6 parts:

| Name     | Role in the Observer Pattern |
|----------|------------------------------|
| Publisher| Sends events to other objects. Events happen when the publisher is changed or does something. |
| Subscription List| When a new event happens, the publisher uses a notification method to notigy all subscribers on the list |
| Subscriber| The subscriber has implements the notification interface, so it can get all the event details every time there is an update  |
| Concrete Subscribers| These special subscribers and do someting in response to getting a notification |
| Updates| Contain special context information so that the subscibers know what to do with the update |
| Clients| Creates the publisher and subscriber objects and signs the subscribers up for updates |

Usually, subscribers need some contextual information to handle the update correctly. For this reason, publishers often pass some context data as arguments of the notification method. The publisher can pass itself as an argument, letting subscriber fetch any required data directly.


For a more expert and in depth description of the Observer pattern, checkout  <a href="https://refactoring.guru/design-patterns/observer	" target="_blank">this excellent post</a> from Refactoring Guru. It describes the Observer pattern in easy to understand language and includes some more great infographics and illustrations to help make envisioning the Observer pattern easy. 																						

<a href="https://docs.google.com/spreadsheets/d/1OlY9JCrjk7uvxffcAcwOa1yOtACNMfv-YUb5PcUrOUI/edit?usp=sharing" target="_blank">Click here</a> for a table of Design Patterns that inclues some class notes on the topic.