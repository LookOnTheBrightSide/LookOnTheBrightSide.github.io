---
layout: post
title:  "CSS Box Model"
permalink: /blog/:title
categories: CSS
introduction: CSS box model basics
---

##### The CSS Box Model

Ok it's been a while since I posted. This time I wanted to visit the basics of frontend development - "The CSS Box Model". I know this used to trip me up in the beginning so I decided to do a post on it.

The box model is basically a box that wraps all html elements that get rendered. I think it will be best to think of these elements as "boxes". They can be displayed as either ```block or inline-block```. To see this visually we can put a border on every element on any website. This can be done by selecting every element and applying a border.

{% highlight css %}
* {
	boder: 1px solid rebeccapurple;
}
{% endhighlight %}


Block elements take full width of the page. Some of these are :
```div
p
h1
etc```

Inline elements do not force new lines. Some are :
```strong
input
span
etc```

What we will need to master will be:
```
margin, padding, border and content
```

Content is self explanatory, this is the content that is between the tags. Something to note here is that some styles will not be applied if there is nothing between the tags i.e if the content is empty.

Padding is applied to "cushion" the content

Border is around the the element.

Margin goes on the outside and it can take negative values.

##### Display

To change the way elements are displayed we use ```display```. This can either be :
```none, inline, inline-block or block ```
None removes the element from the DOM tree.
Block is the default for block elements.
Inline is the default for inline elements.
Inline-block allows for inline elements to respond to hieght, width and margin. Negative top and botton margins will not work for inline-block.

##### Visibility

When set to hidden, content will be hidden but it will still take up space on the page. This has the oppposite effect to ```display: none```

##### Calculating width
Initially, CSS layout way a tricky because of the width. The width was a total of padding and border on either side plus the contents width. This requires some calculations to get right.

##### Box-Sizing
In CSS3 we can use ```box-sizing: border-box``` to force the border and padding into width and height instead of adding to it.

##### Overflow
When we specify a height on an element but have too much content, the content will overflow. If we do not want this behaviour, the overflow property allows us to change this with either ```hidden, visible, scroll or auto```. Hidden will clip any content that overflows. Auto will only show scroll bars when needed, and scroll will show a scroll bar. There might be minor differences with different browsers.

##### Float

Float allows us to "float" elements on a page. It accepts 3 values, ```left, right, none```. None is the default value. Float is the probably the hardest to get your head around. Floated elements are pulled out of the normal flow of elements. Floated elements might cause the container div to collapse. This is because the container element will have no "regard" for floated children. To fix this we can add ```clear: left/right/both``` to parent element. Another efficient technique that has been used to solve this is called clearfix. This class is attached to the container class. You can read more about it here.

With flexbox becoming more popular and it's support growing, the use of floats might go away in the near future.


Until next time folks!