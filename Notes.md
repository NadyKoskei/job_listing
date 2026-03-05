# React Crash Course Notes
Based on: Brad Traversy – React Crash Course

## 1. What React Is

React is a JavaScript library for building user interfaces.

It is mainly used to build single-page applications (SPAs).

React allows developers to create reusable UI components.

Instead of manipulating the DOM directly, React uses a Virtual DOM to efficiently update the UI.

React focuses on the view layer in applications.

Key Ideas

Component-based architecture

Reusable UI

Efficient rendering

Declarative programming style

## 2. Creating a React App

React apps can be created using tools like:

Create React App

Vite

Other React frameworks

Typical command example:

npx create-react-app my-app
cd my-app
npm start

This generates the project structure and starts the development server.

## 3. React Project Structure

Important folders and files:

node_modules

Contains all installed dependencies.

public folder

Contains static files.

The index.html file lives here.

src folder

This is where most of the application code is written.

Important files include:

index.js

App.js

component files

## 4. The Root Component

React apps usually start with a root component.

Example:

function App() {
  return (
    <div>
      <h1>Hello React</h1>
    </div>
  );
}

This component controls the main UI of the application.

## 5. JSX (JavaScript XML)

JSX is a syntax extension that allows writing HTML-like code inside JavaScript.

Example:

const element = <h1>Hello World</h1>

Important rules:

Must return a single parent element

Can embed JavaScript expressions using {}

Example:

const name = "John"
<h1>Hello {name}</h1>

## 6. Expressions in JSX

You can insert JavaScript expressions inside JSX using curly braces {}.

Examples:

const x = 10

<h1>{x + 5}</h1>

You can also call functions or variables inside JSX.

## 7. Creating Components

Components are reusable UI pieces.

Two types exist:

Functional Components (modern approach)
function Header() {
  return <h1>Task Tracker</h1>
}
Usage
<Header />

Components help break UI into small reusable pieces.

## 8. Props (Properties)

Props allow passing data from parent components to child components.

Example:

function Header(props) {
  return <h1>{props.title}</h1>
}

Usage:

<Header title="Task Tracker" />

Props are read-only.

## 9. PropTypes

PropTypes are used to validate props.

Example:

Header.propTypes = {
  title: PropTypes.string
}

Benefits:

Helps detect errors

Improves code reliability

## 10. Styling in React

Styling can be done in several ways:

CSS files

Inline styles

CSS frameworks

Styled components

Example inline style:

<h1 style={{ color: "red" }}>Hello</h1>
11. Events in React

React handles events similar to JavaScript but with camelCase syntax.

Example:

<button onClick={handleClick}>
  Click Me
</button>

Events trigger functions that update UI or state.

## 12. Lists in React

Lists are usually created using .map().

Example:

tasks.map((task) => (
  <Task key={task.id} task={task} />
))

Important:

Each item needs a unique key

## 13. React State

State represents data that can change over time.

React re-renders the component whenever state changes.

Example:

const [tasks, setTasks] = useState([])

## 14. useState Hook

useState allows functional components to store state.

Example:

const [count, setCount] = useState(0)

Update state:

setCount(count + 1)

## 15. Prop Drilling

Prop drilling happens when data is passed through multiple components.

Example:

Parent → Child → Grandchild

This can make apps harder to maintain.

Solutions include:

Context API

State management libraries

## 16. Conditional Rendering

React can render components conditionally.

Example:

{tasks.length === 0 ? (
  <p>No tasks</p>
) : (
  <Tasks tasks={tasks} />
)}

## 17. Forms in React

Forms are usually controlled components.

State controls input values.

Example:

const [text, setText] = useState("")

Input:

<input
  type="text"
  value={text}
  onChange={(e) => setText(e.target.value)}
/>

## 18. useEffect Hook

useEffect runs code when the component renders or when state changes.

Example:

useEffect(() => {
  fetchTasks()
}, [])

Uses:

Fetching API data

Side effects

Lifecycle logic

## 19. Fetching Data from an API

React apps often fetch data from APIs.

Example:

const res = await fetch("http://localhost:5000/tasks")
const data = await res.json()

This data is then stored in state.

## 20. Updating Server Data

Typical operations:

GET → retrieve data

POST → add data

DELETE → remove data

PUT/PATCH → update data

React updates the UI after server responses.

## 21. Routing in React

Routing allows multiple pages in a React app.

Example using React Router:

/ → Home

/about → About page

This makes navigation possible in SPAs.

22. Building for Production

To create a production build:

npm run build

This generates an optimized version of the app for deployment.
