<h1>
  <span class="headline">Intro to JavaScript Objects</span>
  <span class="subhead">Concepts</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to explain what an object, property, key, and value are.

## A shopping cart has related details

Imagine a shopping cart on a store website. We want to remember the store's name and the items in the cart. We could keep these details together in one **object**. An object is a group of related pieces of information.

```javascript
const cart = {
  storeName: 'Corner Market',
  items: ['Bread', 'Milk'],
};
```

The curly braces `{` and `}` mark the object. `cart` is the variable name we use to reach it. Each line inside is a **property**: a **key** (the label), a colon, and a **value** (the information). In `storeName: 'Corner Market'`, `storeName` is the key and `'Corner Market'` is the value. The comma separates properties. The final comma is allowed.

`'Corner Market'` is a string (text). `['Bread', 'Milk']` is an array (an ordered list). A property can hold different kinds of values, including numbers, booleans, arrays, and other objects.

> 💡 Read `cart.storeName` as “the storeName property of cart.” We will write this code in Fundamentals.

An array is useful when the order of items matters. An object is useful when we want named details about one thing. Later, we will put an array **inside** the cart object and objects **inside** that array.

