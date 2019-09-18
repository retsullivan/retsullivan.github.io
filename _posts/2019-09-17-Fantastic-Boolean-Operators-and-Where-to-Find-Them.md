<span class="c8">Fantastic Boolean Operators and Where to Find Them</span>

<span class="c0">By Rachel "Scamander" Sullivan</span>

<span class="c3"></span>

<span class="c3">Boolean Expressions and Operators</span>

<span class="c3"></span>

<span class="c20 c22">Boolean logic is a simple but powerful concept that is the foundation of many mathematical and scientific fields.  It is fundamental to software programming, because it is able to help developers breakdown complex statements into easy to digest logical formulas.</span>

<span class="c20 c22"></span>

<span class="c22">Boolean logic uses bools (true and false values) to organize information. Bools are typically denoted as T or 1 for true and F or 0 for false.  </span><span class="c12">A Boolean operator in Java programming is an operator that returns a Boolean result that’s based on the Boolean result of one or two other expressions.</span><span class="c20 c22"> Boolean variables can have two values - “true” or “false”.</span>

<span class="c20 c22"></span>

<span class="c20 c25">Using Boolean Logic on a single element</span>

<span class="c20 c22"></span>

<span class="c20 c22">The negation operator is written as “~” for primitives and “!” for variables. The term “~a” is read as “not a”. When applied to bools, we can create a truth table to list all the possible logical outcomes.</span>

<span class="c3"></span>

<a id="t.0371726bb7d54d0a645bd43d191aa211f3ea9778"></a><a id="t.0"></a>

<table class="c23">

<tbody>

<tr class="c27">

<td class="c30" colspan="2" rowspan="1">

<span class="c5">Truth Table for Variable Negation</span>

</td>

</tr>

<tr class="c14">

<td class="c9" colspan="1" rowspan="1">

<span class="c5">A</span>

</td>

<td class="c10" colspan="1" rowspan="1">

<span class="c5">!A</span>

</td>

</tr>

<tr class="c14">

<td class="c9" colspan="1" rowspan="1">

<span class="c16">T</span>

</td>

<td class="c10" colspan="1" rowspan="1">

<span class="c16">F</span>

</td>

</tr>

<tr class="c14">

<td class="c9" colspan="1" rowspan="1">

<span class="c16">F</span>

</td>

<td class="c10" colspan="1" rowspan="1">

<span class="c16">T</span>

</td>

</tr>

</tbody>

</table>

<span class="c20 c22"></span>

<span class="c0">When considering a single variable boolean, we see that if a bool (a) is true than its opposite (!a) is false.  Likewise if a bool (a) is false, it’s opposite (!a) must be true.</span>

<span class="c0"></span>

<span class="c0">In Java, the ! operator returns true if the operand to the right evaluates to false.  It returns false if the operand to the right is true.</span>

<span class="c0"></span>

<span class="c20 c25">Using Boolean Logic on two elements</span>

<span class="c20 c25"></span>

<span class="c20 c22">Two more important Boolean operators are “And” and “Or”.  In Java, “And” is written as “&” and “&&”. The “Or” operator is written as “|” for “||”.  Truth tables with two boolean elements are more complicated because we have to compare two bools to create our final true or false declaration.</span>

<span class="c20 c22"></span>

<span class="c0"></span>

<a id="t.e66ee60e5098316bf0b55bb58109fae66e788e2e"></a><a id="t.1"></a>

<table class="c23">

<tbody>

<tr class="c14">

<td class="c17" colspan="1" rowspan="1">

<span class="c3">A</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c3">B</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c3">A||B (or)</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c3">A &&  B (and)</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c3">A XOR B</span>

<span class="c3">Exclusive OR</span>

</td>

</tr>

<tr class="c14">

<td class="c17" colspan="1" rowspan="1">

<span class="c0">True</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c0">True</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c0">True</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c0">True</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c0">False</span>

</td>

</tr>

<tr class="c14">

<td class="c17" colspan="1" rowspan="1">

<span class="c0">False</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c0">True</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c0">True</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c0">False</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c0">True</span>

</td>

</tr>

<tr class="c14">

<td class="c17" colspan="1" rowspan="1">

<span class="c0">True</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c0">False</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c0">True</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c0">False</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c0">True</span>

</td>

</tr>

<tr class="c14">

<td class="c17" colspan="1" rowspan="1">

