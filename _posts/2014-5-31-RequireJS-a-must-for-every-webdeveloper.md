---
layout: post
title: RequireJS a must for every web developer
---

<p>Loading scripts in web development has always been one of a web developers biggest problems. Imagine a modern web application, where modern web application, Backbone handles our models, collections and views, jQuery handles our DOM interactions, we’ll need something to glue all these dependencies together at an architectural level, Requirejs does this.</p>

<p>RequireJS will make your code more manageable. It is a library that’s simple, and makes it easier to pull JS libraries into your code, without muddling your code. It is implemented around Asynchronous Module Definitions (AMDs), which are designed to load modular code asynchronously in the browser and server.</p>

<p>RequireJS is a JavaScript file and module loader. It is optimised for in-browser use, but it can be used in other JavaScript environments, like Rhino and Node. It is used to manage dependencies between modules.</p>

<p>Large applications will require a number of Javascript files, for example, this is our folder structure:</p>

<p>Under js, we have JQuery.js, Backbone.js, Underscore.js</p>

<p>We’ll create a file main.js file that is used for initialization, and will look like this</p>

```
<p>// Filename: main.js</p>

// Require.js allows us to configure shortcut alias
// There usage will become more apparent further along in the tutorial.
requirejs.config({
    //By default load any module IDs from js
    baseUrl: 'js',
    //except, if the module ID starts with "app",
    //load it from the js/app directory. paths
    //config is relative to the baseUrl, and
    //never includes a ".js" extension since
    //the paths config could be for a directory.
    paths: {
        JQuery: ‘lib/jquery.min',
  Backbone: ‘lib/backbone’,
  Underscore: ‘lib/underscore’
    }
});
```

<p>In the above example, app is the directory/subdirectory where your javascript will be written.</p>
```
<p>// Filename: app/talkback.js</p>

// the file prints some text.
Define([‘jquery’].function($){
  $(“#letstalk”).text(‘What’s going on buddy?’);
});
```
<p>Instead of adding all scripts to our index.html file, we’ll only add</p>
```
<script data-main="js/main" src="js/require.js"></script>
<script>
require([talkback], function(
require([‘app/talkback’])
));
</script>
```
<p>That’s a very simple example of what RequireJS can do.</p>

<p>You can read more at <a href="http://requirejs.org/docs/api.html" target="_blank">RequireJS Website</a></p>
