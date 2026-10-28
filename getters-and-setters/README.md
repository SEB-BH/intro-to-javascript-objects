<h1>
  <span class="headline">Intro to JavaScript Objects</span>
  <span class="subhead">Getters and Setters</span>
</h1>

**Learning objective:** By the end of this optional lesson, students will be able to read a getter and assign to a setter.

A **getter** looks like a property when you read it, but runs code to produce its value. A **setter** looks like a property when you assign to it, but runs code with the new value.

```javascript
const cart = {
  items: ['Bread', 'Milk'],
  note: '',
  get itemCount() {
    return this.items.length;
  },
  set deliveryNote(value) {
    this.note = value.trim();
  },
};

console.log(cart.itemCount); // 2 (no parentheses)
cart.deliveryNote = '  Leave at the door  ';
console.log(cart.note); // Leave at the door
```

`get itemCount()` returns the array length. `set deliveryNote(value)` receives the assigned string and stores it in `note`. `.trim()` removes spaces at the start and end. We store the result under a different property name (`note`) so the setter does not repeatedly call itself.

> 💡 Earlier, `itemCount()` was a regular method and needed parentheses. Here, `itemCount` is a getter and does not.

## 🎓 You Do

Add `'Apples'` to `cart.items`, then print `cart.itemCount` again. Predict the value first.
