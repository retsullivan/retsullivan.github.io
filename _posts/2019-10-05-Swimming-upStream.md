---
Layout: Post
Title: Swimming upStream
---

## A Beginner’s Guide to Understanding Stream Notation in Java

![](http://m.quickmeme.com/img/33/3398632cdf583387ac55485651a2cb4a652234cb69f42f22b3fe8b623d688aca.jpg)

Streams are another way to do something to every member of a set (similar to forEach). You can process only as much of the stream as you want to to accomplish the goal. It’s like a forEach with an automatic break in the code. Streams can dramatically shorten the code that we have to create.

I spent some time diagramming the code from Friday's stream examples to better show what each part of a stream statement is doing, and what equivalent logic looks like in loops. Since I know some of the other bootcampers had questions about the syntax, I though I'd post them on the blog to make them easier to find. 


### Example of .forEach()

The .forEach() method of Stream class does exactly what you'd expect it to do - it itereates through all the elements in a stream (just like the for each loop we've already learned about).

 **Stream statement diagram:**

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-6uvu{font-family:"Courier New", Courier, monospace !important;;color:#000000;text-align:left;vertical-align:middle}
.tg .tg-e0yz{font-weight:bold;font-size:13px;font-family:Verdana, Geneva, sans-serif !important;;background-color:#cbcefb;text-align:left;vertical-align:middle}
.tg .tg-a8yd{font-weight:bold;font-size:13px;font-family:Verdana, Geneva, sans-serif !important;;background-color:#cbcefb;text-align:left;vertical-align:top}
.tg .tg-vwu2{font-family:"Courier New", Courier, monospace !important;;color:#000000;text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <th class="tg-e0yz">OriginalObject</th>
    <th class="tg-e0yz">Streaming</th>
    <th class="tg-e0yz">Logic loop</th>
    <th class="tg-a8yd">Lambda(ƛ) parameter</th>
    <th class="tg-a8yd">Lambda(ƛ) expression</th>
  </tr>
  <tr>
    <td class="tg-6uvu">numbers</td>
    <td class="tg-6uvu">.stream()</td>
    <td class="tg-6uvu">.forEach</td>
    <td class="tg-vwu2">(x -&gt;</td>
    <td class="tg-vwu2">System.out.println(x));</td>
  </tr>
</table>



**Stream Code:**

    List numbers = Arrays.asList(2,3,4,5);
    numbers.stream().forEach(x -> System.out.println(x));

**Output:**

    2
    3
    4
    5

**Works Like This Regular For Each Loop**

    List numbers = Arrays.asList(2,3,4,5);
    for  (int x: numbers){
       System.out.println(x*x);
    }

### Example of .map() & .collect()

The .collect() method of Stream class gathers elements of any Stream into a Collection. If you want to return a value, you will need a collector to collect the results.

 **Stream statement diagram:**
 
 <style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:bold;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-juju{font-family:"Courier New", Courier, monospace !important;;text-align:left;vertical-align:top}
.tg .tg-64j6{background-color:#cbcefb;color:#000000;border-color:inherit;text-align:left;vertical-align:middle}
.tg .tg-t5pq{background-color:#cbcefb;color:#000000;border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-s2b1{background-color:#cbcefb;color:#000000;text-align:left;vertical-align:top}
.tg .tg-9gth{font-family:"Courier New", Courier, monospace !important;;border-color:inherit;text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <td class="tg-64j6">New variable</td>
    <td class="tg-64j6">OriginalObject</td>
    <td class="tg-t5pq">Streaming</td>
    <td class="tg-t5pq">Map Function</td>
    <td class="tg-t5pq">ƛ parameter &amp; expression  (input -&gt;output)</td>
    <td class="tg-s2b1">Get all the results</td>
    <td class="tg-s2b1">Puts result in list</td>
  </tr>
  <tr>
    <td class="tg-9gth">List newList =</td>
    <td class="tg-9gth">numbers</td>
    <td class="tg-9gth">.stream()</td>
    <td class="tg-9gth">.map(</td>
    <td class="tg-9gth">x -&gt; x*x)</td>
    <td class="tg-juju">.collect</td>
    <td class="tg-juju">(Collectors.toList());</td>
  </tr>
</table>


**Stream Code**

    List <Integer> numbers = Arrays.asList(2,3,4,5);
    List newList = numbers.stream().map(x -> x*x).collect(Collectors.toList());

**Output**

    None, but now newList = [4,9,16,25]
    
**Works Like This Regular For Each Loop**

    List <Integer> numbers = Arrays.asList(2,3,4,5);
    List newList = new ArrayList();
    for(int x : numbers){
        newList.add(x*x);
    }
## Example of .map and forEach

The .map() method is used when we want to convert a stream of `x` to stream of `f(x)` (aka `y`).


<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-m1zp{font-family:Verdana, Geneva, sans-serif !important;;background-color:#cbcefb;color:#000000;text-align:left;vertical-align:middle}
.tg .tg-juju{font-family:"Courier New", Courier, monospace !important;;text-align:left;vertical-align:top}
.tg .tg-hx3p{font-family:Verdana, Geneva, sans-serif !important;;background-color:#cbcefb;color:#000000;text-align:left;vertical-align:top}
.tg .tg-ikui{font-family:"Courier New", Courier, monospace !important;;text-align:left;vertical-align:middle}
</style>
<table class="tg">
  <tr>
    <td class="tg-m1zp">OriginalObject</td>
    <td class="tg-m1zp">Streaming</td>
    <td class="tg-m1zp">Map Function</td>
    <td class="tg-m1zp">ƛ parameter &amp; expression  (input -&gt;output)</td>
    <td class="tg-m1zp">Logic loop</td>
    <td class="tg-hx3p">print out the result of x*x</td>
  </tr>
  <tr>
    <td class="tg-ikui">numbers</td>
    <td class="tg-ikui">.stream()</td>
    <td class="tg-ikui">.map(</td>
    <td class="tg-ikui">x -&gt; x*x)</td>
    <td class="tg-ikui">.forEach</td>
    <td class="tg-juju">(y -&gt; System.out.println(y);)</td>
  </tr>
</table>

**Stream Code**

        List <Integer> numbers = Arrays.asList(2,3,4,5);
        numbers.stream().map(x -> x*x).forEach(y -> System.out.println(y));

**Output**

    4
    9
    16
    25

    
**Works Like This Regular For Each Loop**

    List <Integer> numbers2 = Arrays.asList(2,3,4,5);
    List newList = new ArrayList();
    for(int x : numbers2){
        System.out.println(x*x);
    }

## Example of .filter() & .collect()

The filter method is used to select elements as per the Predicate passed as argument.

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:bold;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-m1zp{font-family:Verdana, Geneva, sans-serif !important;;background-color:#cbcefb;color:#000000;text-align:left;vertical-align:middle}
.tg .tg-ikui{font-family:"Courier New", Courier, monospace !important;;text-align:left;vertical-align:middle}
</style>
<table class="tg">
  <tr>
    <td class="tg-m1zp">OriginalObject</td>
    <td class="tg-m1zp">Streaming</td>
    <td class="tg-m1zp">filter</td>
    <td class="tg-m1zp">ƛ parameter &amp; expression  </td>
    <td class="tg-m1zp">Collecting</td>
  </tr>
  <tr>
    <td class="tg-ikui">names</td>
    <td class="tg-ikui">.stream()</td>
    <td class="tg-ikui">.filter(</td>
    <td class="tg-ikui">s -&gt; s.startsWith(“S”))</td>
    <td class="tg-ikui">.collect(Collectors.toList());</td>
  </tr>
</table>

**Stream Code**

    List <String> names = Arrays.asList("Reflection","Collection","Stream");
    List result = names.stream().filter(s->s.startsWith("S")).collect(Collectors.toList());

**Output**

    Output: none, but result = [Stream] 

    
**Works Like This Regular For Each Loop**

    List <String> names = Arrays.asList("Reflection","Collection","Stream");
    List result = new ArrayList();
    for  (String name: names){
        if (name.startsWith("S")){
            result.add(name);
        }
    }

## Example of .filter() & .reduce()

 The reduce method is used to reduce the elements of a stream to a single value. The reduce method takes a binary operator as a parameter.
 
 <style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-6uvu{font-family:"Courier New", Courier, monospace !important;;color:#000000;text-align:left;vertical-align:middle}
.tg .tg-k1yy{font-weight:bold;font-family:Verdana, Geneva, sans-serif !important;;background-color:#cbcefb;color:#000000;text-align:left;vertical-align:middle}
</style>
<table class="tg">
  <tr>
    <td class="tg-k1yy">OriginalObject</td>
    <td class="tg-k1yy">Streaming</td>
    <td class="tg-k1yy">filter</td>
    <td class="tg-k1yy">ƛ parameter &amp; expression  </td>
    <td class="tg-k1yy">.reduce</td>
  </tr>
  <tr>
    <td class="tg-6uvu">int even =</td>
    <td class="tg-6uvu">.stream()</td>
    <td class="tg-6uvu">.filter</td>
    <td class="tg-6uvu">(x-&gt; x%2 ==0)</td>
    <td class="tg-6uvu">.reduce(0,*ans, i)-&gt;ans+1);</td>
  </tr>
</table>
 
**Stream Code**

    List number = Arrays.asList(2,3,4,5);
    int even = number.stream().filter(x -> x%2 == 0).reduce(0, (ans, i) -> ans + i));


**Output**

    Output: none, but even = 6 
    
This is becuase the function first filters out the even numbers (2 & 4), then adds them.

    
**Works Like This Regular For Each Loop**

    List numbers = Arrays.asList(2,3,4,5);
    List result = new ArrayList();
    for  (Integer x: numbers){
         if (x%2==0){
           result.add(x);
         }
    }
    
    
## Example of .sort() & .collect()  

The .sort() method returns a stream consisting of the elements of the original stream, sorted according to natural order (numerical, alphabetical, etc.). For ordered streams, the sort method is works well, but for unordered streams, things can get wierd.
    
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-b9ha{color:#000000;border-color:inherit;text-align:left;vertical-align:middle}
.tg .tg-kwiq{color:#000000;border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-tuir{font-weight:bold;background-color:#cbcefb;color:#000000;border-color:inherit;text-align:left;vertical-align:middle}
.tg .tg-lm65{font-weight:bold;background-color:#cbcefb;color:#000000;border-color:inherit;text-align:left;vertical-align:top}
</style>
<table class="tg">
  <tr>
    <td class="tg-tuir">Original Object</td>
    <td class="tg-tuir">Streaming</td>
    <td class="tg-tuir">Using .sort() method </td>
    <td class="tg-tuir">List being sorted </td>
    <td class="tg-lm65">Collecting ordered results in a list</td>
  </tr>
  <tr>
    <td class="tg-b9ha">names</td>
    <td class="tg-b9ha">.stream()</td>
    <td class="tg-b9ha">.sort(</td>
    <td class="tg-b9ha">myNames)</td>
    <td class="tg-kwiq">.collect(Collectors.toList());</td>
  </tr>
</table>
 
**Stream Code**

    Stream Code:
        String[] family = {"Rachel", "Brian", "Molly", "Lucy", "Alice", "Elliott"};
        List<String> names = Arrays.asList(family);
        List<String> sortedNames = names.stream().sorted().collect(Collectors.toList());


**Output**

    Output: none, sortedNames = [Alice, Brian, Elliott, Lucy, Molly, Rachel]

    
**Works Like This Without Streams**   

    String[] family = {"Rachel", "Brian", "Molly", "Lucy", "Alice", "Elliott"};
    List<String> names = Arrays.asList(family);
    names.sort(String.CASE_INSENSITIVE_ORDER);
    
    



