---
layout: recipe
title: Bind attribute
chapter: Basics
---

## Problem

You need to data-bind a tag attribute, however `<img src="{% raw %}{{foo}}{% endraw %}">` doesn't work.

## Solution

The reason why the above doesn't work is because `{% raw %}{{foo}}{% endraw %}` will insert metamorph tags, which results in the following

    <script id="metamorph-0-start" type="text/x-placeholder"></script>
    http://example.com/foo.png
    <script id="metamorph-0-end" type="text/x-placeholder"></script>

What you want to do instead is use `{% raw %}{{bindAttr foo}}{% endraw %}`,
which outputs the following

    <img src="http://example.com/foo.png" data-bindattr-1="1">

