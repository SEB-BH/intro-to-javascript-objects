<h1>
  <span class="headline">Intro to JavaScript Objects</span>
  <span class="subhead">Fundamentals</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to create an object and read or add a property with dot notation.

## Create an object

Start with an empty shopping cart object. Put this in `app.js`, then run `node app.js`:

```javascript
const cart = {};
console.log(cart); // {}
```

The braces `{}` make a new object. Now we'll add a single property to our cart:

```javascript
const cart = {
  storeName: 'Corner Market',
};
console.log(cart); // { storeName: 'Corner Market' }
```

Add an `items` property. Its value is an array of product names:

```javascript
const cart = {
  storeName: 'Corner Market',
  items: ['Bread', 'Milk'],
};
console.log(cart);
```

The commas separate properties. A comma after the last property is also valid. We use it so adding another line later is easy.

## Read properties with a dot

Write the name of the object, a dot, then the property name:

```javascript
console.log(cart.storeName); // Corner Market
console.log(cart.items); // [ 'Bread', 'Milk' ]
```

## A quick note on square brackets

You can read the same property with square brackets and a quoted key:

```javascript
console.log(cart['storeName']); // Corner Market
```

`cart.storeName` and `cart['storeName']` give the same result. For a key whose name you already know, the dot is usually easier to read. Later, the optional [Square Bracket Notation](../square-bracket-notation/README.md) lesson shows how brackets help when the key comes from a variable. These brackets read an **object property**; in `cart.items[0]`, brackets select an **array position**.

## 🎓 You Do

Add a `customerName` property with your name as a string. Print `cart.customerName` and run `node app.js`. Which part of `cart.customerName` is the property name?
