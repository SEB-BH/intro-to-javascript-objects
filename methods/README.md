<h1>
  <span class="headline">Intro to JavaScript Objects</span>
  <span class="subhead">Methods</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to define and call a method on an object.

A **method** is a function stored on an object. A function is a set of instructions we can run. A cart can have a method to add an item.

Replace your earlier cart code with this complete example:

```javascript
const cart = {
  storeName: 'Corner Market',
  items: ['Bread', 'Milk'],
  addItem(item) {
    cart.items.push(item);
  },
};

cart.addItem('Apples');
console.log(cart.items); // [ 'Bread', 'Milk', 'Apples' ]
```

`addItem(item) { ... }` defines the method. `item` is a **parameter**: a name for the value given to the method. In `cart.addItem('Apples')`, `'Apples'` is that value. The parentheses `()` call the method. `.push(item)` adds the value to the end of the array.

`addItem()` belongs to `cart`, so calling `addItem('Apples')` by itself will cause an error.

## Add a method that returns a value

Add a comma after the `addItem` method's closing brace, then add `itemCount`:

```javascript
const cart = {
  storeName: 'Corner Market',
  items: ['Bread', 'Milk'],
  addItem(item) {
    cart.items.push(item);
  },
  itemCount() {
    return cart.items.length;
  },
};

console.log(cart.itemCount()); // 2
cart.addItem('Apples');
console.log(cart.itemCount()); // 3
```

`.length` is the number of entries in the array. `return` sends that number back to the code that called the method. Later, `item` can be a product object instead of a string; the method still adds it to the array.

## 🎓 You Do

Call `cart.addItem('Rice')` and predict the count before printing `cart.itemCount()`. 

Then add a `removeLastItem()` method using and check the count again. 

Reminder: `.pop()` removes the last array entry.
