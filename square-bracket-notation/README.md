<h1>
  <span class="headline">Intro to JavaScript Objects</span>
  <span class="subhead">Square Bracket Notation</span>
</h1>

**Learning objective:** By the end of this optional lesson, students will be able to choose between dot and square bracket notation for object properties.

Use a dot when the property name is written directly in your code. Use square brackets when the name comes from a variable:

```javascript
const cart = { storeName: 'Corner Market', items: ['Bread', 'Milk'] };
console.log(cart.storeName); // Corner Market
console.log(cart['storeName']); // Corner Market

const chosenProperty = 'storeName';
console.log(cart[chosenProperty]); // Corner Market
console.log(cart.chosenProperty); // undefined
```

`cart[chosenProperty]` uses the variable's value (`'storeName'`) as the key. `cart.chosenProperty` searches for a key literally named `chosenProperty`.

## Count product names

We can use that idea to count names from a cart. Start with a small list of known products:

```javascript
const cart = { items: ['Bread', 'Milk', 'Bread'] };
const counts = { Bread: 0, Milk: 0 };

for (const item of cart.items) {
  counts[item] = counts[item] + 1;
}

console.log(counts); // { Bread: 2, Milk: 1 }
```

On each trip through the loop, `item` is the current string. When it is `'Bread'`, `counts[item]` means `counts['Bread']`. The same code works for `'Milk'`. The starting keys in `counts` match the products in this small example.

We can add or delete a property with brackets too:

```javascript
const key = 'Apples';
counts[key] = 0;
console.log(counts.Apples); // 0
delete counts[key];
```

> 💡 `cart.items[0]` uses brackets for an **array index**. `counts[item]` uses brackets for an **object key**. The shapes look alike, but the values inside the brackets do different jobs.

## 🎓 You Do

Change `cart.items` to `['Milk', 'Milk', 'Bread']` and predict `counts` before running the code. Then try `const chosenProperty = 'items'` in the first example.
