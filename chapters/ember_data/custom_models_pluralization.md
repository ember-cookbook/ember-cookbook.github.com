---
layout: recipe
title: Custom Models Pluralization
chapter: Ember Data
---

## Problem

When accessing a remote API (e.g RESTAdapter), Ember.js uses the model name
plural, which means that the `Post` model would automatically map to `/posts`.

Sometimes, you need a customized plural. You may want the Person model to map
to `/people` instead of `/persons`.

## Solution

Under your adapter definition, add the `plurals` containing a hash with
whatever model names you want to customize:

    App.store = DS.Store.create({
      adapter: DS.RESTAdapter.create({
        plurals: {
          'person': 'people'
        }
      })
    });

Although the model name is `Person`, use `person` as the hash key.
