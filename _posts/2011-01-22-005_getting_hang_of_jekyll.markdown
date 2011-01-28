---
layout: default
title: "005_getting_hang_of_jekyll"
published: false
style: text
---

# What I've learned so far

I now have 3 themes for [Jekyll](https://github.com/mojombo/jekyll).  I've learned few things about it.

- Utilize YAML Front Matter values

  I have been using *style* value in YAML Front Matter to change style by using CSS, but I found out that you can use *page.layout*.

 <script src="https://gist.github.com/790906.js?file=using.page.layout.to.switch.metadescription.rb"></script>
 


 If you add description value at YAML Front Matter, you don't have to hard code description like example above.

 Having too many required values in YAML Front Matter is not good things to do, but they can be great helper to build themes lot easier.

- Now I can kill jekyll --server --auto process

  I asked question at my article/([002_jekyll_newbie_guide](http://layouts.studiomohawk.com/2011/01/09/002_jekyll_newbie_guide/)/) about this one.  Now I've found solution.
  This might not be the best way to achieve but this gets jobs done for me.

{% highlight bash linenos %}
	ps aux | grep ruby
{% endhighlight %}
 
 This one line gives find ruby related processes(I guess) so that you can find out pid(I'm guessing this is process ID) for jekyll --server --auto
 then you can

{% highlight bash linenos %}
	kill -9 PID(substitute with digits you found from about code)
{% endhighlight %}

 this to kill process.

- I'm looking for a solution to list all categories

  I have searched and tried most of solutions floating around on internet on this one.

  I have yet to find solution.  If you know, please let me know.
