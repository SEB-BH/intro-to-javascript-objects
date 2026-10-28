<h1>
  <span class="headline">Intro to JavaScript Objects</span>
  <span class="subhead">Property Shorthand Syntax</span>
</h1>

**Learning objective:** By the end of this optional lesson, students will be able to create object properties from variables with matching names.

Imagine you already have separate variables describing a product for your cart:

```javascript
const name = 'Bread';
const price = 2;
const quantity = 1;

const product = {
  name: name,
  price: price,
  quantity: quantity,
};
console.log(product); // { name: 'Bread', price: 2, quantity: 1 }
```

When a variable and the key use the **same spelling**, JavaScript lets you write each name once. Replace the `product` declaration above with:

```javascript
const product = { name, price, quantity };
console.log(product); // { name: 'Bread', price: 2, quantity: 1 }
```

`{ name }` is shorthand for `{ name: name }`. This only works when the variable already exists.

## 🎓 You Do

Make a `category` variable containing `'Bakery'` and include it in `product` using shorthand. Print `product.category`.
