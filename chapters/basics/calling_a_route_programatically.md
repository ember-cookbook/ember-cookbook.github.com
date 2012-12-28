---
layout: recipe
title: Calling a route programatically
chapter: Basics
---

## Problem

You need to transition to a different route programatically, as if you
did `{% raw %}{{action gotoUsers}}{% endraw %}`.

## Solution

Get the router instance from the application and call `send` on it with
the required transition name

{% highlight javascript %}
App.get("router").send("gotoUsers");
{% endhighlight %}

Or with a context

{% highlight javascript %}
App.get("router").send("showUser", App.currentUser);
{% endhighlight %}
