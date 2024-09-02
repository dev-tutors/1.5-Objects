### Object Methods and the `this` Keyword

In JavaScript, objects can not only store data but also perform actions through methods. Methods are simply functions that belong to an object. 

Understanding how to use methods and the `this` keyword is essential for writing dynamic and powerful JavaScript code. Let’s explore these concepts using a simple car object.

## Steps

### 1. Defining Object Methods with `this`

Let's define a car object with properties and a method. We'll include the car's `owner`, `brand`, and `year` as properties, and a method to calculate the car’s age.

#### Example Code

```javascript
const car = {
    owner: "Alice",
    brand: "Toyota",
    year: 2015,
    calculateAge: function() {
        const currentYear = new Date().getFullYear();
        return currentYear - this.year;
    }
};

console.log(`${car.owner}'s ${car.brand} is ${car.calculateAge()} years old.`);
// Outputs: "Alice's Toyota is X years old." (X depends on the current year)
```

In this example, `this.year` refers to the `year` property of the `car` object. The `calculateAge` method uses the `this` keyword to access the `year` property and calculate how old the car is.

### 2. Improving the Object with Additional Methods

But how can we improve this object so that we can have a method that tells us the car’s age automatically in a more descriptive way? 

Let's enhance our `car` object by adding a new method that automatically displays the car's age when called.

#### Updated Example Code

```javascript
const car = {
    owner: "Alice",
    brand: "Toyota",
    year: 2015,
    calculateAge: function() {
        const currentYear = new Date().getFullYear();
        return currentYear - this.year;
    },
    displayAge: function() {
        return `${this.owner}'s ${this.brand} is ${this.calculateAge()} years old.`;
    }
};

console.log(car.displayAge());
// Outputs: "Alice's Toyota is X years old." (X depends on the current year)
```

### Explanation:

- **calculateAge Method:** The `calculateAge` method uses the `this` keyword to access the `year` property and calculate how old the car is.
- **displayAge Method:** Instead of using `console.log()` outside the object, we create a method inside the object to return the message. Notice how we use the `return` keyword inside the method to return a string. To see this message, you need to call `console.log()` when you call the method, like this: `console.log(car.displayAge());`.

By structuring your code this way, your object becomes more self-contained and easier to manage, as it handles both data and how that data is presented.

## Exercises

### Exercise 1: Extend the Car Object

Building on the car object we’ve created, add the following methods:

1. **getCarDetails():** Create a method that returns a string with the car owner’s name, the brand, and the year in a sentence.
   
   **Expected Output:**
   ```javascript
   console.log(car.getCarDetails());
   // Outputs: "Alice owns a Toyota from 2015."
   ```

2. **updateOwner(newOwner):** Create a method that allows you to change the owner’s name to a new name passed as an argument.

   **Expected Output:**
   ```javascript
   car.updateOwner("Bob");
   console.log(car.owner); // Outputs: "Bob"
   ```

## Important Notes

- **The `this` Keyword:** The `this` keyword is crucial for accessing other properties of the same object within a method. It always refers to the object that is calling the method.

- **Object Methods:** Methods are functions that belong to an object. They allow you to encapsulate functionality within your objects, making your code more organized and easier to manage.

Understanding how to use methods and the `this` keyword will take your ability to work with objects to the next level. Practice these exercises to reinforce what you've learned and see how methods can make your objects more powerful and versatile.