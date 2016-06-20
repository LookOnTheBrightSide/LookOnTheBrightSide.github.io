---
layout: post
title:  "Javascript life hack"
permalink: /blog/:title
categories: Javascript
introduction: Applying javascript code in the real world
---

##### Javascript to solve real problems

So we have been trying to find an apartment in Dublin and it has not been easy. There just isn't enough housing for everyone &#x1f625; An agent told us that everything is on a first come first served basis, meaning you have to be first to respond to the advert.

How was I going to do this? Well the site in question does not have a public api that I could maybe send automated responses. So I had do some silly hacking ...  a minute timer to disrupt you.
It's really hard to work with constant disruptions but it has to be done. Here is the code and all you have to do is paste it in your console in one of the tabs and make sure you don't close or refresh that tab.

{% highlight javascript %}
	var daftie = function() {
	      function reminder() {
	          alert("Refresh ____.ie, you are still homeless");
	      };
	      setInterval(reminder, 300000);
	   }
	 daftie();
 {% endhighlight %}