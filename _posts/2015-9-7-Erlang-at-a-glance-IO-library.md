---
layout: post
title: Erlang at a glance, IO library
---

<p>For the past few weeks, I’ve been writing a bit of code in Erlang. For those who have no idea what Erlang is, it is a declarative /functional language developed by Ericsson in 1986(it’s that old.) Erlang is awesome at concurrency, fault tolerance, scalability and that explains its frequent use in the telecom and networking sector.
A few things about Erlang;</p>
<ul>
<li>All variables start with a capital letter</li>
<li>Variables don’t change</li>
<li>Erlang uses functions, and every function must have an argument</li>
<li>Erlang functions are closed/terminated with a 'dot'</li>
</ul>

<p>An example of constant variables in Erlang is, let’s write a list of atoms.</p>
	```
	L = [cow, goats, chicken].
	L. 
	```
<p>Then we use the lists library to delete one value.</p>
	```
	L = lists:delete(cow, L). 
	Will generate an error (** exception error: no match of right hand side value [cow,chicken]).
	```
<p>This is because variable L is already taken (bound), the correct code is;</p>
	```
	D = lists:delete(cow, L). 
	```
<p>My favorite part, the IO library. Erlang is pretty straightforward when it comes to Creating, writing and reading files. For example to write a basic txt file, in your console write;</p>
	```
	{ok, F} = file:open("C:\\Users\\Daniel\\Desktop\\work\\erlang\\text.txt" ,write).
	io:format(F, “~s ~n”, [“This is my first Erlang text file”]).
	File:close(F).
	```
<p>Easy, huh?<br />
To read the file from console, </p>
	```
	{ok, G} = file:open("C:\\Users\\Daniel\\Desktop\\work\\erlang\\text.txt" ,read).
	io:get_line(G, "").
	```
<p>Why G, instead of F? F is already binded, remember in Erlang variables are bound to there values.
To unbind the variables, all we do is use the function f.</p>
	```
	f(F). %%unbinds F
	f(G). %%unbinds G
	f(). %%to unbind all at once
	```
<p>
Now, F and G are free variables.
Well, this is a really tiny glance into Erlang, I hope you pick up interest in the language.
</p>
