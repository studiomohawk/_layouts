---
layout: post
title: "Host a Static Website on Amazon S3"
published: true
---

You may already noticed that Amazon S3 is able to host static websites now.  
If you are like me, you always wonder what the fuss about all the cloud talking among developers.  
And I'm not that kinda guy who can let it go or pretend it's nothing.  
So here I am, I'm having the cloud experience right now.

## \_layouts is now hosted on Amazon S3.

Does my website need a could server?  
I'm pretty sure it doesn't, but I've learned few things and it was fun doing it.  

I'll share my little experiment with whoever read this blog.  
I don't think no one does, so it'll be like my memo.

## Motivation behind it

I did want to know what it's all about to have my site on cloud.  
I stumbled upon press release of Amazon saying S3 is now capable to host static
websites.  
And I do have static website created by
[Jekyll](https://github.com/mojombo/jekyll).

Then I found an article by digital inspiration, [How to Host Your Website on Amazon S3](http://www.labnol.org/internet/web-hosting-with-amazon-s3/18742/).

## Let's get to the tutorial part

I've follow the tutorial except when he uses Amazon S3 Console.  
Since I am using Jekyll, I've learned to use rsync to upload my update to the
server.

Though I've never tried, I assume I cannot use ssh and rsync to Amazon S3. So
I went out to search alternatives.  
What I've found was [S3sync](http://www.s3sync.net/wiki).  
It's easy to install on my Mac.

{% highlight sh %}
gem install s3sync
{% endhighlight %}

It's written in ruby and packaged using gem (though it's not the latest one).  
It's not a equivalent of rsync but pretty much the same.  
I still need to read the document but it is fairly easy to use if you already
familiar with rsync.

I did used Amazon S3 Console to create a bucket (which is like a directory for
Amazon Web Service, I guess), to make contents of bucket public and to make
a bucket treated as website.  
All of those is one time task so I don't need to do that again for while.  
(S3Sync has a sibling command called s3cmd which arrows you to create a bucket)

## There are few things you need to be aware of

If you need to have your domain points to Amazon S3 (I assume that's mostly
everybody), you need to name your bucket **www.YOUR-DOMAIN-NAME.WHATEVER** like
this.

**www** is crucial since you need change something called CNAME setting on your
domain provider(Mine is GoDaddy).  
I still don't quite understand what CNAME is after reading Wikipedia entry, but
I'm guessing that you only can point subdomain (and I'm guessing www IS a
subdomain) with CNAME.  

Well, I've tried without **www** but no luck so if you know better than I am
please help me on this.

And since Amason S3 is not an Apache server, you can't use .htaccess to do all
the tricks.  

I need help on this one too.

**Are there anyway I can do .htaccess tricks on Amazon S3?**

That's it!  
Isn't it easy and fun?

I do still have a few minor things to iron out, but I can live with it, at
least for a while.  

If you are a server ninja who can help me, please give me your shout at [Twitter@cssradar](http://twitter.com/#!/cssradar).
If you are like me and having problems on hosting static website on Amason S3,
I'd love to help you.
