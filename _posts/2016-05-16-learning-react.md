---
layout: post
title:  "Learning React"
permalink: /blog/:title
categories: React
introduction: ReactJS beginnings.
---
![image](https://facebook.github.io/react/img/logo.svg){: .img-fluid .img-center .blog_post--image}

Ok, so today I began my journey in learning React. I started off by doing the official [Faceboook tutorial](https://facebook.github.io/react/docs/tutorial.html) which I am now halfway through.

##### Take Aways

The main thing that I picked up is that ```React.create()``` is passed an object with some javascript methods. You need to have a ```render()``` method that will actually create the DOM node. You can actually return anything like a tree of components for example.

```ReactDOM.render()``` takes in the component that you want to be rendered as the first argument and the second argument will be the where it will be injected.
It should be called after your components.

Html tags and components can be mixed up in JSX.

The easiest way to get started with React is through the official tutorial. I had previously tried but failed in the tooling stage due to my inexperience with Webpack.

In the next few days I will continue learning react and will try to connect to some api for a simple app.

to be continued ...
