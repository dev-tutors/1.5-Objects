### Accessing and Modifying Object Properties

Imagine you're building a personal organizer to keep track of your daily tasks, favorite books, or even your contacts. Each item you store has various details—like a task's due date, a book's author, or a contact's phone number. In JavaScript, we use objects to store and manage all this related information together. 

Let's dive in and learn how to access and modify these properties, making your code as organized and dynamic as your life! 💪

## Steps

### 1. Accessing Object Properties

You can access the properties of an object using **dot notation** or **bracket notation**. 

- **Dot Notation** is the most straightforward and commonly used method.
  
  ```javascript
  const person = {
      name: "Alice",
      age: 28,
      occupation: "Engineer"
  };

  console.log(person.name); // Outputs: "Alice"
  console.log(person.age);  // Outputs: 28
  ```

- **Bracket Notation** is useful when you need to access a property dynamically (e.g., using a variable) or if the property name contains spaces or special characters.

  ```javascript
  console.log(person["occupation"]);  // Outputs: "Engineer"

  const key = "age";
  console.log(person[key]);  // Outputs: 28
  ```

### 2. Modifying Object Properties

Modifying properties in an object is as simple as accessing them. You can reassign a new value to a property using either dot notation or bracket notation.

### Example Code

```javascript
person.name = "Bob";  // Using dot notation
console.log(person.name); // Outputs: "Bob"

person["age"] = 30;  // Using bracket notation
console.log(person.age);  // Outputs: 30
```

In this example, we’ve changed the `name` from "Alice" to "Bob" and the `age` from 28 to 30.

### 3. Adding New Properties

You can also add new properties to an existing object using the same notations. If the property doesn’t exist, it will be created.

### Example Code

```javascript
person.email = "bob@example.com";  // Adding a new property with dot notation
console.log(person.email);  // Outputs: "bob@example.com"

person["hobby"] = "Photography";  // Adding a new property with bracket notation
console.log(person.hobby);  // Outputs: "Photography"
```

---

## Exercises

### Exercise 1: Personal Info Update

Create an object called `student` with the following properties: `name`, `age`, and `grade`. Then, do the following:

1. Access and print each property using dot notation.
2. Change the `grade` to a new value using bracket notation.
3. Add a new property `email` to the `student` object.
4. Print the updated object.

**Expected Output:**

```javascript
// Example output
console.log(student.name); // Outputs the student's name
console.log(student.age);  // Outputs the student's age
console.log(student.grade);  // Outputs the updated grade
console.log(student.email);  // Outputs the new email property
```

### Exercise 2: Car Details

Create an object called `car` with the following properties: `make`, `model`, and `year`. Then:

1. Access and print the `make` and `model` using bracket notation.
2. Update the `year` to the current year using dot notation.
3. Add a new property `color` and set it to your favorite color.
4. Print the updated `car` object.

**Expected Output:**

```javascript
// Example output
console.log(car.make);  // Outputs the car's make
console.log(car["model"]);  // Outputs the car's model
console.log(car.year);  // Outputs the updated year
console.log(car.color);  // Outputs the new color property
```

### Exercise 3: Dynamic Property Access

Create an object `book` with properties `title`, `author`, and `year`. Then:

1. Use a variable to dynamically access and print the `title` property.
2. Modify the `author` property using bracket notation.
3. Add a `genre` property and set it to a genre of your choice.
4. Print the updated `book` object.

**Expected Output:**

```javascript
// Example output
let key = "title";
console.log(book[key]);  // Outputs the book's title

book["author"] = "New Author";  // Updates the author
console.log(book.author);  // Outputs the updated author

book.genre = "Fiction";  // Adds a new genre property
console.log(book.genre);  // Outputs the new genre
```

## Important Notes

- **Dot Notation vs. Bracket Notation:** Use dot notation for most cases, as it’s simpler and more readable. Use bracket notation when you need to dynamically access properties or when property names contain spaces, special characters, or start with a number.
  
- **Adding New Properties:** You can add new properties to an object at any time, which makes objects flexible and easy to extend.

- **Mutability:** Objects in JavaScript are mutable, meaning you can change their properties at any time.