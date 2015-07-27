---
layout:     post
title:      Make beatiful websites using Google Fonts
date:       2015-03-16 11:30:00
picture:    /images/google-fonts/main.jpg
summary:    It's time to leave behind the most common typefaces, and start using those that really make your web pages more attractive! You’ll be surprised how a beautiful typeface can change the overall user experience.

categories: 
---

![Test image](/images/google-fonts/main.jpg)

<span class="small">_Image by [Picjumbo](https://picjumbo.com/webdesign-layout-sketching/)_</span>

It's time to leave behind the most common typefaces, and start using those that really make your web pages more attractive! You’ll be surprised how a beautiful typeface can change the overall user experience.

In this post we'll take a look at using&nbsp;[Google Fonts](https://www.google.com/fonts "Google Fonts")&nbsp;to make your website more readable and engaging. Back some time ago we had a limited number of typefaces available, but currently we can embed a wide range of fonts through HTML and CSS stylesheet.

[Google Fonts&nbsp;](https://www.google.com/fonts "Google Fonts")offer their awesome typefaces with free license, so the only thing we have to do is to make sure we have the right to do so. Let's follow this steps to include typefaces in your next site:

1-&nbsp;[Explore](https://www.google.com/fonts)&nbsp;and choose from countless of fonts that Google provides for free. When you've found the one that best suits you, let's click the “Add to your collection” button.

![image](/images/google-fonts/1-add.png)

Then, you can select which font weights you'd want to use. Typefaces provide weight that can vary from 100 (Thin) to 900 (Ultra-Bold).

![image](/images/google-fonts/1-weight.png)

2- You can add more fonts to your collection and compare them using the “Review” button. Let's check how your chosen fonts look like in paragraphs or headlines.

![image](/images/google-fonts/2-review.png)

3- By clicking on “Use” button, you can verify the font weights selected.&nbsp;

![image](/images/google-fonts/3-use.png)

Then, you can copy the code given by Google and embed this &lt;link&gt; into the &lt;`head`&gt; element of your HTML document.

![image](/images/google-fonts/3-head.png)

Your HTML document should look like this:

{% highlight html lineanchors%}
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Google Font Example</title>
    <link rel="stylesheet" href="assets/stylesheets/main.css">
    <link href='http://fonts.googleapis.com/css?family=Lato:100,300,400,700|Oswald:400,300,700' rel='stylesheet' type='text/css'>
  </head>
  <body>
    <h1>Google Font Example</h1>
    <a href="#" class="btn">Home</a>
    <a href="#" class="btn">About</a>
    <a href="#" class="btn">Services</a>
    <a href="#" class="btn">Contact</a>
  </body>
</html>
{% endhighlight %}

4- Finally, include the font name and font weight in your CSS style as follows:

{% highlight css lineanchors %}
body{
  padding:75px;
  background:#16a085;
  font-family: 'Lato', sans-serif;
  font-weight:200;
  text-align:center; 
}

h1{
  font-family: 'Oswald', sans-serif;
  font-weight:100;
  color:#fff;
}
{% endhighlight %}

**Worried about how to combine Google Fonts?**

![image](/images/google-fonts/6-example.png)

If you'd like to know about how best to combine fonts, you only have to add the typeface selected at the end of this URL: www.google.com/fonts/specimen/**font**

For instance, in the previous example I wanted to combine ‘Oswald’ font, so I had a look at this URL:
&nbsp;[https://www.google.com/fonts/specimen/Oswald](https://www.google.com/fonts/specimen/Oswald)

Then, by clicking on ‘Pairings’ you'll find out lovely combinations that will be useful to use in your next project!

![image](/images/google-fonts/7-pairing.png)

I hope you can come across great combinations that really fit with your purpose. Let me know what combinations you feel are more inspiring!


