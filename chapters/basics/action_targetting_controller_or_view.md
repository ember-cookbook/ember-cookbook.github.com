---
layout: recipe
title: Action targetting controller or view
chapter: Basics
---

## Problem

Using `{% raw %}{{action foo}}{% endraw %}` will call a `foo` method on the router by
default. But you might need to do that with a view or a controller.

## Solution

Specify a `target` for your `{% raw %}{{action}}{% endraw %}`, such as the following

{% highlight javascript %}

{% raw %}{{action foo target="controller"}}{% endraw %}
{% raw %}{{action foo target="view"}}{% endraw %}

{% endhighlight %}
