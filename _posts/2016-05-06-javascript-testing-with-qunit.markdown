---
layout: post
title:  "Introduction to QUnit testing"
permalink: /blog/:title
date:   2016-05-06 17:09:21 +0100
categories: javascript
introduction: This is an introduction to writing tests in javascript using QUnit.
---
##### Unit Tests
I am sure you have heard about "testing" in software development and wondered why it was necessary. This is an introduction post aimed at total beginners. Being a beginner myself, I would greatly appreciate it if experts also read this post and corrected/added to my take.

##### Why test?
Imagine I am your king and you are my servant. Everyday I leave a note for you describing what I want my next meal to be. It is entirely up to you how you source the ingredients.

A typical note might look like below:

{% highlight javascript %}
meal.delicious
//should be true
meal.hasPoison
//should be false
meal.calories
//should be 100
{% endhighlight %}

The above conditions should all be met in order for the tests to pass. So to make them pass I could the write the following:

{% highlight javascript %}
var meal = {
  delicious: true,
  hasPoison: false,
  calories: 100
}
{% endhighlight %}

So you made the king a peanut butter sandwich, all the conditions are met and the tests pass. The king is not happy! He does not eat peanuts...oops. He did not mention this to you so it's not your fault. He should have included this in his tests, no?  

##### More rigorous tests

Our tests can be as rigorous as we want them to be. So for instance the king could decide that his meals should not contain nuts, should not be hot, no chilli, weigh a maximum 50 grams, no sugar and all the ingredients should be organic.

{% highlight javascript %}
meal.delicious
//should be true
meal.hasPoison
//should be false
meal.calories
//should be 100
meal.hasNuts
//should be false
meal.hot
//should be false
meal.weight
//should be 50 or less
meal.hasSugar
//should be false
meal.organic
//should be true
{% endhighlight %}

You see, now there is very little room for the king to be disappointed with his meal if all the tests pass. So the more rigorous you are, the less room there is for error.

##### QUnit

To get started we will use qunit (a javascript testing framework) to test some code. We will set it up and then make our tests pass.

##### Set Up

Make a folder and name it what you will.
In the folder make 2 files named ```app.js``` and ```index.html```.

In your index.html include the following code

{% highlight html %}
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>QUnit Example</title>
  <link rel="stylesheet" href="https://code.jquery.com/qunit/qunit-1.23.1.css">
</head>
<body>
  <div id="qunit"></div>
  <div id="qunit-fixture"></div>
  <script src="https://code.jquery.com/qunit/qunit-1.23.1.js"></script>
  <script src="app.js"></script>
  <script src="test.js"></script>

</body>
</html>
{% endhighlight %}

The id's ```qunit``` and ```qunit-fixture``` are simply for styling purposes needed by qunit. QUnit also requires jquery and jquery ui. These are added via the the first script tag.
The next two files are where we will actually write our code. ```app.js``` will have our code that will be checked by the next file, which hosts our QUnit tests ```test.js```.
So to get started we need to write a test in ```test.js```. The test can look something like this:

{% highlight javascript %}
QUnit.test('length', function(assert) {
    assert.equal(length("Sam"), 3);
});
{% endhighlight %}
***
[QUnit api documentation](http://api.qunitjs.com/category/assert/){:target="_blank" .site-link}

***

If we then run ```index.html``` in the browser we will see that we have a failing test.

![failing test screenshot](http://i.imgur.com/KfMWQLR.png){: .img-fluid .img-center}

So to make it pass we need to write some code!

From looking at the code we can tell that we need to write a function that takes in a single parameter and returns the parameter's length. To make this test pass we can then add the following to ```app.js```:

{% highlight javascript %}
var length = function(name) {
	return name.length;
}
{% endhighlight %}

And now we have a passing test!
![passing test screenshot](http://i.imgur.com/6cjXKJS.png){: .img-fluid .img-center}

*****
The final code can be found on my github [here](https://github.com/LookOnTheBrightSide/qunit_base){:target="_blank" .site-link}.
