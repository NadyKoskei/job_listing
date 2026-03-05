# ⚛️ React Learning Project

## 📌 Overview

This repository documents my journey learning **React.js**, one of the most widely used JavaScript libraries for building modern user interfaces.

The goal of this project is to understand the **core concepts of React development** and apply them by building small components and experimenting with modern frontend workflows.

My learning is currently based on the following crash course:

**React Crash Course (YouTube)**
https://www.youtube.com/watch?v=LDB4uaJ87e0

This course introduces the fundamental concepts needed to start building React applications.

---

# 🎯 Learning Goals

Through this project I aim to:

* Understand how React works internally
* Build reusable UI components
* Learn modern JavaScript (ES6+) used in React
* Manage state and component data
* Understand React project structure
* Learn best practices for scalable frontend applications

---

# 🛠 Tech Stack

| Technology            | Purpose                     |
| --------------------- | --------------------------- |
| **React**             | Frontend JavaScript library |
| **JavaScript (ES6+)** | Core programming language   |
| **Node.js**           | Runtime environment         |
| **npm**               | Package manager             |
| **Vite**              | React project build tool    |
| **HTML & CSS**        | UI structure and styling    |

---

# 🧠 Core Concepts Learned

## 1. React Fundamentals

React is a **JavaScript library used to build interactive user interfaces** using reusable components.

Key ideas:

* Component-based architecture
* Declarative UI
* Virtual DOM

---

## 2. Components

Components are **independent reusable pieces of UI**.

Example:

```jsx
function Button() {
  return <button>Click Me</button>;
}
```

Benefits:

* Code reusability
* Easier maintenance
* Modular UI design

---

## 3. JSX

JSX allows developers to write **HTML-like syntax inside JavaScript**.

Example:

```jsx
const element = <h1>Hello React</h1>;
```

JSX makes UI code easier to read and write.

---

## 4. Props

Props are used to **pass data between components**.

Example:

```jsx
function Greeting(props) {
  return <h1>Hello {props.name}</h1>;
}
```

Usage:

```jsx
<Greeting name="Nady" />
```

---

## 5. State

State allows React components to **store and update dynamic data**.

Example:

```jsx
import { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <button onClick={() => setCount(count + 1)}>
      Count: {count}
    </button>
  );
}
```

---

## 6. Event Handling

React handles user interactions like clicks or inputs.

Example:

```jsx
function handleClick() {
  alert("Button clicked");
}

<button onClick={handleClick}>Click Me</button>
```

---

# 📁 Project Structure

```
react-learning-project
│
├── node_modules
├── public
│
├── src
│   ├── components
│   │   └── Button.jsx
│   │
│   ├── App.jsx
│   ├── main.jsx
│   └── index.css
│
├── package.json
├── package-lock.json
└── vite.config.js
```

---

# 🧪 What I Am Practicing

During this learning process I am practicing:

* Creating functional components
* Passing props between components
* Managing component state
* Handling user events
* Structuring scalable React applications

---

# 📈 Learning Progress

| Topic                | Status         |
| -------------------- | -------------- |
| React Introduction   | ✅              |
| Project Setup (Vite) | ✅              |
| JSX                  | ✅              |
| Components           | ✅              |
| Props                | ✅              |
| State                | 🔄 In Progress |
| Event Handling       | 🔄 In Progress |
| Small React Projects | ⏳ Coming Next  |

---

# 🚀 Future Improvements

As I progress, I plan to extend this repository by adding:

* Mini React projects
* API integration
* React hooks
* Component styling with Tailwind
* Deployment of React applications

---

# 👩🏾‍💻 Author

**Nady**

Final-year **Cybersecurity Top-Up Degree Student** expanding skills in:

* Frontend Development
* Modern JavaScript
* React Ecosystem
* Full-stack development foundations

---

⭐ This repository represents my **continuous learning journey into modern web development with React**.

