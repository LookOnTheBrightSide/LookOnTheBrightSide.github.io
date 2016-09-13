---
layout: post
title:  "Free Code Camp in Ruby"
permalink: /blog/:title
categories: Ruby
introduction: Doing Free Code Camp's algorithms in Ruby.
---
It's been a while since I wrote a post &#128582;. I have been working on personal projects and learning Python and React in between. I have also since started doing full-stack Ruby on Rails development on my own.

I have worked as a front-end developer on Rails applications before but never really took the time to dive into the framework's backend side of things. I really like Rails' "convention over configuration" convention. This means I can jump into any application and start working without having to figure out the projects structure for example.

Since I decided to go with Rails, I knew the best place to start would be with the language itself. I have done the Free Code Camp algorithms in the past and thought they were really good. Due to this I will implement them in Ruby, which means writing tests first. I'll be using Test Unit for this. The following is for the first "Reverse a String" algorithm on Free Code Camp.

{% highlight ruby %}
require "test/unit"
	class StringReverseTest < Test::Unit::TestCase
		def test_string_reverse
			string = "hello"
			assert_equal('olleh', string.reverse)
		end
	end
{% endhighlight %}

I am still trying to figure out the best way to test individual methods in a way that's similar to javascript's QUnit. Until then ... &#128587;