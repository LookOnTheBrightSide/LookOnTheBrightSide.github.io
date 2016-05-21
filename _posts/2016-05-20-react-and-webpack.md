---
layout: post
title:  "Getting started with Webpack"
permalink: /blog/:title
categories: React and Webpack
introduction: The ReactJS journey continues ...
---

##### The journey continues

So continuing with learning React I am now at a point where I understand what problem it solves. To be able work with React in a team I realised that I will need to know [Webpack](https://webpack.github.io/){:target="_blank" .site-link} and some [ES6/2015](https://tc39.github.io/ecma262/){:target="_blank" .site-link}.

##### What Webpack does
It is a build tool. Mostly, while working with React we need it for Combining files, minifying, maintaining file order, transpiling, linting and many more other tasks. An alternative would be to use Task Runners such as Gulp and Grunt.
The difference between Webpack and Task Runners is that Webpack is specialized, it takes an input file and spits out an output file. It uses loaders to do this. Webpack does not work with Bower.

The files produced are often called bundles and this has been the common naming convention.

***
You'll need to have installed node and the webpack cli

***

Provided we have an app.js file in our root folder we can then run the following:


```$ webpack ./app.js bundle.js```

The above command generates a bundle.js file from the code in ```app.js```

```webpack.config.js```


This file helps us avoid typing the parameters in the command line.

{% highlight javascript %}

module.exports = {
	entry: "./app.js",
	output: {
		filename: "bundle.js"
	}
}

{% endhighlight %}

The above will enable us to just run ```$ webpack``` from the command line.

##### Extras
Some addons that helpful in development are the ```--watch flag```. It basically watches for changes in your files and bundles when you save the changes.

##### Webpack-dev-server

Another useful one is the ```webpack-dev-server``` which is a nodejs server for Webpack.

```
$ webpack-dev-server
```

This brings to the table a really useful feature which is auto-refresh in the browser! This can increase productivity by saving you time of switching windows. The only thing worth mentioning is that it also adds a status bar that can be removed by entering the --inline flag

```
$ webpack-dev-server --inline
```

##### Loaders

To use features like ES6/ES2016 we need loaders. These loaders can be entered into the ```webpack.config``` file like so:


{% highlight javascript %}
module.exports = {
    entry: ["./master","./app.js"],
    output: {
    	filename: "bundle.js"
    },
    watch: true,
    module:{
    loaders:[
    	{
        test: /\.es6$/,
        // regex to check all the files with
        // the .e6 extension to run through the loader
        exclude: /node_modules/,
        // ignore files in this folder
        loader: "babel-loader"
        // name of the loader we are using
    	}
    ]
    },
    resolve: {
      extensions: ["",".js", ".es6", ".futurejs"]
      // webpack checks for all .js files but here you
      // can states which other one you want to be checked
      // without specifying the extension
    }
}
{% endhighlight  %}

##### Preloaders

We can use preloaders in bundling. These are run before the loaders. An example of this would be ```jshint-loader``` which is just a linter. They are implemented in the same way as loaders except they are named ```preLoaders```

Warnings and Errors can then be viewed in the terminal and browser console should there be any.
