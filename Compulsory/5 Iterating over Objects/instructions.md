### Iterating Over Objects

Now that you’ve learned how to create and interact with objects in JavaScript, it’s time to explore how to iterate over them. 

Iterating over an object allows you to access each key-value pair, which is particularly useful when you need to process or display all the properties of an object.

## Steps

### 1. Understanding the `for...in` Loop

In JavaScript, the `for...in` loop is used to iterate over the keys (or properties) of an object. Unlike arrays, where you iterate over elements by their index, objects are iterated over by their property names.

#### Example Code

```javascript
const gameCharacter = {
    name: "Mario",
    lives: 3,
    level: 5,
    powerUp: "Fire Flower"
};

for (let key in gameCharacter) {
    console.log(`${key}: ${gameCharacter[key]}`);
}

// Outputs:
// name: Mario
// lives: 3
// level: 5
// powerUp: Fire Flower
```

### Explanation:

- **`for...in` Loop:** The `for...in` loop iterates over each property in the `gameCharacter` object. The `key` variable stores the name of the current property, and `gameCharacter[key]` accesses the value associated with that property.

- **Dynamic Access:** Notice how we use bracket notation (`gameCharacter[key]`) to dynamically access the value of each property. This is necessary because `key` is a variable and not a static property name.

### 2. Practical Use Case: Displaying Object Information

Iterating over objects is particularly useful when you need to display or process all the properties of an object, such as showing character stats in a game or details about a movie.

#### Example Code

```javascript
const movie = {
    title: "Inception",
    director: "Christopher Nolan",
    year: 2010,
    genre: "Science Fiction"
};

for (let property in movie) {
    console.log(`${property}: ${movie[property]}`);
}

// Outputs:
// title: Inception
// director: Christopher Nolan
// year: 2010
// genre: Science Fiction
```

Here, the `for...in` loop is used to print out all the details of the `movie` object, showing how iterating over an object can easily display its full set of properties and values.

## Exercises

### Exercise 1: Favorite Game Character

Create an object called `character` with the following properties: `name`, `lives`, `level`, and `ability`. Then:

1. Use a `for...in` loop to iterate over the `character` object.
2. Print out each property and its corresponding value.

**Expected Output:**

```javascript
// Example output
// name: Pikachu
// hp: 95
// level: 20
// ability: Thundershock
```

### Exercise 2: Iterating Over Movie Details

Given the `movie` object from the example:

1. Add a new property `rating` to the `movie` object.
2. Use a `for...in` loop to print out all the properties and values of the `movie` object, including the new `rating` property.

**Expected Output:**

```javascript
// Example output
// title: Barbie
// director: Greta Gerwig
// year: 2023
// genre: Adventure/Comedy
// rating: PG-13
```

### Exercise 3: Dynamic Property Access in a Movie Object

Create an object called `film` with properties `title`, `director`, `releaseYear`, and `genre`. Then:

1. Use a `for...in` loop to dynamically access and print out each property.
2. After printing, check if any property is `releaseYear`. If it is, increment the year by 1.

**Expected Output:**

```javascript
// Example output
// title: The Matrix
// director: The Wachowskis
// releaseYear: 2000
// genre: Action

// Note: The releaseYear should now be incremented by 1
```

---

## Important Notes

- **Use Cases:** Iterating over objects is common when you need to handle configurations, display details, or process multiple properties in one go.