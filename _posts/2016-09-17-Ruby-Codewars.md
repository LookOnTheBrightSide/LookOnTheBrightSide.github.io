---
layout: post
title:  "Ruby Codewars"
permalink: /blog/:title
categories: Ruby
introduction: Ruby Codewars kata.
---

I have been working on Ruby for the past while in an attempt to up my Rails skills. The code below is for ```Return Two Highest Values in List``` kata on [Codewars](https://www.codewars.com/){:target="_blank" .site-link}.

I usually like to have everything on my own machine so I had to write the tests. The two files that I worked on are as follows:

{% highlight ruby %}
require 'minitest/autorun'
require './katas'

class KataTest < Minitest::Test
 def setup
  @kata = Kata.new
 end
 def test_two_highest
  assert_equal([20, 17], @kata.two_highest([15, 20, 20, 17]))
  assert_equal([11, 10], @kata.two_highest([10, 10, 11, 7]))
  assert_equal([120, 117], @kata.two_highest([5, 2, 120, 117]))
  assert_equal([], @kata.two_highest([]))
  assert_equal(false, @kata.two_highest(""))
	end
end
{% endhighlight %}

{% highlight ruby %}
class Kata
 def two_highest(arr)
  if arr.class == String
   return false
  elsif arr.empty? or arr == nil
   return arr
  else
   return [arr.sort.reverse.uniq[0],arr.sort.reverse.uniq[1]]
  end
 end
end
{% endhighlight %}

[Solutions](https://www.codewars.com/kata/return-two-highest-values-in-list/solutions/ruby/){:target="_blank" .site-link}

{% highlight ruby %}
def two_highest(arr)
 if arr.class == String
  return false
 elsif arr.empty? or arr == nil
  return arr
 else
  return [arr.sort.reverse.uniq[0],arr.sort.reverse.uniq[1]]
 end
end
{% endhighlight %}

After submitting I looked at all the solutions and found one that made me realise that I need to work more on refactoring my code. Basically going back to the basics ... "red, green, refactor".

The following is the solution in question which uses a ternary operator. ```test-expression ? if-true-expression : if-false-expression```.

{% highlight ruby %}
def two_highest(list)
 list.class != Array ? false : list.max(2)
end
{% endhighlight %}
