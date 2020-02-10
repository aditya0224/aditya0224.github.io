---
layout: post
title:  "Debugging Node.JS!"
author: "Adi Bhamidipati"
---

As per Hofstadter's Law, it always takes longer than we expected to implement any development feature. 
Bugs are by product of code. The number of lines of code and bugs are directly proportional.
So, debugging is one of the essential skills every developer will have. The more knowledge about the local variables and
flow of the control, easy to triage bugs and fix them.

Node.js has become one of the popular language since it is proved efficient in highly scalable data intensive 
and real time apps. Learning node.js development with novice knowledge in javascript, the first I learned is debugging.

Here are the three techniques to debug a node application:

#### Log to console:
Node.js is a run time environment for executing javascript outside browser. 
So, we don’t have window or document object in this environment.Fortunately console is now part of the global object of 
node.js.

{% highlight markdown %}
global.console.log(“This is a wanderers web debug post !”)
{% endhighlight %}

#### Throw Exceptions:
Log your debug statements, if you are logging your error some where you can see it there or you can see if it on console if you are running in local environment.
Since the error always takes string, we can use JSON.stringify(<json>);

{% highlight markdown %}
Throw Error(“This is a wanderers web debug post !”);
{% endhighlight %}

#### Debug with ide:

Third way to debug is with break points in your ide. One of the popular ide for javascript visual studio code. 
We need to add a launch.json with the similar configuration.

{% highlight markdown %}
{
   // Use IntelliSense to learn about possible attributes.
   // Hover to view descriptions of existing attributes.
   // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
   "version": "0.2.0",
   "configurations": [
       {
           "type": "node",
           "request": "launch",
           "name": "Launch Program",
           "skipFiles": [
               "<node_internals>/**"
           ],
           "program": "${workspaceFolder}/dist/index.js",
           "preLaunchTask": "tsc: build - tsconfig.json",
           "outFiles": [
               "${workspaceFolder}/dist/**/*.js"
           ]
       }
   ]
}
{% endhighlight %}
