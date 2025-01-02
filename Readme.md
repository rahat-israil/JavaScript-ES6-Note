## Six JS Fundamentals Must Know

### 1. How to Declare a Variable using “ let & Const “

### `let`

- `let` দিয়ে একটি ভেরিয়েবল ডিক্লেয়ার করা যায়, যা শুধুমাত্র তার ব্লকের (যেমনঃ ফাংশন বা লুপ) ভিতরে অ্যাক্সেস করা যায়।
- `let` দিয়ে ডিক্লেয়ার করা ভেরিয়েবলের মান পরবর্তীতে পরিবর্তন করা যায়।

```jsx
let name = "Ali";
name = "Hasan"; // মান পরিবর্তন করা যাবে
console.log(name); // আউটপুট: Hasan
```

### `const`

- `const` দিয়ে ডিক্লেয়ার করা ভেরিয়েবলের মান পরিবর্তন করা যায় না। এটি নির্দিষ্ট একটি মান ধরে রাখে।
- `const` ডিক্লেয়ার করার সময়ই ভেরিয়েবলের মান দিতে হবে।

```jsx
const age = 20;
age = 25; // এরর: কনস্ট্যান্ট ভেরিয়েবলে মান পরিবর্তন করা যাবে না
console.log(age); // আউটপুট: 20
```

### 2. Six Basic Conditions & Multiple Conditions

- In JavaScript, there are six basic conditions used to compare values:
1. **`>`** - বড় কিনা চেক করতে
2. **`<`** - ছোট কিনা চেক করতে
3. **`===`** - সমান কিনা চেক করতে (টাইপসহ সমান হতে হবে)
4. **`!==`** - সমান নয় কিনা চেক করতে (টাইপসহ ভিন্ন হতে হবে)
5. **`<=`** - ছোট বা সমান কিনা চেক করতে
6. **`>=`** - বড় বা সমান কিনা চেক করতে

```jsx
let a = 10;
let b = 20;

console.log(a > b);  // false, কারণ ১০ বড় নয় ২০ থেকে
console.log(a < b);  // true, কারণ ১০ ছোট ২০ থেকে
console.log(a === 10);  // true, কারণ a এর মান ১০
console.log(a !== b);  // true, কারণ a এর মান b এর সমান নয়
console.log(a <= 10);  // true, কারণ a এর মান ১০ এর সমান
console.log(b >= 15);  // true, কারণ b এর মান ১৫ এর বড়
```

- **`&&` (এন্ড অপারেটর)**: দুইটি শর্তই সত্য হতে হবে।

```jsx
let age = 25;
let isStudent = true;

if (age >= 18 && isStudent) {
    console.log("You are an adult and a student.");
} else {
    console.log("Condition not met.");
}
// Output: "You are an adult and a student." 
//          because both age >= 18 and isStudent are true.
```

- **`||` (অর অপারেটর)**: যেকোনো একটি শর্ত সত্য হলেই সত্য হবে।

```jsx
let age = 16;
let hasPermission = true;

if (age >= 18 || hasPermission) {
    console.log("You are allowed.");
} else {
    console.log("You are not allowed.");
}
// Output: "You are allowed." because hasPermission is true.
```

### 3. Array Declare

- JavaScript-এ একটি অ্যারে ডিক্লেয়ার করতে `[]` ব্র্যাকেট ব্যবহার করা হয়। ব্র্যাকেটের ভিতরে বিভিন্ন মান (elements) কমা দিয়ে আলাদা করে লিখতে হয়।

```jsx
let fruits = ["apple", "banana", "orange"];
let numbers = [10, 20, 30, 40, 50]
```

### Index

Each item in an array has an index (position) that starts from `0`. So, in the `fruits` array:

- `"apple"` is at index `0`
- `"banana"` is at index `1`
- `"orange"` is at index `2`

To access an element by its index:

```jsx
console.log(fruits[1]); // Output: "banana"

fruits[1] = "mango";  // Set the value at index 1
console.log(fruits); // Output: ["apple", "mango", "orange"]
```

### Length

The `length` property gives the total number of elements in the array.

```jsx
console.log(fruits.length); // Output: 3
```

### `push()`

The `push()` method adds a new element to the end of an array.

```jsx
fruits.push("grape");
console.log(fruits); // Output: ["apple", "banana", "orange", "grape"]
```

### `pop()`

The `pop()` method removes the last element from the array.

```jsx
fruits.pop();
console.log(fruits); // Output: ["apple", "banana", "orange"]
```

### Summary

