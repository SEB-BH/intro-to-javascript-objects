<h1>
  <span class="headline">Intro to JavaScript Objects</span>
  <span class="subhead">Manipulation</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to change and delete properties of an object.

## Add or change a value

Let's add a discount code to our cart object.

```javascript
const cart = {
  storeName: 'Corner Market',
  items: ['Bread', 'Milk'],
  discountCode: 'WELCOME',
};

cart.discountCode = 'SAVE10';
console.log(cart.discountCode); // SAVE10
```

The key `discountCode` already exists, so `=` changes its value. If the key does not exist, `=` creates it instead:

```javascript
cart.customerName = 'Sam';
console.log(cart.customerName); // Sam
```

## Delete a property

Suppose we need to remove the discount code. `delete` removes the whole property, including its key:

```javascript
delete cart.discountCode;
console.log(cart); // { storeName: 'Corner Market', items: [ 'Bread', 'Milk' ], customerName: 'Sam' }
console.log(cart.discountCode); // undefined
```

`undefined` here means that property is no longer there. It does not remove the whole cart.

## 🎓 You Do

Add a `deliveryNote` property with a short string. Print it, delete it, then print `cart.deliveryNote` again. Predict what the second print will show before running the file.
