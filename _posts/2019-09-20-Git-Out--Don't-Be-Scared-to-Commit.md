---
layout: post
title: Git Out - Don't be Scared to Commit
---

by Rachel Turek Sullivan


**Command Line Challenges**

Learning to use the command line to navigate and manipulate files has been a surprisingly challenging task this week.  This post is a repository of common Git commands we've been using in Bootcamp.  I plan to update it occasionally when needed.

**Git the Big Picture**

Git creates snapshots of our saves and changes - it does not save the files.  It’s similar to save points in a video game. Every time we create a save point (commit a snapshot), git allows us to revert to the state the file was at when we saved it.  


**Quick Commands**

history - shows everything you've just typed in

clear - deletes everything from the window to make visual space

cd - change directory

git ls - get a list of things in your folder


**Changing directories between jsquire and tag**


AKA - Looking at a different folder

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-fymr{font-weight:bold;border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-fymr">If I see</th>
    <th class="tg-fymr">I type</th>
    <th class="tg-fymr">To do</th>

  </tr>
  <tr>
    <td class="tg-0pky">C:\source\jsquire [master ↑1]&gt;</td>
    <td class="tg-0pky">cd /source/tag</td>
    <td class="tg-0pky">Change directories to tag</td>

  </tr>
  <tr>
    <td class="tg-0pky">C:\source\tag [master +2 ~0 -0 | +0 ~3 -0 !]&gt;</td>
    <td class="tg-0pky">git status</td>
    <td class="tg-0pky">See what has been changed since the last time we committed</td>

  </tr>
 
</table>

**Commiting a change in a file**

This is how we save versions of jsquire and tag in GitHub.

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-yla0{font-weight:bold;text-align:left;vertical-align:middle}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-yla0">If I see</th>
    <th class="tg-yla0">I type</th>
    <th class="tg-yla0">To do</th>
  </tr>
  <tr>
    <td class="tg-0lax">C:\source\jsquire [master ↑1]&gt;</td>
    <td class="tg-0lax">cd /source/tag</td>
    <td class="tg-0lax">Make sure you’re in the right folder (cd if needed)</td>
  </tr>
  <tr>
    <td class="tg-0lax">C:\source\tag [master +2 ~0 -0 | +0 ~3 -0 !]&gt;</td>
    <td class="tg-0lax">git status</td>
    <td class="tg-0lax">See what has been changed since the last time we committed (to see if we need to commit anything</td>
  </tr>
  <tr>
    <td class="tg-0lax">C:\source\tag [master +2 ~0 -0 | +0 ~3 -0 !]&gt;</td>
    <td class="tg-0lax">git add .</td>
    <td class="tg-0lax">Tells the command line we’re about to add a snapshot</td>
  </tr>
  <tr>
    <td class="tg-0lax">C:\source\tag [master +2 ~1 -0 ~]&gt;</td>
    <td class="tg-0lax">git commit -m "constructors and person"</td>
    <td class="tg-0lax">Creates a new snapshot of our latest changes called “constructors and person”</td>
  </tr>
  <tr>
    <td class="tg-0lax">C:\source\tag [master]&gt;</td>
    <td class="tg-0lax">git push origin master</td>
    <td class="tg-0lax">Git please push my code to GitHub (named origin), and please push the master branch specifically.  Shortcut: git pom</td>
  </tr>
</table>



**Commits**

Committing changes in jsquire and resetting to the master

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-cly1{text-align:left;vertical-align:middle}
.tg .tg-yla0{font-weight:bold;text-align:left;vertical-align:middle}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-yla0">If I see</th>
    <th class="tg-yla0">I type</th>
    <th class="tg-yla0">To do</th>
  </tr>
  <tr>
    <td class="tg-cly1">C:\source\jsquire [ThursdayAMdrill]&gt;</td>
    <td class="tg-cly1">git checkout master</td>
    <td class="tg-cly1">Switched to branch 'master'</td>
  </tr>
  <tr>
    <td class="tg-0lax">C:\source\jsquire [master ↑1]&gt;</td>
    <td class="tg-0lax">git reset --hard origin/master</td>
    <td class="tg-0lax">This makes it so jquire is now pointing to the original file</td>
  </tr>
</table>


**Checkout a branch**

This saves a new snapshot of our latest changes called “constructors and person”

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-cly1{text-align:left;vertical-align:middle}
.tg .tg-yla0{font-weight:bold;text-align:left;vertical-align:middle}
</style>
<table class="tg">
  <tr>
    <th class="tg-yla0">If I see</th>
    <th class="tg-yla0">I can type</th>
    <th class="tg-yla0">To do</th>
  </tr>
  <tr>
    <td class="tg-cly1">C:\source\tag [master]&gt;</td>
    <td class="tg-cly1">git checkout -b ioc</td>
    <td class="tg-cly1">Moves our file to a new branch 'ioc'?</td>
  </tr>
</table>

**Find the differences between files**

Checking what has been changed in a file since it was committed

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-cly1{text-align:left;vertical-align:middle}
.tg .tg-yla0{font-weight:bold;text-align:left;vertical-align:middle}
</style>
<table class="tg">
  <tr>
    <th class="tg-yla0">If I see</th>
    <th class="tg-yla0">I type</th>
    <th class="tg-yla0">To do</th>
  </tr>
  <tr>
    <td class="tg-cly1">C:\source\jsquire [master ↑1]&gt;</td>
    <td class="tg-cly1">git diff</td>
    <td class="tg-cly1">This lets you see what you’ve changed in a filesince you last commited</td>
  </tr>
</table>

**Merging with the master file**

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-cly1{text-align:left;vertical-align:middle}
.tg .tg-yla0{font-weight:bold;text-align:left;vertical-align:middle}
.tg .tg-0lax{text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-yla0">If I see</th>
    <th class="tg-yla0">I type</th>
    <th class="tg-yla0">To do</th>
  </tr>
  <tr>
    <td class="tg-cly1">C:\source\jsquire [ThursdayAMdrill]&gt;</td>
    <td class="tg-cly1">git checkout master</td>
    <td class="tg-cly1">Points you at the master branch so that the program knows where to combine the files</td>
  </tr>
  <tr>
    <td class="tg-0lax">C:\source\jsquire [master ↑1]&gt;</td>
    <td class="tg-0lax">git merge ioc</td>
    <td class="tg-0lax">Lets you integrate all the changes you’ve made into the master file</td>
  </tr>
</table>
