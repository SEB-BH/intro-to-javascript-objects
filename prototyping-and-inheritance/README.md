<h1>
  <span class="headline">Intro to JavaScript Objects</span>
  <span class="subhead">Prototyping and Inheritance</span>
</h1>

**Learning objective:** By the end of this optional lesson, students will be able to explain where a built-in array method comes from.

We used `.push()` on `cart.items`, even though we never wrote a `push` method ourselves:

```javascript
const cart = { items: ['Bread'] };
cart.items.push('Milk');
console.log(cart.items); // [ 'Bread', 'Milk' ]
```

JavaScript arrays share built-in methods through their **prototype**. When we ask the array for `push`, JavaScript can find it on `Array.prototype`. This is called **inheritance**. We can inspect that connection:

```javascript
console.log(Object.getPrototypeOf(cart.items) === Array.prototype); // true
```

Our own `cart.addItem()` method, when we define one, belongs to the cart object itself. The built-in `.push()` is available to arrays generally. We do not need to write it for every new array.

> 💡 Prototypes are an advanced topic. For now, remember that JavaScript provides shared methods for arrays and other kinds of objects.

## 🎓 You Do

Try `cart.items.pop()`, then print `cart.items`. Did you write a `pop` method yourself? Where does the array find it?
