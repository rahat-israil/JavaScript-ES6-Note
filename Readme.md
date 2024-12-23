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

