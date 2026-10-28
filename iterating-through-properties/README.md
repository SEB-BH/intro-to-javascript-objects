<h1>
  <span class="headline">Intro to JavaScript Objects</span>
  <span class="subhead">Iterating Through Properties</span>
</h1>

**Learning objective:** By the end of this optional lesson, students will be able to visit the keys and values of an object.

Suppose one product in the cart has several named details:

```javascript
const product = {
  name: 'Bread',
  price: 2,
  quantity: 1,
};
```

If we want to look at every detail, `Object.keys(product)` gives us an array of its keys:

```javascript
console.log(Object.keys(product)); // [ 'name', 'price', 'quantity' ]

for (const key of Object.keys(product)) {
  console.log(key, product[key]);
}
// name Bread
// price 2
// quantity 1
```

`key` changes with each trip through the loop. `product[key]` reads the property whose name is stored in that variable. `product.key` would look for a property literally named `key`.

`Object.values(product)` gives the values; `Object.entries(product)` gives an array of `[key, value]` pairs. Another option is `for...in`:

```javascript
for (const key in product) {
  if (Object.hasOwn(product, key)) {
    console.log(key, product[key]);
  }
}
```

The `Object.hasOwn` check keeps `for...in` to properties on this product, excluding any inherited ones. Use these loops when the property names may vary; when you know a key, `product.name` is simpler.

## 🎓 You Do

Add `inStock: true` to `product` and rerun the first loop. What extra line appears?
