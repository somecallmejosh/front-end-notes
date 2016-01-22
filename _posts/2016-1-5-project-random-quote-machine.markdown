---
layout: post
title:  "Build a Random Quote Machine"
date:   2016-1-5 09:59:53 -0500
categories: projects
---

##Requirements
- Design a web page / view that shows a single quote and citation (one quote at a time) from a list of quotes.
- The user should be able to click a button to display a new **random** quote.
- The user should be able to click a button to Tweet the **random** quote.

##Dev Notes
The real trick for me was in using [Twitter's Web Intents](https://dev.twitter.com/web/tweet-button) to ensure the tweets updated in the same random manner as the quotes. I also truncated the quotes with the [substring](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/substring) method to ensure they didn't exceed 140 characters. In an effort to minimize my dependency on external libraries, I decided to forego the use of jQuery. 

##Finished Project

- [Code](https://github.com/somecallmejosh/random-quotes)
- [Demo](http://somecallmejosh.github.io/random-quotes/)

