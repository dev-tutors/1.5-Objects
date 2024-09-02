### Calculate Total Product

In this lesson, you’ll learn how to calculate the total cost of products in a shopping cart. This exercise will involve working with both arrays and objects, where each object represents a product in the cart. 

You’ll use a loop to iterate through the array of products and calculate the total cost.

## Steps

### 1. Create an Array of Grocery Products

Start by creating an array named `groceryCart`. Each element in the array should be an object representing a product, with properties such as `name`, `price`, and `quantity`.

```javascript
const groceryCart = [
  { name: 'Milk', price: 2.5, quantity: 2 },
  { name: 'Bread', price: 1.5, quantity: 1 },
  { name: 'Eggs', price: 3.0, quantity: 1 },
  { name: 'Cheese', price: 4.0, quantity: 3 }
];
```

### 2. Initialize a Variable to Store the Total Cost

Before iterating through the array, initialize a variable named `totalCost` to store the cumulative cost of the products.

```javascript
let totalCost = 0;
```

### 3. Iterate Through the Array and Calculate the Total Cost

Use a `for` loop to iterate through the `groceryCart` array. For each product, multiply the `price` by the `quantity` to get the total cost for that product, then add it to `totalCost`.

```javascript
for (let i = 0; i < groceryCart.length; i++) {
  totalCost += groceryCart[i].price * groceryCart[i].quantity;
}
```

### 4. Output the Total Cost

After the loop, use `console.log()` to display the total cost of the products in the cart.

```javascript
console.log(`The total cost of the products in the cart is $${totalCost.toFixed(2)}.`);
```

### Expected Output

```
The total cost of the products in the cart is $18.00.
```

<details>
<summary>Full Code</summary>

```javascript
const groceryCart = [
  { name: 'Milk', price: 2.5, quantity: 2 },
  { name: 'Bread', price: 1.5, quantity: 1 },
  { name: 'Eggs', price: 3.0, quantity: 1 },
  { name: 'Cheese', price: 4.0, quantity: 3 }
];

let totalCost = 0;

for (let i = 0; i < groceryCart.length; i++) {
  totalCost += groceryCart[i].price * groceryCart[i].quantity;
}

console.log(`The total cost of the products in the cart is $${totalCost.toFixed(2)}.`);
```

</details>

---

### Key Takeaways:

- **Combining Arrays and Objects:** This lesson demonstrates how to combine arrays and objects to solve real-world problems like calculating the total cost of items in a shopping cart.
- **Looping Through Arrays:** Iterating over an array of objects allows you to perform calculations on each object’s properties, making it easy to handle complex data structures.

Understanding how to work with arrays and objects together is essential for solving many practical coding problems. Practice with different scenarios to deepen your understanding and enhance your coding skills.