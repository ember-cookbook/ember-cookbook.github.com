---
layout: recipe
title: Observing attribute change
chapter: Basics
---

## Problem

Sometimes you need to be notified when an attribute changes it's value.
A simple way to do that is by using **observers**.

## Solution

{% highlight javascript %}
App.SearchBox = Ember.TextField.extend({

  valueChanged: function () {
    console.log("search query changed to " + this.get("value"));
  }.observes("value")

});
{% endhighlight %}

[A demo of this can be found
here](http://jsfiddle.net/darthdeus/6p6XJ/243/)
