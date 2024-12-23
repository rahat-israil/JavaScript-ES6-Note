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

### 2.