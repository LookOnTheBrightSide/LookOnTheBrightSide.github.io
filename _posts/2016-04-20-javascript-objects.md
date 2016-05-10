---
layout: post
title:  "Javascript Objects 101"
permalink: /blog/:title
categories: Javascript
introduction: Javascript Objects, the fundamentals.
---

Objects store data. This data can be of any type.
Whenever you use a dot in javascript you're dealing with an Object.

##### Constructor notation

{% highlight javascript %}
var bottle = new Object();
// creates an empty object
{% endhighlight %}

##### Object literal notation

{% highlight javascript %}
var bottle = {};
bottle.material = "plastic";
bottle.fragile = false;
bottle.color = "green"
{% endhighlight %}

##### Alternative syntax

{% highlight javascript %}
var box = {
  "material" : "plastic",
  "fragile" : false;
  "color" : "green"
}
{% endhighlight %}

##### Access with dot notation

{% highlight javascript %}
bottle.material
// plastic
{% endhighlight %}

##### Access with bracket notation

{% highlight javascript %}
bottle["material"]
// plastic
{% endhighlight %}

##### Store things by value

{% highlight javascript %}
var fantaBottle = bottle.material
// plastic
bottle.material = "glass"
// "glass"
fantaBottle;
// "plastic"
{% endhighlight %}
The fanta bottle is still plastic because where ```fantaBottle``` is saved in memory, it is plastic.

##### Access using variables

{% highlight javascript %}
var bottleType = "material";
bottle[bottleType];
// glass
// notice you do not need quotes
// if you use quotes it will return undefined because
// we do not have a property called "bottleType"
{% endhighlight %}

##### Methods

{% highlight javascript %}
bottle.isFragile = function(){
  if  (this.fragile === true)  {
    return true;
  }
  return false
}
{% endhighlight %}

The same can be achieved with:

{% highlight javascript %}
var box = {
  "material"  : "plastic",
  "fragile"   : false;
  "color"     : "green",
  isFragile : function(){
                if  (this.fragile === true)  {
                  return true;
                  }
                return false
                  }
}

// Note that we don't need to store the keys as strings.
// They are assumed to be strings.
// You just need to be consistent.
{% endhighlight %}

{% highlight javascript %}
bottle.isFragile();
// true
{% endhighlight %}

##### Iteration

'For in' loops can be used to loop Objects in Javascript

{% highlight javascript %}
for(var key in bottle){
  if( bottle.hasOwnProperty(key)){
    console.log(key + " : " + bottle[key]);
  }
}
// Note that when you loop Objects in Javascript there is no
// guarantee that they will come back in order that you made object.
// We use "hasOwnProperty(key)" because
// we only want to loop the bootle Object.
// key and prop are common but you can name this anything that you want.
{% endhighlight %}
