---
layout: post
title: "Jekyll Newbie Guide"
published: true
---

##A Newbie(like me) Guide for Jekyll

###Tools(for Mac)
* [Vim](http://www.vim.org/) + [tpope's vim-markdown](https://github.com/tpope/vim-markdown) + [csexton's jekyll.vim](https://github.com/csexton/jekyll.vim) + [tpope's vim-fugitive](https://github.com/tpope/vim-fugitive)

  Vim is, needless to say, an editor. I recommend plugins mentioned above for writing and version controlling(you should always do that) your posts.

* [Visor](http://visor.binaryage.com/)

  You need to be familiar with Terminal in order to use [Jekyll](https://github.com/mojombo/jekyll). I'm a GUI guy as much as you are so Visor make my life a little easier. Visor is a system-wide terminal on a hot key.
  When you press your hotkey, Terminal wrapped with Visor drops down. It looks cool enough to use it more often so you can learn commands(well, you'll only need cd to move around directory and jekyll to build sites).
  
#Websites Get You Started on Jekyll
* [Official Wiki](https://github.com/mojombo/jekyll/wiki)
* [Site Point's Jekyll: Sites Made Simple](http://articles.sitepoint.com/article/jekyll-sites-made-simple) - Little bit old but useful guide.
* [Daring Fireball: Markdown Syntax Documentation](http://daringfireball.net/projects/markdown/syntax) - Using as my markdown syntax cheat sheet.
* [Official Issue](https://github.com/mojombo/jekyll/issues) - Some Issues are resolved.
* [Official Mailing list](http://groups.google.com/group/jekyll-rb) - You can ask questions. You should search your question *fitst*. 

##Recommend Plugins for Jekyll
Jekyll can be extended its capability via [plugins](https://github.com/mojombo/jekyll/wiki/Plugins). Here I'm not gonna try to collect all plugins available, but I'll list ones I use or I'll try to use.

###Currently Using

* [tatey's jekyll\_plugins](https://github.com/tatey/jekyll_plugins)

  I use LESS CSS converter and JavaScript Minifier. I couldn't figure out how to use growl one, but I'd like to try it again.

* [indirect's jekyll\_postfiles](https://github.com/indirect/jekyll-postfiles)

  A plugin adds files for each post. You can add files on post basic. You need to create a directory named after the post in \_postfiles, then you can refer to the file using {% postfile YOURFILENAME.EXTENSION %}.
  I need this to show screen shots of my theme.

###Will Look into

* [pattex's jekyll\_tagging](https://github.com/pattex/jekyll-tagging)

  According to its author, jekyll-tagging is a Jekyll plugin, to add a tag cloud and per tag pages to your Jekyll generated Website.

* [Recursive-design.com's jekyll plugins](http://recursive-design.com/projects/jekyll-plugins/)

  generate\_categories.rb and generate\_sitemap.rb look interesting.

* [blackwinter's jekyll-pagination](https://github.com/blackwinter/jekyll-pagination)

  Extend pagination generator. Not sure how this differs from native pagination since I have no idea how to use native pagination.
