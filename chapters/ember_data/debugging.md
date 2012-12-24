---
layout: recipe
title: Debuggin
chapter: Ember Data
---

## Debugging checklist

Make sure you didn't specify `id` as an attribute in your model

{% highlight javascript %}
App.User = DS.Model.extend({
  // THIS IS WRONG!
  id: DS.attr("string"),

  username: DS.attr("string")
});
{% endhighlight %}

the model should look like this instead

{% highlight javascript %}
App.User = DS.Model.extend({
  username: DS.attr("string")
});
{% endhighlight %}

since Ember Data will handle the `id` automatically.
