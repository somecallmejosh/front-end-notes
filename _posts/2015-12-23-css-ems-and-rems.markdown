---
layout: post
title:  "CSS ems and rems"
date:   2015-12-23 09:59:53 -0500
categories: css
---

Talking about simple relative font sizing in this post. Gonna take a look at REMs and EMs. Let's look at the similarites, differences and how to convert them to pixels.

##EM Units

EM Units are calculated based on a parent element's font size.

{% highlight css %}
html {font-size: 16px;} /* This is the context value */
html p {font-size: 1em;} /* == 16px */
html p {font-size: 1.5em} /* == 24px */
{% endhighlight %}

If the parent is 16px, then 1em is the equivalent size.


###Converting `px` to `em`

Convert 26px with a context of 16px

formula: `desired px value / parent context = em value`

26px/16px = 1.625em

###EM Unit Compounding problem

If nested, the context changes.

{% highlight css %}
.header {font-size: 2em;}
.header p {font-size: 1.625em} /* now based on the context of header.  */
{% endhighlight %}

original context = 16px

new context = 16px * 2 (32px)

.header p = 52px, as opposed to 16px which we may have thought it would.


##REM Units

REM stands for **R**oot *EM* Unit

REMs help resolve the compounding issues of EM Units because they are sized relative to the root element (html) of the page. They're not affected by inheritance like EM Units.

`.header p (font-size: 1.625rem}`

now equals 26px

Here's a sample:

<a class="jsbin-embed" href="http://jsbin.com/depedubixi/embed?html,css,output">JS Bin on jsbin.com</a><script src="http://static.jsbin.com/js/embed.min.js?3.35.5"></script>