```jsx
let fruits = ["apple", "banana", "orange"]; // Declaring an array

console.log(fruits[1]); // Accessing element by index - Output: "banana"

console.log(fruits.length); // Checking length - Output: 3

fruits.push("grape"); // Adding an element - Output: ["apple", "banana", "orange", "grape"]
fruits.pop(); // Removing the last element - Output: ["apple", "banana", "orange"]
```

### 4. for Loop

- `for` লুপ কোডের একটি অংশ বারবার চালাতে ব্যবহৃত হয়। এটি সাধারণত কোনো নির্দিষ্ট সংখ্যক বার বা অ্যারের প্রতিটি আইটেমে পুনরাবৃত্তি করতে ব্যবহৃত হয়।

```jsx
for (let i = 1; i <= 5; i++) {
    console.log(i);
}
// আউটপুট: 1, 2, 3, 4, 5
```

```jsx
let fruits = ["apple", "banana", "orange"];

for (let i = 0; i < fruits.length; i++) {
    console.log(fruits[i]);
}
// আউটপুট: "apple", "banana", "orange"
```

### 5. Function

- A **function** is a reusable block of code designed to perform a particular task. Functions help make code more organized, readable, and easier to maintain.

```jsx
function multiply(num1, num2) {
    const result = num1 * num2;
    return result;
}

const output = multiply(35, 78);
console.log(output);
```

```jsx
function greet(name) {
    console.log("Hello, " + name);
}

greet("Alice"); // Output: "Hello, Alice"
```

### 6. Object

- In JavaScript, an **object** is a collection of **key-value pairs** used to store related data and functions (known as properties and methods). Objects allow you to group related information together.

**Syntax**

```jsx
let objectName = {
    key1: value1,
    key2: value2
};
```

- **objectName**: The name you give to the object.
- **key**: The property name.
- **value**: The data associated with the property. It can be a string, number, array, another object, or even a function.

```jsx
const person = {
    name: "John",
    age: 30,
    city: "New York"
};
```

**3 Way to access Property** 

```jsx
console.log(person.name); // Output: "John"
console.log(person["age"]); // Output: 30

const cityName = "city"
console.log(person[cityName])  // Output: "New York"
```

## Template String  ( `   ` )

