<h1>
  <span class="headline">Intro to JavaScript Objects</span>
  <span class="subhead">How Variables Reference Objects</span>
</h1>

**Learning objective:** By the end of this optional lesson, students will be able to predict what happens when two variables refer to the same object.

A variable holding an object refers to that object. Assigning that variable to another variable gives both names access to the **same** object:

```javascript
const cart = { items: ['Bread'] };
const sharedCart = cart;

sharedCart.items.push('Milk');
console.log(cart.items); // [ 'Bread', 'Milk' ]
console.log(sharedCart === cart); // true
```

Both names lead to the same cart. `const` prevents reassigning the variable name; it does not freeze the object's properties or its array.

Creating a second cart with the same contents creates a different object:

```javascript
const otherCart = { items: ['Bread', 'Milk'] };
console.log(otherCart === cart); // false
```

`===` compares whether these object variables refer to the **same object**, rather than comparing every item inside them. Arrays behave the same way.

## 🎓 You Do

Before running it, predict what `cart.items` contains after `sharedCart.items.pop()`. Then run the code to check.
