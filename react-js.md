# 📝 ReactJS Notes 📝

`Developed By: Meta(Facebook)`

`No.1 Most Popular JS Library`

`Used in MERN Stack`

## 📢 Introduction - More About React 📢

**React** also known as **ReactJS** or **React.Js**, is an open-source **Javascript Library** for building user interfaces(UIs) and single-page applications(SPAs). Developed and maintained by Meta, React was first released in 2013 and has since gained widespread adoption in the web development community.

**Key features and Concepts accosiated with React:**

- **Component Based Architexture**: React is built around the concept of reusable components. Components are self-contained, isolated building blocks for UI elements, and they can be composed together to create complex user interfaces.
- **Virtual DOM**: React uses a virtual representation of the actual DOM(Document Object Model). When changes are made to the UI, React first updates the Virtual DOM, and then it calculates the most efficient way to update the real DOM, minimizing performance bottlenecks and re-renders.
- **Declarative Syntax**: React applications are built using a declarative syntax, which means you describe what the UI should look like for a given state, and React takes care of updating the DOM to match that description.
- **React Native**: In addition to web development, React can be used to build mobile applications through React Native. React Native allows developers to write code in React and deploy it as a native app on both iOS and Android platforms.
- **State Management**: While React itself provides a mechanism for managing component state, it is often used in conjuction with state management libraries like Redux or the Context API for managing global application state.
- **Component Lifecycle**: React components have a lifecycle that includes various methods like `componentDidMount`, `componentDidUpdate`, `componentWillUnmount`, which allow developers to hook into different phases of a component's existence.
- **React Router**: For building single-page applications with multiple views or pages, React developers often use React Router, a popular routing library that integrates seamlessly with React.
- **JSX(JavaScript XML)**: React uses a syntax extension called JSX, which allows you to write HTML-like code within your JavaScript. JSX is transpiled to JavaScript code that React understands.

React is often used in **combination** with other libraries and tools, such as `Babel` for transpiling `JSX` and `ES6/ES7 JavaScript` into browser-compatible code, and Webpack for bundling and optimizing the application's assets.

**More functionalities and key features offered by React:**

- **Undirectional Data Flow**: React enforces an undirectional data flow. Data flows from parent components to child components, which makes it easier to understand how data is passed and modified in your application. This data flow helps prevent common bugs and makes debugging more straightforward.
- **Component Reusability**: One of React's core principles is the reusability of components. Developers can create UI components for common elements(e.g. buttons, forms, cards) and reuse them across different parts of their application or even different projects. This promotes code consistency and maintainability.
- **Virtual DOM Reconciliation**: React's Virtual DOM system efficiency updates the actual DOM. Instead of making direct and potentially costly changes to the real DOM, React calculates the difference between the current Virtual DOM and the new one, and then selectively updates only the parts of the DOM that have changed. This minimizes performance bottlenecks associated with frequent DOM manipulations.
- **Server-Side Renderin(SSR)**: The initial HTML for a web page is generated on the server and sent to the client. This can improve initial page load performance and is crucial for search engine optimization(SEO).
- **React Hooks**: Introduced in React 16.8, hooks are functions that allow you to use state and other React features in functional components. Hooks eliminate the need for class components in many cases and make it easier to manage component state and side effects.
- **Context API**: React provides the Context API, which simplifies the process of passing data down the component tree without having to explicitly pass props at every level. It's particularly useful for managing global state and settings in an application.
- **React DevTools**: React offers browser extensions and tools like React DevTools, which can help developers inspect and debug React components. They provide valuable insights into component hierarchies, state changes, and performance.
- **Community and Ecosystem**: React has a vast ecosystem of libraries and tools built around it. Some popular ones include Redux for state management, Axios for handling HTTP requests, and Material-UI or Ant Design for pre-designed UI components. This ecosystem makes it easier for developers to extend React's capabilities and integrate with other technologies.
- **Compatibility**: React can be integrated with other Javascript frameworks and libraries. This means you can graddually adopt React into an existing codebase, which is useful when migrating from older technologies or frameworks.

### 💻 Creating and Nesting Components 💻 

React apps are made out of components. A component is a place of the UI that has its own logic and appearance. A component can be as a button or as large as an entire page.
React components are JavaScript functions that return markup.

```javascript
    function MyButton() {
        return (
            <button>A Button</button>
        )
    }
```

Now that `MyButton` has been declared, it can be nested into another component.

```javascript
    export default function MyApp() {
        return (
            <div>
                <h1>Welcome to my App</h1>
                <MyButton />
            </div>
        )
    }
```

The `export default` keywords specify the main component in the file. If you're not familiar with some piece of JavaScript syntax, `[https://developer.mozilla.org/en-US/docs/web/javascript/reference/statements/export](MDN)` and `[https://javascript.info/import-export](javascript.info)` have great references.

Notice <MyButton /> starts with a capital letter. That's how you know it's a React component. React component names must always start with a capital letter, while HTML tags must be lowercase.

### 💻 Writing markup with JSX 💻 

The markup syntax you've seen above is called JSX. It is optional, but most React projects use JSX for its convenience.
JSX is stricter than HTML. You have to close tags like <br />. Your component also can't return multiple JSX tags. You have to wrap them into a shared parent, like a `<div>...</div>` or an empty `<>...</>` wrapper:

```javascript
    function AboutPage() {
        return (
            <>
                <h1>About</h1>
                <p>
                    Hello
                    <br />
                    How are you?    
                </p>
            </p>
        )
    }
```

If you have a lot of HTML to port to JSX, you can use:
`[https://transform.tools/html-to-jsx](HTML to JSX Converter)`