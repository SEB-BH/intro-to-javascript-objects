<h1>
  <span class="headline">Intro to JavaScript Objects</span>
  <span class="subhead">Data Structures</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to read and update an object inside an array inside another object.

So far, the cart's `items` array has stored product names as strings. A store may also need a price and quantity for each product. We can represent **one product** with an object:

```javascript
const bread = {
  name: 'Bread',
  price: 2,
  quantity: 1,
};
```

`price` and `quantity` are numbers. Now each entry in the cart's array can be a product object. Replace your previous `cart` code with this complete example:

```javascript
const cart = {
  storeName: 'Corner Market',
  items: [
    { name: 'Bread', price: 2, quantity: 1 },
    { name: 'Milk', price: 3, quantity: 2 },
  ],
  addItem(item) {
    cart.items.push(item);
  },
  itemCount() {
    return cart.items.length;
  },
};
```

Read from left to right: `cart` is an object; `.items` is its array; `[0]` selects the **first** entry (array indexes start at zero); `.name` reads a property of that product object.

```javascript
console.log(cart.items[0].name); // Bread
console.log(cart.items[1].price); // 3
console.log(cart.itemCount()); // 2 products (not total quantity)
```

The methods from the previous lesson still work. `addItem(item)` accepts an object just as it accepted a string:

```javascript
cart.addItem({ name: 'Apples', price: 4, quantity: 1 });
console.log(cart.items[2].name); // Apples
console.log(cart.itemCount()); // 3
```

## 🎓 You Do

Change Milk's `quantity` from `2` to `3` using the assignment operator `=`. 

Print it to confirm. Then print the name of the first product. 