<span class="c0">False</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c0">False</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c0">False</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c0">False</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c0">False</span>

</td>

</tr>

</tbody>

</table>

<span class="c0"></span>

<span class="c0">Included in the table below is a concept called “exclusive or”.  This is a logical concept that does not have a character exclusive operator in Java.  However, we can construct the logic behind it through a bit of code (seen in the table below) that combines the || and && operators. In simple language, exclusive or mean “this or that, but not both’.</span>

<span class="c0"></span>

<a id="t.7772bfda3d46b2138b840c24e658425df7f84fd7"></a><a id="t.2"></a>

<table class="c23">

<tbody>

<tr class="c14">

<td class="c18" colspan="1" rowspan="1">

<span class="c20 c21">Operator</span>

</td>

<td class="c13" colspan="1" rowspan="1">

<span class="c20 c21">Code</span>

</td>

<td class="c11" colspan="1" rowspan="1">

<span class="c20 c21">Explanation</span>

</td>

</tr>

<tr class="c14">

<td class="c18" colspan="1" rowspan="1">

<span class="c15">!</span>

</td>

<td class="c13" colspan="1" rowspan="1">

<span class="c15">if( !a){</span>

<span class="c15">//do code</span>

<span class="c15">}</span>

</td>

<td class="c11" colspan="1" rowspan="1">

<span class="c15">This will execute only if A is not true</span>

</td>

</tr>

<tr class="c14">

<td class="c18" colspan="1" rowspan="1">

<span class="c15">||</span>

</td>

<td class="c13" colspan="1" rowspan="1">

<span class="c15">if (a||b){                                </span>

<span class="c15">//do code</span>

<span class="c26">}</span>

</td>

<td class="c11" colspan="1" rowspan="1">

<span class="c26">This will execute as long as ONE of the elements is TRUE</span>

</td>

</tr>

<tr class="c14">

<td class="c18" colspan="1" rowspan="1">

<span class="c15">&&</span>

</td>

<td class="c13" colspan="1" rowspan="1">

<span class="c15">if (a&&b){                                </span>

<span class="c15">//do code</span>

<span class="c15">}</span>

</td>

<td class="c11" colspan="1" rowspan="1">

<span class="c15">This will execute ONLY if BOTH a and b are TRUE</span>

</td>

</tr>

<tr class="c14">

<td class="c18" colspan="1" rowspan="1">

<span class="c20 c6">XOR</span>

</td>

<td class="c13" colspan="1" rowspan="1">

<span class="c6">public</span><span class="c6"> </span><span class="c6">static</span><span class="c6"> </span><span class="c6">boolean</span><span class="c6"> logicalXOR(</span><span class="c6">boolean</span><span class="c6">x,</span> <span class="c6">boolean</span><span class="c20 c6"> y) {</span>

<span class="c6">return</span><span class="c20 c6"> ( ( x || y ) && ! ( x && y ) );</span>

<span class="c6 c20">}</span>

<span class="c15"></span>

</td>

<td class="c11" colspan="1" rowspan="1">

<span class="c15">There is no character exclusive or operator in java.  However, one can create the logic though combining the || and && operators.</span>

<span class="c15"></span>

<span class="c15">This will only execute if the truth values don’t match. (One must be true and one must be false)</span>

<span class="c15"></span>

</td>

</tr>

</tbody>

</table>

<span class="c0"></span>

<span class="c15"></span>

<span class="c0">The examples above are all conditional boolean operators.  Java also has bitwise boolean operators with similar properties.  </span>

<span class="c0"></span>

<span class="c3">Bitwise Negation Truth Table</span>

<span class="c0"></span>

<a id="t.026f7c48de8e28f4ba863f3163602c72eda411d1"></a><a id="t.3"></a>

<table class="c23">

<tbody>

<tr class="c14">

<td class="c17" colspan="1" rowspan="1">

<span class="c3">a</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c3">~a</span>

</td>

</tr>

<tr class="c14">

<td class="c17" colspan="1" rowspan="1">

<span class="c0">0</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c0">1</span>

</td>

</tr>

<tr class="c14">

<td class="c17" colspan="1" rowspan="1">

<span class="c0">1</span>

</td>

<td class="c17" colspan="1" rowspan="1">

<span class="c0">0</span>

</td>

</tr>

</tbody>

</table>

<span class="c0"></span>

<span class="c0"></span>

