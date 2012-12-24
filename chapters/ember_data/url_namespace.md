---
layout: recipe
title: URL Namespace
chapter: Ember Data
---

## Problem

When accessing a remote API (e.g RESTAdapter), Ember.js will use the URL's root,
which means that the `Post` model would automatically map to `/posts`.

Sometimes, you need a customized URL namespace. You may want all the app's URL
routes to map to `/superadmin`, for instance. So, instead of `/persons`, Ember.js
would hit `/superadmin/persons` automatically.

## Solution

Under your REST adapter definition, add the `namespace` key like the following:

    App.store = DS.Store.create({
      adapter: DS.RESTAdapter.create({
        namespace: 'superadmin'
      })
    });

From now on, every call to the server will preppend `/superadmin` in the URL.
