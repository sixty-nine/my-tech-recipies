# Backbone Models Recipies

### Move a model after another model in the collection
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