<span class="c3">Bitwise Or, And, and Exclusive Or Truth Table</span>

<span class="c0"></span>

<a id="t.37efd1cd9bbeb7e27cfa629ea5aec1b9a672b947"></a><a id="t.4"></a>

<table class="c23">

<tbody>

<tr class="c14">

<td class="c4" colspan="1" rowspan="1">

<span class="c3">a</span>

</td>

<td class="c4" colspan="1" rowspan="1">

<span class="c3">b</span>

</td>

<td class="c4" colspan="1" rowspan="1">

<span class="c3">a|b</span>

</td>

<td class="c4" colspan="1" rowspan="1">

<span class="c3">a&b</span>

</td>

<td class="c4" colspan="1" rowspan="1">

<span class="c3">a^b</span>

</td>

</tr>

<tr class="c14">

<td class="c4" colspan="1" rowspan="1">

<span class="c0">0</span>

</td>

<td class="c4" colspan="1" rowspan="1">

<span class="c0">1</span>

</td>

<td class="c4" colspan="1" rowspan="1">

<span class="c0">1</span>

</td>

<td class="c4" colspan="1" rowspan="1">

<span class="c0">0</span>

</td>

<td class="c4" colspan="1" rowspan="1">

<span class="c0">1</span>

</td>

</tr>

<tr class="c14">

<td class="c4" colspan="1" rowspan="1">

<span class="c0">1</span>

</td>

<td class="c4" colspan="1" rowspan="1">

<span class="c0">1</span>

</td>

<td class="c4" colspan="1" rowspan="1">

<span class="c0">1</span>

</td>

<td class="c4" colspan="1" rowspan="1">

<span class="c0">1</span>

</td>

<td class="c4" colspan="1" rowspan="1">

<span class="c0">0</span>

</td>

</tr>

<tr class="c14">

<td class="c4" colspan="1" rowspan="1">

<span class="c0">0</span>

</td>

<td class="c4" colspan="1" rowspan="1">

<span class="c0">0</span>

</td>

<td class="c4" colspan="1" rowspan="1">

<span class="c0">0</span>

</td>

<td class="c4" colspan="1" rowspan="1">

<span class="c0">0</span>

</td>

<td class="c4" colspan="1" rowspan="1">

<span class="c0">0</span>

</td>

</tr>

<tr class="c14">

<td class="c4" colspan="1" rowspan="1">

<span class="c0">1</span>

</td>

<td class="c4" colspan="1" rowspan="1">

<span class="c0">0</span>

</td>

<td class="c4" colspan="1" rowspan="1">

<span class="c0">1</span>

</td>

<td class="c4" colspan="1" rowspan="1">

<span class="c0">0</span>

</td>

<td class="c4" colspan="1" rowspan="1">

<span class="c0">1</span>

</td>

</tr>

</tbody>

</table>

<span class="c0"></span>

<span class="c0"></span>

<span class="c0"></span>

<span class="c3">Be careful!</span>

<span class="c3"></span>

<span class="c0">When using boolean operators in Java, you have to be careful. There are fundamental differences between “&” and “&&”  and “|” and “||”. The single & and | REQUIRE the compiler to look at both conditions.  In contrast, as soon as the compiler sees that && and || has reached inevitability, it stops comparing and doesn’t validate the rest of the statement is true.</span>

<span class="c0"></span>

<span class="c3"></span>

<span class="c3"></span>

<span class="c3">Keep Looking</span>

<span class="c3"></span>

<span class="c0">You may have noticed that, despite the title of this post, you only spotted 8 boolean logical operators. What are the other 8 operators you ask?  Despite consulting with multiple expert programmers, the author was unable to identify the additional 8\.  There was some speculation among the experts polled that comparison statements like !=, <, >, <=, >=, could be considered conditional boolean expressions.  In the search for the elusive 8 operators, even = and == were considered. However, no consensus could be reached in the time allotted since the expert programmers had to go to bed early. One can hope that, in the future, exciting new research will merit follow up post detailing the mysterious additional boolean operators.</span>

<span class="c0"></span>

<span class="c0"></span>

<span class="c0"></span>

<span class="c0"></span>

<span class="c0"></span>

<span class="c0"></span>

<span class="c0"></span>

<span class="c0"></span>

<span class="c0"></span>

<span class="c0"></span>

<span class="c20 c29"></span>
