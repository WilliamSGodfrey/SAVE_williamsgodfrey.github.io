---
layout:     post
title:      A new look via Jekyll
date:       2016-02-01 09:06:19
excerpt:    williamsgodfrey.com is now running on Jekyll, a parsing engine bundled as a ruby gem used to build static websites from dynamic components.
categories: jekyll pixyll
---

I recently migrated this website from [Wordpress](https://wordpress.org/) to [Github Pages](https://pages.github.com/) using [Jekyll](https://jekyllrb.com/) and [Pixyll](https://github.com/johnotander/pixyll). Wordpress was becoming annoying, with its constant nagging about updates and awful WYSIWYG editor on the backend. I felt like I had to very carefully work around the awfully generated HTML in order to accomplish the simplest things. And it wasn't like I needed all that functionality anyway. This site is used very little. It was time to simplify.

### Why Jekyll?

Jekyll is a parsing engine bundled as a ruby gem used to build static websites from dynamic components such as templates, partials, liquid code, markdown, etc. Jekyll is known as "a simple, blog aware, static site generator." In other words, the website is now simply a set of static files. Posts are written in [Markdown](https://en.wikipedia.org/wiki/Markdown) and, since I'm using Github Pages for hosting, pushed to the site.

###Still a work in progress

Jekyll prides itself as being the way to ["blog like a Hacker"](http://tom.preston-werner.com/2008/11/17/blogging-like-a-hacker.html). As a result, there is a fair amount of work still to be done here with respect to fully migrating the old site and ensuring an equal level of functionality.

Still to be done:

  1. Figure out how to display the normalized beer ratings on the review posts.
  2. Figure out how to reduce post title font size on index page without messing up other stuff.
  3. Clean up all the old posts migrated from Wordpress via the wordpress2jekyll script.
  4. Change wording in the contact form.
