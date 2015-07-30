---
layout:     post
title:      Getting started with Sass - Mac lovers
date:       2015-07-30 11:30:00
picture:    /images/sass/main.png
summary:    When you decide to use Sass in your project, it's important to take into account that you can choose between installing specific applications or using the command line. This post explains how to set up Sass with the latter option on Mac.

categories: 
---
<div class="center">
  <img src="/images/sass/main.png">
</div>

<span class="small">_Original image by [Unsplash](https://unsplash.com/)_</span>

When you decide to use [Sass](http://sass-lang.com/) (Syntactically Awesome Stylesheets) in your project, it's important to take into account that you can choose between installing specific applications or using the command line. This post explains how to set up Sass with the latter option on Mac.

### 1- Install Sass

Sass is a library built upon Ruby, so we'll need to use the Ruby gem utility to install it. If you’re using a Mac this step will be pretty painless, since this usually comes with a Ruby version preinstalled.

Let's start by opening your Terminal and typing:

{% highlight bash %}
$ gem install sass
{% endhighlight %}

![image](/images/sass/sass_1-1.png)

As this example show, you might run into an error installing this gem — this is because you need administration privileges to do this. Just use <span class="light-gray">sudo</span>, which runs the command as the root user. 

{% highlight bash %}
$ sudo gem install sass
{% endhighlight %}

After a successful installation you'll get a message like this:

![image](/images/sass/sass_1-2.png)

We can also check it's alright by typing:

{% highlight bash %}
$ sass -v 
{% endhighlight %}

### 2- Install Compass

Let's go ahead and add Compass, an open-source CSS framework that provides powerful tools for Sass. Compass allows you to build efficient and maintainable stylesheets in a very user friendly way. Learn more about compass [here](http://compass-style.org/). 

To install it we'll also use <span class="light-gray">sudo</span>.

{% highlight bash %}
$ sudo gem install compass
{% endhighlight %} 

![image](/images/sass/sass_2.png)

### 3- Create a new project with Compass 

Once Sass and Compass are up and running, it's time to set up our Sass project. First, let’s locate the directory where you want to create it.

{% highlight bash %}
$ cd <directory-path>
{% endhighlight %}

If you want to use the SCSS syntax in your project, run:

{% highlight bash %}
$ compass create <myproject>
{% endhighlight %}

Or, if you prefer the Sass syntax instead, type: 

{% highlight bash %}
$ compass create <myproject> - -syntax sass 
{% endhighlight %}

Once your Compass project has been created, you'll get a successful message like this one:

![image](/images/sass/sass_3.png)

### 4- Configure your project

In the base directory of your project you'll have:

- config.rb, where you can configure properties. Look &nbsp;[here](http://compass-style.org/help/documentation/configuration-reference/) for further details.
- sass, where you'll put your CSS code.
- stylesheets, where the CSS will be compiled.

![image](/images/sass/sass_4-1.png)

The first thing we need to do is to configure the Ruby file config.rb with an editor like Sublime. Let's specify where your Sass, CSS, images and javascript files will be placed. 

Here's how I set the properties. The only change I made was adding a folder called “assets” to store the files I mentioned above.

![image](/images/sass/sass_4-2.png)

### 5- Compile your project Sass into CSS with Compass 

First make sure you’re in your project folder.

{% highlight bash %}
$ cd directory-path/myproject 
{% endhighlight %}

There are two ways to compile your Sass stylesheets:

{% highlight bash %}
$ compass watch
{% endhighlight %}

![image](/images/sass/sass_5.png)

This will monitor all changes in your project and recompile Sass files automatically. With this option, you'll always keep your CSS files up to date.

{% highlight bash %}
$ compass compile
{% endhighlight %}

This means it works on demand, so whenever you run this command your CSS files will be compiled.

Congratulations! You're ready to make the most of what the Compass framework provides.

If you haven't had the chance to get your hands dirty with it yet, check the following resources to get started!

### Some guides:

- [Best practices](http://compass-style.org/help/tutorials/best_practices/) - Compass documentation

- [Sass basics](http://sass-lang.com/guide) - Sass-lang

- [Style guide](http://sass-lang.com/styleguide/typography) - Sass-lang

- [Sass documentation](http://sass-lang.com/documentation/file.SASS_REFERENCE.html) - Sass-lang

Tutorials and examples:

- [Code examples](http://compass-style.org/examples/) - Compass documentation

- [Sass snippets](https://css-tricks.com/snippets/sass/) - CSS Tricks

### More specific:

- [Compass Reset](http://compass-style.org/reference/compass/reset/) - Compass documentation

- [Media queries in Sass](https://css-tricks.com/approaches-media-queries-sass/) - CSS Tricks

- [Responsive Web in Sass](http://thesassway.com/intermediate/responsive-web-design-in-sass-using-media-queries-in-sass-32) - The Sass Way

- [Susy grids](https://css-tricks.com/build-web-layouts-easily-susy/) - Susy 
