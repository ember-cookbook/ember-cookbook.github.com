---
layout: recipe
title: Select field
chapter: Ember Data
---

## Problem

You need to give the user option to select from multiple choices.

## Solution

Use `Ember.Select`

{% highlight javascript %}
App.burgers = ["double cheesburger", "mini-burger", "triple bacon
cheesburger"];

App.burger = Em.Object.create({
  name: null
});
{% endhighlight %}

{% highlight html %}
{% raw %}{{view Ember.Select valueBinding="App.burger.name" contentBinding="App.burgers"}}{% endraw %}
<label>value of {% raw %}{{App.burger.name}}{% endraw %}</label>
{% endhighlight %}

[Here's a JSFiddle](http://jsfiddle.net/darthdeus/qgpK8/5/)


### Multiple choice

You can also allow the user to select multiple values from the select

{% highlight javascript %}
App.burgers = ["double cheesburger", "mini-burger", "triple bacon
cheesburger"];

App.burger = Em.Object.create({
    names: []
});
{% endhighlight %}

{% highlight html %}
<label>
  Pick your burger:
  {% raw %}{{view Ember.Select valueBinding="App.burger.names" contentBinding="App.burgers" multiple="true"}}{% endraw %}
</label>

<p>You picked: "{% raw %}{{#each burger in App.burger.names}}{{burger}}{{/each}}{% endraw %}"</p>
{% endhighlight %}

[Here's a JSFiddle](http://jsfiddle.net/darthdeus/qgpK8/6/)
