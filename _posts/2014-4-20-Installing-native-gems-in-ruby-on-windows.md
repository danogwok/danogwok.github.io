---
layout: post
title: Installing Native Ruby Gems in Windows
---

<p>This is one of the biggest issues I’ve faced while working on a Ruby project in Windows. Native gems might depend on other libraries which are hard, or sometimes, impossible to build on Windows. In order to install C/C++ Ruby extensions on each system you must have build tools and all dependencies installed. The fact is that most of such gems are developed primarily on Linux where developers, naturally, rely on existing libraries. On the other hand lot of these libraries are portable and can be used on Windows, but number of them are shipped in a binary format because building them on Windows is quite complicated. The main reason I wrote this article is because I had issues installing the Nokogiri gem in Ruby while running on Windows.</p>

<p>Nokogiri needs to be compiled and dynamically linked against libxml and libxslt. I figured we needed zlib and libiconv too.</p>

<p>Download and install Cygwin , and install all the packages under “devel” (not all are needed, but we need to be on the safer side). Make sure the above listed dependencies are installed too. I would also suggest that you install ruby from Cygwin.</p>

<b>Installing Nokogiri<b>
<p>Download the Nokogiri gem from this link, http://rubygems.org/downloads/nokogiri-1.6.1.gem. Change into that directory and run “gem install –local nokogiri-1.6.1.gem” .</p>

<p>This should work, though my advice is, please switch to Linux, preferably Opensuse :) …</p>
