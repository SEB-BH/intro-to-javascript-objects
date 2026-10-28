<h1>
  <span class="headline">Intro to JavaScript Objects</span>
  <span class="subhead"><code>this</code></span>
</h1>

**Learning objective:** By the end of this optional lesson, students will be able to use `this` inside a method called on an object.

In our earlier method, we wrote `cart.items.push(item)`. Inside a regular object method, `this` can refer to the object **before the dot** in the call. When we call `cart.addItem(...)`, `this` inside `addItem` is `cart`.

```javascript
const cart = {
  items: ['Bread', 'Milk'],
  addItem(item) {
    this.items.push(item);
  },
  itemCount() {
    return this.items.length;
  },
};

cart.addItem('Apples');
console.log(cart.itemCount()); // 3
```

`this.items` means “the items of the object that called this method.” It is useful if we later use the same method with another cart. For now, call these methods as `cart.addItem(...)` and `cart.itemCount()` so the object before the dot is clear. We use regular method syntax here; arrow functions handle `this` differently.

## 🎓 You Do

Add `removeLastItem() { this.items.pop(); }` to the object. Call it as `cart.removeLastItem()` and print `cart.itemCount()`.
