### Objective: Use Object Destructuring to Simplify Data Handling

In this lesson, you’ll learn how to use object destructuring to extract data from an object and use it in your code. Destructuring helps make your code cleaner and more concise, especially when dealing with objects that have many properties.

## Steps

### 1. Create an Object Named `product`

Start by creating an object named `product` that represents an item in a store. The object should include properties such as `name`, `price`, `category`, `stock`, and `rating`.

```javascript
const product = {
  name: 'Laptop',
  price: 1200,
  category: 'Electronics',
  stock: 35,
  rating: 4.7
};
```

### 2. Extract the Properties of the `product` Object

Next, use object destructuring to extract the properties of the `product` object into individual variables: `name`, `price`, `category`, `stock`, and `rating`.

```javascript
const { name, price, category, stock, rating } = product;
```

### 3. Use the Extracted Variables in a Statement

Now that you have the properties in separate variables, use template literals to create a statement that describes the product. Output the result with `console.log`.

```javascript
console.log(`The ${name} belongs to the ${category} category and is priced at $${price}. It has a rating of ${rating} and ${stock} units are available.`);
```

### 4. Run the Code

Run the code to view the statement in the console.

**Expected Output:**

```
The Laptop belongs to the Electronics category and is priced at $1200. It has a rating of 4.7 and 35 units are available.
```

<details>
<summary>Full Code</summary>

```javascript
const product = {
  name: 'Laptop',
  price: 1200,
  category: 'Electronics',
  stock: 35,
  rating: 4.7
};

const { name, price, category, stock, rating } = product;

console.log(`The ${name} belongs to the ${category} category and is priced at $1200. It has a rating of ${rating} and ${stock} units are available.`);
```
</details>

---

### Key Takeaways:

- **Object Destructuring:** This technique allows you to extract multiple properties from an object in a single statement, making your code more concise and easier to read.
- **Template Literals:** By using template literals (enclosed in backticks), you can easily create strings that include variables, which is especially useful for dynamic content.
  
Object destructuring is a powerful feature in JavaScript that makes working with objects more efficient. Practice using destructuring in different contexts to become more familiar with this handy tool.