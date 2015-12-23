---
layout: post
title:  "Type Coercion"
date:   2015-12-22 09:59:53 -0500
category: javascript
categories: javascript
---

Javascript does some neat and unexpected things when you mix types (`string`, `boolean`, `number`, `object`, etc.)


##Mixing Numbers with Undefined
{% highlight javascript %}
console.log( 10 * null);
// 0
{% endhighlight %}

##Adding Strings & Numbers
Javascript concatenates the string and the number (converting the number to a string).
{% highlight javascript %}
console.log( "20" + 5);
// 205
{% endhighlight %}

##Subtracting Strings & Numbers
Javascript converts the string to a number and subtract.
{% highlight javascript %}
console.log( "20" - 5);
// 15
{% endhighlight %}

##Multiplying Strings & Numbers
Javascript doesn't know what the heck to do with this.
{% highlight javascript %}
console.log( "20" * 5);
// NaN
{% endhighlight %}

##Combining Booleans & Numbers
In Javascript, zero is false. Any non-zero number is true.

{% highlight javascript %}
console.log( false == 0);
// true

console.log(false != 0);
// false
{% endhighlight %}
`0`, `NaN` and `""` (empty string) are all false.