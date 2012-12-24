---
layout: recipe
title: Text field
chapter: Ember Data
---

## Problem

You need to create a two way data binding for a text field

## Solution

Use `Ember.TextField` class either directly, or by subclassing

{% highlight javascript %}
App.burger = Em.Object.create({
  name: null
});
{% endhighlight %}

{% highlight html %}
{% raw %}{{view Ember.TextField valueBinding="App.burger.name"}}{% endraw %}
<label>value of {% raw %}{{App.burger.name}}{% endraw %}</label>
{% endhighlight %}

[Here's a JSFiddle](http://jsfiddle.net/darthdeus/qgpK8/1/)
