---
layout: post
title: Ruby, UNIX and Object Orientation
---

<p>Ruby, Python, and Perl all have fairly complete interfaces to common Unix system calls as part of their standard libraries.</p>

<p>My good friend David has always called Ruby, the language for the cool kids, because of the continuous need for internet access. Gems and Libraries have to be downloaded and updated frequently, something that’s frustrating especially with the high internet rates.</p>

<p>Even with all that, the reason as to why I still love and use RUBY is that, it is a purely object oriented language(supports encapsulation and all these features that you can only find in object oriented languages) and is very compatible with unix. I can interact with the terminal and do lots of stuff. Unix.</p>

<p>It’s mind-blowing when a Unix user figures out how to snap together their system’s various small command-line programs to accomplish tasks. The channel renders each command-line tool more powerful as a stage in a larger operation than it could have been as a stand-alone utility. We can couple together any number of these small programs as necessary and build new tools which add specific features as we need them. We can now speak “Unix” in compound sentences.</p>

<p>According to Wikipedia, “A shell script is a computer program designed to be run by the Unix shell, a command line interpreter. The various dialects of shell scripts are considered to be scripting languages. Typical operations performed by shell scripts include file manipulation, program execution, and printing text.”</p>

<p>Ruby is a scripting language. It provides a whole set of I/O-related methods implemented in the Kernel module. All the I/O methods are derived from the class IO.</p>

<p>The class IO provides all the basic methods, such as read, write, gets, puts, readline, getc, and printf. This means with Ruby, we can write scripts in the console and do lots of things.</p>

<p>For example, we can rename files in the Terminal using Ruby, and it’s basic code, we use the rename method:<p>

<p>#!/usr/bin/ruby # Rename a file danogwok.txt to wishlist.txt File.rename( "danogwok.txt", "wishlist.txt" )<br/>
Ruby provides support for many other I/O methods as mentioned above.<p>

<p>Another example is the “File Modes and Ownership”</p>

<p>Using the chmod method, we can change permissions to files;</p>

<p>#!/usr/bin/ruby file = File.new( "danogwok.txt", "w") file.chmod( 0755 )<br />
There are many other ways Ruby provides for us to interact with the shell. These include open4, open, exec, system, etc.</p>

<p><b>Object-Oriented Programming.</b></p>

<p>Applying the Unix Philosophy to Object-Oriented Design.</p>

<p>“Good code invariably has small methods and small objects. I get lots of resistance to this idea, especially from experienced developers, but no one thing I do to systems provides as much help as breaking it into more pieces.” – <b>Kent Beck</b>, <a href="http://www.amazon.com/Smalltalk-Best-Practice-Patterns-Kent/dp/013476904X" target="_blank">Smalltalk Best Practice Patterns</a></p>

<p>The Unix philosophy demonstrates that small components that work together through an interface can be amazingly powerful. Nesting a facet of your domain as an implementation detail of a specific model conflates responsibilities, bloats code, makes tests less isolated and slower, and hides concepts that should be first-class in your system.</p>

<p>Don’t let your domain concepts be shy. Promote them to full-fledged objects to make them more understandable, isolate and speed up their tests, reduce the likelihood that changes in neighboring features will have ripple effects, and provide the concepts a place to evolve apart from the rest of the system. The only thing we know with certainty about the futures of our systems is that they will change. We can design our systems to be more amenable to inevitable change by following the Unix philosophy and building clean interfaces between small objects that have one single responsibility.</p>

<p>Ruby is a dynamic, reflective, general purpose object-oriented programming language. Ruby originated in Japan during the mid-1990s and was first developed and designed by Yukihiro "Matz" Matsumoto.</p>

<p>Ruby supports many programming paradigms, including functional, object oriented, imperative and reflective. It also has a dynamic type system and automatic memory management.</p>

<p>For more information, you can visit one of my favorite Blogs <a href="http://tomayko.com/writings/unicorn-is-unix"target="_blank">Ryan Tomayko’s article on Unix</a> and <a href="https://practicingruby.com/articles/building-unix-style-command-line-applications" target="_blank">Building Unix-style command line apps in Ruby.</a></p>