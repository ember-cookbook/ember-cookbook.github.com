---
layout: recipe
title: Getting an instance of a controller in the console
chapter: Basics
---

## Problem

With the old router, it was possible to simply do
`App.router.get("homeController")` to get to the controller instance,
but this syntax has been deprecated in the new router.

## Solution

Use `App.container.lookup` method.

{% highlight javascript %}
// accessing HomeController instance
App.container.lookup("controller:home");
// accessing the router
App.container.lookup("router:main");
{% endhighlight %}
