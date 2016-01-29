---
layout: post
title:  "ARRAY: Remove Arguments from Array"
date:   2016-1-27 09:59:53 -0500
categories: javascript
---

Create a function that accepts an array as it's first argument, and any number of additional arguments. The additional arguments will be removed from the array in the first argument.

I tried a bunch of approaches with this. For loops, manually adding the arguments to the filter, and other shennanigans. Then I learned how to <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/indexOf#Checking_occurrences" target="_blank">check occurences with `indexOf`</a>. Thanks MDN!

<a class="jsbin-embed" href="http://jsbin.com/losebujake/embed?js,console">JS Bin on jsbin.com</a><script src="http://static.jsbin.com/js/embed.min.js?3.35.9"></script>
