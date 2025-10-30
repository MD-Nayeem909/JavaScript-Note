# JavaScript-Note
##JavaScript-এর কিছু ফাংশন আর ধারণা (concepts) প্রতিদিনের কাজ আর প্রজেক্টে বারবার লাগে।

🧠 ১. Most Used Built-in JavaScript Functions

এগুলো এমন ফাংশন যেগুলো আপনি প্রায় প্রতিটি প্রজেক্টে ব্যবহার করবেন।

🔹 String Functions
let text = "Hello World";
text.length;            // 11
text.toUpperCase();     // "HELLO WORLD"
text.toLowerCase();     // "hello world"
text.includes("World"); // true
text.split(" ");        // ["Hello", "World"]
text.replace("World", "JS"); // "Hello JS"
text.trim();            // removes spaces from start and end

👉 ব্যবহার: form input পরিষ্কার করা, validation, search filter ইত্যাদি।

🔹 Array Functions (সবচেয়ে গুরুত্বপূর্ণ)
let numbers = [1, 2, 3, 4, 5];

numbers.map(n => n * 2);         // [2, 4, 6, 8, 10]
numbers.filter(n => n > 2);      // [3, 4, 5]
numbers.find(n => n === 3);      // 3
numbers.reduce((a, b) => a + b, 0); // 15
numbers.some(n => n > 4);        // true
numbers.every(n => n > 0);       // true
numbers.sort((a, b) => b - a);   // [5, 4, 3, 2, 1]
numbers.forEach(n => console.log(n)); // loops

👉 ব্যবহার: ডেটা লিস্ট প্রক্রিয়াজাত করা, API থেকে পাওয়া data পরিবর্তন করা, UI তে map করা ইত্যাদি।


🔹 Object Functions
const user = { name: "Alfa", age: 22 };

Object.keys(user);   // ["name", "age"]
Object.values(user); // ["Alfa", 22]
Object.entries(user); // [["name","Alfa"],["age",22]]


👉 ব্যবহার: dynamic key-value কাজ করা, JSON data হ্যান্ডেল করা।


⚙️ ২. Important JavaScript Concepts (must know)

🔸 ১. Destructuring
const { name, age } = user;
const [a, b] = [10, 20];

🔸 ২. Spread & Rest Operators
const newUser = { ...user, city: "Dhaka" };
const sum = (...nums) => nums.reduce((a, b) => a + b);

🔸 ৩. Template Literals
const greeting = `Hello ${user.name}, your age is ${user.age}`;

🔸 ৪. Ternary Operator
const isAdult = user.age > 18 ? "Yes" : "No";

🔸 ৫. Optional Chaining & Nullish Coalescing
user?.address?.city;      // avoid errors if address undefined
user.age ?? 18;           // default value if null or undefined

🕒 ৩. Useful Utility Functions (যেগুলো নিজেই বানাতে পারেন)

✅ Random number
function random(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}

✅ Capitalize first letter
function capitalize(str) {
  return str.charAt(0).toUpperCase() + str.slice(1);
}

✅ Format date
function formatDate(date) {
  return new Date(date).toLocaleDateString();
}

💡 ৪. Bonus: Asynchronous Concepts

এসব API data fetch বা React/Vue প্রজেক্টে অপরিহার্য।

// Promise
fetch("https://api.example.com/data")
  .then(res => res.json())
  .then(data => console.log(data))
  .catch(err => console.error(err));

// async/await
async function loadData() {
  try {
    const res = await fetch("https://api.example.com/data");
    const data = await res.json();
    console.log(data);
  } catch (err) {
    console.error(err);
  }
}

🧩 সারসংক্ষেপে — প্রতিদিন দরকার হয় এমন মূল বিষয়গুলো:
Category                   	Topics
String      : 	toUpperCase, split, replace
Array	      :   map, filter, reduce, find
Object	    :   keys, values, entries
Modern JS  	:   destructuring, spread, template literal
Logic      	:   ternary, optional chaining
Async       :   fetch, async/await





























