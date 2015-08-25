---
layout: post
title: Build a simple mp3 player in C#
---

<p>Personally I prefer SharpDevelop over Visual Studio, find them at sharpdevelop.net or https://github.com/icsharpcode (we love Open source: 0). Truth be told, it’s a matter of preference here, go with whatever IDE you find comfortable. Click File, new Project, then Windows application. In SharpDevelop, this screen wit show up.</p>

<p>Switch between Design and Source to change the view. Word of advice, whenever building an application, it’s better to first develop the UI, before you start working on the logic, reason being, since this is a basic/starter tutorial, it allows you to quit thinking in abstract terms and let’s you hone in on accomplishing specific things. Well, if you mind, you can start with the code.</p>

<p>To add more UI features like buttons, radio buttons, click View, and then Tools. Add a few buttons to your form, these will include Open, Play and Stop. Then add an OPENFILEDIALOG form, don’t worry, this will appear at the bottom.</p>

<b>The Logic</b>
<p>I bet you all are familiar with the concept of Object Oriented Programming. Create a new class, let’s call it Player. We add the methods for Open, Play and Stop. We’ll need to add a DllImport attribute, which will allow us to access functionality from a dll file, called winmm.dll allowing us to play mp3 files. We’ll use the mciSendString function to send commands to Windows so that it can do things with our mp3.</p>

<b>The Form</b>
<p>Then, go back to the source code of your form. Add a new Player instance variable and set it equal to a new player object. Something like this: Player mp3player = new Player(); Double click the Open File button you had on your form, then add a method to open file, in the Handler that already exists. Do the same to the open file Dialog control, which is at the bottom of the form(not really part of the form). Edit the Handler.</p>

<p>The source code can be found at <a href="https://github.com/danogwok/mp3player" target="_blank">MP3 Player</a>.</p>

<p>You can try out the player too… mp3 player”</p>
