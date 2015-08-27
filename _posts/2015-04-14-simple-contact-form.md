---
layout:     post
title:      How to create a simple contact form
date:       2015-04-14 11:30:00
picture:    /images/contact-form/main.png
summary:    One of the most common sections you'll find in a website is a Contact Form, and it was unavoidable that I had to tackle this in my current project. In this post I'd like to share with you an easy way to build a contact form from scratch. 

categories: 
redirect_from:
  - /post/109767703457
  - /post/109767703457/
  - /post/109767703457/simple-contact-form
  - /post/109767703457/simple-contact-form/
---
<div class="center">
  <img src="/images/contact-form/main.png">
</div>

One of the most common sections you'll find in a website is a Contact Form, and it was unavoidable that I had to tackle this in my current project. In this post I'd like to share with you an easy way to build a contact form from scratch. 

Let’s start with your HTML document:

* First, you can include Google Fonts to make more attractive your contact form ([see how to do it in my previous post](http://karlajaramillo.github.io/2015/03/16/make-beatuful-websites-using-google-fonts/)).

* Add a &lt;`form`&gt; element, which will wrap different elements and attributes of the contact form. Apply _action_ (URL to which the information will be sent) and _method_ (HTTP method to submit the data) attributes to the form element.

* Create a &lt;`fieldset`&gt; element inside the &lt;`form`&gt; for a better organization. Fieldset is a block-level element that will wrap form elements. This &lt;`fieldset`&gt; includes a border outline by default, which we'll modify within the CSS sheet.

* Add &lt;`input`&gt; elements to get information from users, using the type attributes. Some of the [input types](http://html5doctor.com/html5-forms-input-types/) for forms are: text, password, email, date, time, url, search, tel, number, range…

* Use &lt;`textarea`&gt; element to collect user's comments.&nbsp;

* Add &lt;`input`&gt; element with the submit  attribute (type="submit") to process user data.

* Provide a hint within the form with placeholder attribute, which will disappear once the user click on the input area.

* If you want to ensure that users complete information, use a required attribute, which will also check if an email input is correct.

{% highlight html lineanchors%}
<!DOCTYPE html>
<html lan="en">
<head>
<link rel="stylesheet" type="text/css" href="assets/stylesheet/main.css">
<link href='http://fonts.googleapis.com/css?family=Lato:100,300,400|Pacifico' rel='stylesheet' type='text/css'>
</head>
<body>
  <h1>Simple Contact Form</h1>
  <!-- Contact Form -->
  <form action="#" method="post">
    <fieldset class="contact-form">
      <input type="text" name="name" placeholder="Name" required>
      <input type="email" name="email" placeholder="Email address" required>
      <input type="text" name="subject" placeholder="Subject" required>
      <textarea name="message" placeholder="Add your message here" required></textarea>
      <input type="submit" id="submit" value="Submit" >
    </fieldset>
  </form>
</body>
</html>
{% endhighlight %}

This is the result:
![Image](/images/contact-form/a_web.png)

Now, let's add some styles within out CSS stylesheet to polish our contact form:

* Add the box-sizing property, using border-box value to make sizing all of our elements much easier. It will maintain the element's width no matter the padding or border values they have. Use the universal selector * to select all the elements and apply the box-sizing property.

{% highlight css lineanchors%}
*,
*:before,
*:after {
  -webkit-box-sizing: border-box;
     -moz-box-sizing: border-box;
          box-sizing: border-box;
{% endhighlight %}

* Custom styles for the body and headlines, including the typefaces chosen through Google Fonts:


{% highlight css lineanchors%}
body {
  color: #bfbfbf;
  font-family: 'Lato', 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif;
  background: rgba(245,245,245,1);
}
h1 {
  font-family: 'Pacifico', 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif;
  text-align: center;
  text-shadow: 2px 2px 0px rgba(255,255,255,.7), 5px 7px 0px rgba(0, 0, 0, 0.1);
}
{% endhighlight %}

* Add attributes to the &lt;`form`&gt;, center the elements within the form and include a maximum width. Then, eliminate the border by default from the &lt;`fieldset&gt; element:

{% highlight css %}
form {
  max-width: 600px;
  text-align: center;
  margin: 0 auto;
}
fieldset {
  border: 0;
  margin: 0;
  padding: 0;
}
{% endhighlight %}

* Configure .contact-form class for input and textarea elements. To get rid of the blue outline they have by default, set the outline property to 0 (cero). You also can enhance the user’s experience adding more space to the textarea element with the use of height property.

{% highlight css %}
.contact-form input,
.contact-form textarea {
  border: 0;
  outline: 0;
  display: block;
  width: 100%;
  margin-top: 1em;
  padding: .8em;
  font-family: 'Lato', 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif;
  font-weight: 300;
  font-size: 14px;
  border-radius: 6px;
  box-shadow: 0 1px 1px rgba(34,34,34,0.1);
  resize: none;
}
.contact-form textarea {
  margin-bottom: 1em;
  height: 125px;
}
{% endhighlight %}

* Style the element that is currently activated by the mouse or targeted by the keyboard, adding `box-shadow` property to the `:focus` pseudo-class.

{% highlight css %}
.contact-form input:focus {
  box-shadow: 0 0px 2px rgba(3,201,169,1)!important;
}
.contact-form textarea:focus {
  box-shadow: 0 0px 2px rgba(3,201,169,1)!important;
} 
{% endhighlight %}

* Submit input is used to process the user data, we'll add `:hover` pseudo-class to change the color when the mouser hovers over it:

{% highlight css %}
#submit {
  color: white; 
  background-color: #bfbfbf;
  cursor: pointer;
  font-weight: 400;
}
#submit:hover {
  background-color: rgba(3,201,169,.6);
}
{% endhighlight %}

That’s it! this is a simple contact form to add in your web page. Feel free to [customize](http://jsfiddle.net/kavajaga/4je44kz8/1/) it with your favorite styles.

[![image](/images/contact-form/b_web.png)](http://jsfiddle.net/kavajaga/4je44kz8/1/)

If you feel that you'd like to include some icons to make your contact form even more stunning, I'll recommend to try with [FontAwesome icons](http://fortawesome.github.io/Font-Awesome/). First, you'll find out some ways to [get started&nbsp;](http://fortawesome.github.io/Font-Awesome/get-started/)with Font Awesome, I chose to download the library and reference the location to my font-awesome.min.css

* Include in the `head` of your HTML document the reference to your font-awesome.min.css.

{% highlight css %}
<link rel="stylesheet" href="assets/font-awesome/css/font-awesome.min.css">
{% endhighlight %}

* Add &lt;`div`&gt; elements to wrap the icons. Then, [choose icons](http://fortawesome.github.io/Font-Awesome/icons/), click on them and copy the snippet provided into your HTML document.

I add also a .wrapper class to use it later in the CSS sheet. See examples about how to use Font Awesome icons [here](http://fortawesome.github.io/Font-Awesome/examples/).

{% highlight html %}
<form action="#" method="post">
  <fieldset class="contact-form">
    <div class="wrapper">
      <i class="fa fa-user"></i>
      <input type="text" name="name" placeholder="Name" required>
    </div>
    <div class="wrapper">
      <i class="fa fa-envelope"></i>
      <input type="email" name="email" placeholder="Email address" required>
    </div>
    <div class="wrapper">
      <i class="fa fa-quote-right"></i>
      <input type="text" name="subject" placeholder="Subject" required>
    </div>
    <div class="wrapper">
      <i class="fa fa-comments"></i>
      <textarea name="message" placeholder="Add your message here" required></textarea>
    </div>
    <input type="submit" id="submit" value="Submit" >
  </fieldset>
</form>
{% endhighlight %}

* In your CSS configure the .wrapper class and icon's properties, such as color or position.

{% highlight css%}
.wrapper {
  position: relative;
}
.fa-user,
.fa-envelope,
.fa-quote-right,
.fa-comments {
  color: #bfbfbf;
  position: absolute;
  top: 12px;
  left: 15px;
}
{% endhighlight %}

* Finally, change the `padding` property to add some space between icons and placeholder's boxes.

{% highlight css%}
.contact-form input,
.contact-form textarea {
  border: 0;
  outline: 0;
  display: block;
  width: 100%;
  margin-top: 1em;
  padding: .6em .06em .6em 2.8em;
  font-family: 'Lato', 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif;
  font-weight: 300;
  font-size: 14px;
  border-radius: 6px;
  box-shadow: 0 1px 1px rgba(34,34,34,0.1);
  resize: none;
}
{% endhighlight %}

This was the result of this simple contact form using Font Awesome icons.
![Main image](/images/contact-form/main.png)

It is really worth it to start coding, and I feel really happy with what I’ve learnt so far. I'd love to hear your feedback and your experience.









