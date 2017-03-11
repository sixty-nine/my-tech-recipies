# Backbone Models Recipies

### Move collection model at a specific position
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