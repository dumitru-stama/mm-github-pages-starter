---
title: "Python vs Rust"
categories:
  - Programming
tags:
  - Python
  - Rust
  - Comparison
---

I need a way to quickly get into the mindset of using Python or Rust. I switch programming languages a lot and everytime I do it I feel the need for some kind of summary to properly execute the *context switch*.

I am not trying to claim these languages are similar (far from truth) but they are two of the most loved/used languages.

### Types

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Python</th>
<th>Rust</th>
</tr>
</thead>
<tbody>

<tr>
<td>
int
</td>
<td>
i8, i16, i32, i64, i128, isize<br/>
u8, u16, u32, u64, u128, usize
</td>
</tr>

<tr>
<td>
float
</td>
<td>
f32, f64
</td>
</tr>

<tr>
<td>
bool True/False
</td>
<td>
bool true/false
</td>
</tr>

<tr>
<td>
list
</td>
<td>
[ 0u8; 30 ] <span style="color:#BBBBBB">[type/value; size]</span><br/>
vec![ f32; 17 ]<br/>
&[..] <span style="color:#BBBBBB">(slice)</span>
</td>
</tr>

<tr>
<td>
str
</td>
<td>
char (unicode character)<br/>
String<br/>
&str <span style="color:#BBBBBB">(string slice)</span>
</td>
</tr>

<tr>
<td>
tuple
</td>
<td>
(u16, f64, String)
</td>
</tr>

<tr>
<td>
dictionary
</td>
<td>
std::collections::HashMap
</td>
</tr>

<tr>
<td>
set
</td>
<td>
std::collections::HashSet
</td>
</tr>

<tr>
<td>
None
</td>
<td>
() <span style="color:#BBBBBB">(empty tuple)</span>
</td>
</tr>

<tr>
<td>
complex
</td>
<td>
<span style="color:#BBBBBB">(various crates)</span>
</td>
</tr>

<tr>
<td>
Python is strongly dynamically typed: a string cannot become a number without conversion and variables don't have types but objects they point to have.
</td>
<td>
Arrays are allocated on the stack, vectors are allocated on the heap.
</td>
</tr>
</tbody>
</table>


### Declaring and initializing variables

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><center>Python</center></th>
<th><center>Rust</center></th>
</tr>
</thead>
<tbody>
<tr>
<td>
{% highlight python %}
a = 5

b = 'Test'
{% endhighlight %}
</td>
<td>
{% highlight rust %}
let a = 5;      // simple asignment
let a:u32 = 5;  // explicit type
let b = 'Test'; // a string slice
{% endhighlight %}
</td>
</tr>
<tr>
<td>
Strings are immutable
</td>
<td>
Compiler is usually able to infer a variable type but if is needed it can be specified
</td>
</tr>
</tbody>
</table>