- JavaScript-এ টেমপ্লেট স্ট্রিংস বা টেমপ্লেট লিটারালস স্ট্রিং তৈরি করার একটি সহজ উপায়। এটি ভেরিয়েবল এবং এক্সপ্রেশন সহজেই স্ট্রিং-এর মধ্যে যোগ করতে সাহায্য করে, যা কোডকে আরও পড়তে সহজ করে তোলে। টেমপ্লেট স্ট্রিংস ব্যাকটিকস (```) ব্যবহার করে তৈরি করা হয়

```jsx
const numbers = [89, 35, 98, 12];
const student = {
    name: 'Salib Khan',
    age: 32,
    movies: ['king khan', 'Dhakar Mastan']
};

const about = `My Name is ${student.name} age of ${student.age} has number ${numbers[2]} also liked movies ${student.movies[0]}`;

console.log(about)
```

```jsx
let price = 100;
let discount = 15;
let finalPrice = `The final price is $${price - discount}.`;

console.log(finalPrice); // Output: "The final price is $85."
```

## Ternary Operator

- **Ternary Operator** হলো `if...else` স্টেটমেন্টের একটি শর্টকাট বা সংক্ষিপ্ত রূপ। এটি একটি কন্ডিশন চেক করে এবং কন্ডিশন `true` হলে এক ভ্যালু, আর `false` হলে আরেকটি ভ্যালু রিটার্ন করে।

### **Syntax**

```jsx
condition ? expression1 : expression2;
```

- `condition`: A boolean expression (evaluates to `true` or `false`).
- `expression1`: The value or code to return if the condition is `true`.
- `expression2`: The value or code to return if the condition is `false`.

```jsx
const age = 18;

// Using Ternary Operator
const eligibility = age >= 18 ? "Eligible to vote" : "Not eligible to vote";

console.log(eligibility); // Output: Eligible to vote
```

```jsx
const isLoggedIn = true;

// Assign a message based on login status
const message = isLoggedIn ? "Welcome back!" : "Please log in.";

console.log(message); // Output: Welcome back!
```

```jsx
const isDarkMode = true;

// Using ternary for inline functionality
isDarkMode ? console.log("Dark mode enabled") : console.log("Light mode enabled");
// Output: Dark mode enabled
```

**Multiple condition**

```jsx
let drink = (money > 100 && myVar > 100) ? 'coke' : 'filter water';
```

## Arrow Function  ( ⇒ )

- **Arrow functions** are a shorter and more concise way to write functions in JavaScript. They are especially useful for simple operations and are often used in modern JavaScript development. Arrow functions use the `=>` syntax and were introduced in ES6.

```jsx
const getFiftyFive = () => 55;
const addSixtyFive = num => num + 65;
const isEven = x => x % 2 == 0;
const addThree = (x, y, z) => x + y + z;

const doMath = (num1, num2) => {
    const sum = num1 + num2;
    return sum;
}
```

```jsx
const add = (a, b) => a + b
console.log(add(5, 3)); // Output: 8

let numbers = [1, 2, 3, 4, 5];
let doubled = numbers.map(num => num * 2);

console.log(doubled); // Output: [2, 4, 6, 8, 10]
```

## Spread Operator

- **স্প্রেড অপারেটর** (`...`) JavaScript-এ একটি শক্তিশালী ফিচার যা আপনাকে **এরে** বা **অবজেক্ট** থেকে উপাদানগুলি "স্প্রেড" বা "আনপ্যাক" করতে সাহায্য করে। এটি একাধিক অ্যারে/অবজেক্টকে একত্রিত করতে বা একটি অ্যারে/অবজেক্টের উপাদানগুলোকে অন্য অ্যারে/অবজেক্টে কপি করতে ব্যবহৃত হয়। স্প্রেড অপারেটরটি অ্যারে এবং অবজেক্টের সাথে কাজ করার সময় খুবই কার্যকর।

```jsx
let arr1 = [1, 2, 3];
let arr2 = [4, 5, 6];

// Copying elements from arr1 into a new array
let copiedArray = [...arr1];
console.log(copiedArray); // Output: [1, 2, 3]

// Combining two arrays
let combinedArray = [...arr1, ...arr2];
console.log(combinedArray); // Output: [1, 2, 3, 4, 5, 6]
```

```jsx
let person = {
    name: "John",
    age: 30
};

let contact = {
    email: "john@example.com",
    phone: "123456789"
};

// Copying the person object
let newPerson = {...person};
console.log(newPerson); // Output: { name: "John", age: 30 }

// Combining two objects
let combinedObject = {...person, ...contact};
console.log(combinedObject);
// Output: { name: "John", age: 30, email: "john@example.com", phone: "123456789" }
```

```jsx
let arr = [1, 2, 3];

// Adding a new element to the front
let updatedArr = [0, ...arr];
console.log(updatedArr); // Output: [0, 1, 2, 3]

// Adding a new element to the end
updatedArr = [...arr, 4];
console.log(updatedArr); // Output: [1, 2, 3, 4]
```

## Array Map

- **`map()`** মেথড JavaScript-এ একটি অ্যারের প্রতিটি উপাদানের উপর কাজ করে এবং সেই উপাদানগুলোকে পরিবর্তন করে একটি **নতুন অ্যারে** তৈরি করে। এটি মূল অ্যারেটিকে পরিবর্তন না করেই নতুন মান যুক্ত করে।
- একটি **নতুন অ্যারে** রিটার্ন করে যেখানে পরিবর্তিত উপাদান থাকে।


```jsx
const numbers = [1, 2, 3, 4, 5];

// Use map() to create a new array with doubled values
const doubled = numbers.map(num => num * 2);

console.log(doubled); // Output: [2, 4, 6, 8, 10]
console.log(numbers); // Original array remains unchanged: [1, 2, 3, 4, 5]
```

```jsx
const users = [
    { name: "Alice", age: 25 },
    { name: "Bob", age: 30 },
    { name: "Charlie", age: 35 }
];

// Extract only the names of the users
const names = users.map(user => user.name);

console.log(names); // Output: ["Alice", "Bob", "Charlie"]
```

```jsx
const fruits = ["apple", "banana", "cherry"];

// Convert each fruit name to uppercase
const uppercased = fruits.map(fruit => fruit.toUpperCase());

console.log(uppercased); // Output: ["APPLE", "BANANA", "CHERRY"]
```

### Key Points:

- **`map()` সবসময় একটি নতুন অ্যারে রিটার্ন করে।** এটি মূল অ্যারেকে পরিবর্তন করে না।
- নতুন অ্যারের দৈর্ঘ্য মূল অ্যারের সমান হয়।
- `map()` সাধারণত একটি অ্যারের উপাদান প্রক্রিয়া করতে বা নতুনভাবে সাজাতে ব্যবহৃত হয়।

### When to Use `map()`:

- অ্যারের ডেটা পরিবর্তন বা রূপান্তর করতে।
- নির্দিষ্ট প্রোপার্টি বের করতে।
- অ্যারে লুপ করার কাজ সহজ করতে।


## for Each

- **`forEach()`** মেথড একটি অ্যারের প্রতিটি উপাদানের উপর কাজ করে এবং একটি **callback function** চালায়। এটি মূলত প্রতিটি উপাদানের উপর নির্দিষ্ট কোনো কাজ (যেমন প্রিন্ট করা, একটি ভেরিয়েবল আপডেট করা ইত্যাদি) করার জন্য ব্যবহৃত হয়।
- **তবে এটি নতুন কোনো অ্যারে রিটার্ন করে না।**

```jsx
const numbers = [1, 2, 3, 4, 5];

// Print each element
numbers.forEach(num => {
    console.log(num);
});
// Output:
// 1
// 2
// 3
// 4
// 5
```

```jsx
const fruits = ["apple", "banana", "cherry"];

fruits.forEach((fruit, index) => {
    console.log(`Index: ${index}, Fruit: ${fruit}`);
});
// Output:
// Index: 0, Fruit: apple
// Index: 1, Fruit: banana
// Index: 2, Fruit: cherry
```

```jsx
const numbers = [10, 20, 30];
let sum = 0;

// Calculate the sum of all elements
numbers.forEach(num => {
//	sum = sum + num
    sum += num;
});

console.log(sum); // Output: 60
```

## Filter

- **`filter()`** মেথডটি একটি **নতুন অ্যারে** তৈরি করে, যেখানে শুধুমাত্র সেই উপাদানগুলো থাকে যেগুলো নির্দিষ্ট শর্ত (যা `true` রিটার্ন করে) পূরণ করে। এটি সাধারণত একটি অ্যারের নির্দিষ্ট উপাদানগুলো ফিল্টার করার জন্য ব্যবহার করা হয়।
- Returns all elements that satisfy the condition.
- Always returns a new array (even if empty).

```jsx
const numbers = [1, 2, 3, 4, 5, 6];
const evenNumbers = numbers.filter(num => num % 2 === 0);

console.log(evenNumbers); // Output: [2, 4, 6]
```

```jsx
const names = ["Ali", "Hasan", "John", "Sarah", "Kate"];
const longNames = names.filter(name => name.length > 4);

console.log(longNames); // Output: ["Hasan", "Sarah"]
```

```jsx
const numbers = [5, -3, 8, -1, 10, -6];
const positiveNumbers = numbers.filter(num => num > 0);

console.log(positiveNumbers); // Output: [5, 8, 10]
```

```jsx
const names = ["Ali", "Hasan", "rahim", "Rita", "Sarah", "rafiq"];

// Filter names starting with 'R' or 'r'
const namesWithR = names.filter(name => name.toLowerCase().startsWith("r"));

console.log(namesWithR); // Output: ["rahim", "Rita", "rafiq"]
```

```jsx
const names = ["Ali", "Hasan", "rahim", "Rita", "Sarah", "rafiq"];

// Filter names containing 'R' or 'r'
const namesWithR = names.filter(name => name.toLowerCase().includes("r"));

console.log(namesWithR); // Output: ["rahim", "Rita", "Sarah", "rafiq"]
```

## Find

- **`find()`** মেথডটি একটি অ্যারের প্রথম উপাদানটি খুঁজে বের করে যা একটি নির্দিষ্ট শর্ত পূরণ করে। এটি **শুধুমাত্র প্রথম ম্যাচিং উপাদান** রিটার্ন করে। যদি কোনও উপাদান শর্ত পূরণ না করে, তাহলে এটি `undefined` রিটার্ন করে।
- Returns only the first element that satisfies the condition.
- `find()` Returns an Object (If the Condition Matches)
- If the condition doesn't match any object in the array, `find()` returns `undefined`.

```jsx
const numbers = [2, 4, 6, 8, 9, 10, 11];

// Find the first odd number
const firstOdd = numbers.find(num => num % 2 !== 0);

console.log(firstOdd); // Output: 9
```

```jsx
const names = ["Ali", "Hasan", "Rahim", "Rita", "Sarah", "Rafiq"];

// Find the first name with length > 5
const longName = names.find(name => name.length > 5);

console.log(longName); // Output: "Hasan"
```

```jsx
const names = ["Ali", "Hasan", "Rahim", "Rita", "Sarah", "Rafiq"];

// Find the first name containing 'a' (case-insensitive)
const nameWithA = names.find(name => name.toLowerCase().includes("a"));

console.log(nameWithA); // Output: "Ali"
```

## Array Destructuring

- **Array destructuring** হচ্ছে একটি ES6 এর একটি ফিচার যা  একটি অ্যারে থেকে মানগুলো আলাদা ভেরিয়েবল হিসেবে আনপ্যাক করার সুবিধা দেয়। এটি অ্যারে থেকে মানগুলো সহজে আলাদা করার এবং তা আলাদা ভেরিয়েবলগুলোতে যুক্ত করার উপায়।

```jsx
const array = [1, 2, 3];

// Destructuring the array
const [a, b, c] = array;

console.log(a); // Output: 1
console.log(b); // Output: 2
console.log(c); // Output: 3
```

```jsx
const array = [10];

// Assigning a default value to `b` and `c`
const [a, b = 20, c = 30] = array;

console.log(a); // Output: 10
console.log(b); // Output: 20 (default value)
console.log(c); // Output: 30 (default value)
```

```jsx
const student = {
    name: 'Salib Khan',
    age: 32,
    movies: ['king khan', 'Dhakar Mastan']
}

const [firstMovie, secondMovie] = student.movies;
```

## Object Destructuring

- **Object destructuring** হলো একটি ES6 ফিচার যা আপনাকে একটি অবজেক্ট থেকে তার প্রপার্টিগুলোকে আলাদা ভেরিয়েবল হিসেবে নিতে দেয়। এতে কোড লেখা সহজ হয় এবং একাধিক প্রপার্টি সহজে একসাথে এক্সট্র্যাক্ট করা যায়।

```jsx
const person = {
  name: "Ali",
  age: 25,
  profession: "Developer"
};

// Object destructuring
const { name, age, profession } = person;

console.log(name);       // Output: Ali
console.log(age);        // Output: 25
console.log(profession); // Output: Developer
```

```jsx
const person = {
  name: "John"
};

// Default value
const { name, age = 30 } = person;

console.log(name); // Output: John
console.log(age);  // Output: 30 (default value)
```

### Nested Object Destructuring

```jsx
const person = {
  name: "Sarah",
  contact: {
    email: "sarah@example.com",
    phone: "123-456-7890"
  }
};

// Nested object destructuring
const { name, contact: { email, phone } } = person;

console.log(name);  // Output: Sarah
console.log(email); // Output: sarah@example.com
console.log(phone); // Output: 123-456-7890
```

- **Object Destructuring**-এ `?` অপারেটর সরাসরি কোনো ভিন্ন কাজ করে না, কিন্তু এটি **Optional Chaining (`?.`)** এর মাধ্যমে অবজেক্টের গভীরতর প্রপার্টি নিরাপদে অ্যাক্সেস করতে সাহায্য করে। এটি `null` বা `undefined` প্রপার্টি থাকলে এরর না দিয়ে `undefined` রিটার্ন করে।

```jsx
const employee = {
    ide: 'VS Code',
    designation: 'developer',
    machine: 'mac',
    languages: ['html', 'css', 'js'],
    specification: {
        height: 66,
        weight: 67,
        address: 'kumarkhali',
        drink: 'water',
        watch: {
            color: 'black',
            price: 500,
            brand: 'garmin'
        }
    }
}

const { machine, ide } = employee;
// const { weight, address } = employee.specification;
const { brand } = employee?.specification?.watch;
```

## JSON

- **`JSON.stringify()`** এবং **`JSON.parse()`** হলো জাভাস্ক্রিপ্টের দুটি মেথড যা ডাটা ফরম্যাট পরিবর্তনের জন্য ব্যবহৃত হয়।
- **`JSON.stringify()`**: জাভাস্ক্রিপ্ট অবজেক্টকে JSON ফরম্যাটে স্ট্রিং-এ রূপান্তর করে।
- **`JSON.parse()`**: JSON ফরম্যাটের স্ট্রিংকে আবার জাভাস্ক্রিপ্ট অবজেক্টে রূপান্তর করে।

### **Stringifying JSON (Convert JavaScript Object to JSON String)**

```jsx
const user = {
  name: "Ali",
  age: 25
};

// Convert JavaScript object to JSON string
const jsonString = JSON.stringify(user);

console.log(jsonString);
// Output: {"name":"Ali","age":25}
```

### **Parsing JSON (Convert JSON String to JavaScript Object)**

```jsx
const jsonString = '{"name": "Ali", "age": 25}';

// Convert JSON string to JavaScript object
const user = JSON.parse(jsonString);

console.log(user.name); // Output: Ali
console.log(user.age);  // Output: 25
```

