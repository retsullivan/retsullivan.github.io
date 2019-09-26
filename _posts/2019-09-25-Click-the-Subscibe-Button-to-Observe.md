---
layout: post
title: Click the Subscribe Button to Observe
---

You're 10 years old, and you can't get enough of your favorite YouTuber. You never want to miss a video, and look forward with avid intensity to each new drop. But since, **gasp**, your mom won't let you be on your phone all the time, how will you know when a new video is posted?  Subscribe, of course! 

![](https://media1.tenor.com/images/030643feae2c2c4bef5429d45f9605b7/tenor.gif)

In Java, objects sometimes need to be alerted when something they contain or are connected to is modified. The **Observer** design pattern is the framework we can use to keep track of changes on our objects.  In Bootcamp, we're using the robust <a href="https://spring.io/" target="_blank">Spring framework</a> as our Observer on the Text Action Game (TAG) project. 

The behavior protocol for Observer described in the <a href="https://retsullivan.github.io/Almost-Famous-the-Fab-4-of-Design-Patterns/" target="_blank">Gang of Four</a>'s famous book on Design Patterns states: define a one-to-many dependency between objects so that when one object changes state, all its dependents are notified and updated automatically. 

**Subscibe Now!**

So, *how* are the dependents notified and updated about the change? Like the avid YouTube fan, dependants get notifications from their **subscription**. This subscription allows all the objects affected by the change to get update information automatically every time something is changed in the object to which the dependants are subscribed.

**Structure**

I found this flowchart from <a href="https://refactoring.guru/" target="_blank">Refactoring Guru</a> very helpful in picturing the different interactions between elements of the Observer pattern.
![](https://refactoring.guru/images/patterns/diagrams/observer/structure-indexed-2x.png)

In it, you can see the Observer pattern described in 6 parts:

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;border-color:#9ABAD9;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;border-color:#9ABAD9;color:#444;background-color:#EBF5FF;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:0px;overflow:hidden;word-break:normal;border-color:#9ABAD9;color:#fff;background-color:#409cff;}
.tg .tg-phtq{background-color:#D2E4FC;border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-lboi{border-color:inherit;text-align:left;vertical-align:middle}
.tg .tg-48yq{background-color:#D2E4FC;border-color:inherit;text-align:left;vertical-align:middle}
.tg .tg-w8l6{font-weight:bold;font-size:13px;border-color:inherit;text-align:left;vertical-align:middle}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-w8l6">Name</th>
    <th class="tg-w8l6">Role in the Observer Pattern</th>
    <th class="tg-lboi"></th>
  </tr>
  <tr>
    <td class="tg-48yq">Publisher</td>
    <td class="tg-48yq">Sends events to other objects. Events happen when the publisher is changed or does something.</td>
    <td class="tg-48yq"></td>
  </tr>
  <tr>
    <td class="tg-lboi">Subscription List</td>
    <td class="tg-lboi">When a new event happens, the publisher uses a notification method to notify all subscribers on the list</td>
    <td class="tg-lboi"></td>
  </tr>
  <tr>
    <td class="tg-phtq">Subscriber</td>
    <td class="tg-phtq">The subscriber implements the notification interface, so it can get all the event details every time there is an update</td>
    <td class="tg-phtq"></td>
  </tr>
  <tr>
    <td class="tg-0pky">Concrete Subscribers</td>
    <td class="tg-0pky">These special subscribers do someting in response to getting a notification</td>
    <td class="tg-0pky"></td>
  </tr>
  <tr>
    <td class="tg-phtq">Updates</td>
    <td class="tg-phtq">Contain special context information so that the subscibers know what to do with the update</td>
    <td class="tg-phtq"></td>
  </tr>
  <tr>
    <td class="tg-0pky">Clients</td>
    <td class="tg-0pky">Creates the publisher and subscriber objects and signs the subscribers up for updates</td>
    <td class="tg-0pky"></td>
  </tr>
</table>



For a more expert and in depth description of the Observer pattern, checkout  <a href="https://refactoring.guru/design-patterns/observer	" target="_blank">this excellent post</a> from Refactoring Guru. It describes the Observer pattern in easy to understand language and includes some more great infographics and illustrations to help make envisioning the Observer pattern easy. 																						

<a href="https://docs.google.com/spreadsheets/d/1OlY9JCrjk7uvxffcAcwOa1yOtACNMfv-YUb5PcUrOUI/edit?usp=sharing" target="_blank">Click here</a> for a table of Design Patterns that inclues some class notes on the topic.
