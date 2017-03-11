# Backbone Models Recipies

### Move a model in the collection

You want to move `model1` after `model2` in a collection.

```js
Backbone.Collection.extend({
    // ...
    moveModelAfter : function(model1, model2) {
        this.remove(model1);
        this.add(model1, { at: this.indexOf(model2) + 1 });
    }
    // ...
});
```

Source: [`http://stackoverflow.com/a/18365468`](http://stackoverflow.com/a/18365468)

### Swap two models in a collection

You want to swap two models of a collection given by their indexes in the collection.

```js
Backbone.Collection.extend({
    // ...
    swapItems : function(index1, index2) {
        this.models[index1] = this.models.splice(index2, 1, this.models[index1])[0];
    }
    // ...
});
```

Source: [`http://stackoverflow.com/a/10987580`](http://stackoverflow.com/a/10987580)
