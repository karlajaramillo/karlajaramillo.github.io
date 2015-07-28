---
layout:     post
title:      Starting my resolution list for 2015. Specificity weight of selectors
date:       2015-01-11 11:30:00
picture:    /images/selectors/main.png
summary:    With the new year the people usually make a list of resolutions, in my case an important one will be to dive deeper into coding. It sounds easy to just change my career into programming, but I soon ran into questions like which language should I choose for a start. Since I'd like to build web and mobile applications, I decided to start with CSS and HTML.

categories: 
---
<div class="center">
  <img src="/images/selectors/main.png">
</div>

<span class="small">_Image by [Startup Stock Photos](http://startupstockphotos.com/)_</span>

With the new year the people usually make a list of resolutions, in my case an important one will be to dive deeper into coding.

It sounds easy to just change my career into programming, but I soon ran into questions like which language should I choose for a start. Since I'd like to build web and mobile applications, I decided to start with CSS and HTML.

I'm extremely happy with the course I chose to begin my journey: [Learn to Code HTML &amp; CSS by Shay Home&nbsp;](http://learn.shayhowe.com/html-css/ "ShayHowe")

In the four days I've been practicing one of the most useful concepts I've learned: the `specificity weight of selectors`.

In a CSS stylesheet the selector's style will cascade from top to bottom. However, when a different kind of selectors come into play we need to keep in mind their specificity weight.

You'll see #-#-# three columns. The left one weighs more than the middle and the right ones. To calculate the specificity weight of a selector you need to consider that ID selectors weigh more than class selectors, and class selectors weigh more than type selectors:

* Type selector: 0-0-1. The lowest specificity. Last column is for Type selectors.

* Class selector: 0-1-0. Medium specificity. Middle column is for Class selectors.

* ID selector: 1-0-0. High specificity. First column is for ID selectors.

Let's take the example below. We can calculate the specificity of .col-1-3 code.color-section and .col-1-3 code#color-section-id:

[![image](/images/selectors/selector.png)](http://jsfiddle.net/kavajaga/xg383y9x/2/ "Specificity weight of selectors")

`.col-1-3 code#color-section-id`

It has three selectors, one class (0-1-0), one type selector (0-0-1) and one ID selector (1-0-0). Adding the type of selectors the total value would be 1-1-1.

`.col-1-3 code.color-section`

It has three selectors, two classes (0-1-0 + 0-1-0) and one type selector (0-0-1). Adding the type of selectors the total value would be 0-2-1.


After combining selectors, the first one has a higher specificity weight which results in more precedence within the cascade no matter their order in our CSS stylesheet.

Click below to see it live:

[![image](/images/selectors/example.png)](http://jsfiddle.net/kavajaga/xg383y9x/2/ "Specificity weight of selectors")


