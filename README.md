# expansion-emit

```js
import expansionEmit from 'expansion-emit';
import expand from 'expand-expansion';

var obj = expand(null, expansionEmit, {
    value: null,
});

obj.on('update', function(value) {
    console.log('update', value);
});

function set(value) {
    obj.value = value;
    obj.emit('update', obj.value);
};

set(777);

```