# Readings: React 1

## ES6

- Variable declaration
- Constant declaration
- Arrow function syntax
- Template literals
- Implicit returns
- Key/property shorthand
- Method definition shorthand
- Destructuring (object matching)
- Array iteration (looping)
- Default parameters
- Spread syntax
- Classes/constructor functions
- Inheritance
- Modules - export/import
- Promises/callbacks

## React

> Hello World

React is a JavaScript library, and so we’ll assume you have a basic understanding of the JavaScript language.

```commandline
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<h1>Hello, world!</h1>);
```

> Introducing JSX

``` const element = <h1>Hello, world!</h1>;```

This tag syntax is neither a string nor HTML.
It is called JSX, and it is a syntax extension to JavaScript.

React embraces the fact that rendering logic is inherently coupled with other UI logic: how events are handled, how the state changes over time, and how the data is prepared for display.

Instead of artificially separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units called “components” that contain both.


> Rendering Elements

An element describes what you want to see on the screen

Unlike browser DOM elements, React elements are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.

Applications built with just React usually have a single root DOM node. If you are integrating React into an existing app, you may have as many isolated root DOM nodes as you like.

To render a React element, first pass the DOM element to ```ReactDOM.createRoot()```, then pass the React element to ```root.render()```

React elements are immutable. Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie: it represents the UI at a certain point in time.

React DOM compares the element and its children to the previous one, and only applies the DOM updates necessary to bring the DOM to the desired state.

> Components and Props

Components let you split the UI into independent, reusable pieces, and think about each piece in isolation.

Conceptually, components are like JavaScript functions. They accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen.

The simplest way to define a component is to write a JavaScript function

Components can refer to other components in their output. This lets us use the same component abstraction for any level of detail. A button, a form, a dialog, a screen: in React apps, all those are commonly expressed as components.

Whether you declare a component as a function or a class, it must never modify its own props.

> State and Lifecycle

You can convert a function component to a class in five steps:

1. Create an ES6 class, with the same name, that extends React.Component.
2. Add a single empty method to it called render().
3. Move the body of the function into the render() method.
4. Replace props with this.props in the render() body.
5. Delete the remaining empty function declaration.

In applications with many components, it’s very important to free up resources taken by the components when they are destroyed.

There are three things you should know about setState().

- Do Not Modify State Directly
- State Updates May Be Asynchronous
- State Updates are Merged

> Handling Events

Handling events with React elements is very similar to handling events on DOM elements. There are some syntax differences:

- React events are named using camelCase, rather than lowercase.
- With JSX you pass a function as the event handler, rather than a string.

Another difference is that you cannot return false to prevent default behavior in React. You must call preventDefault explicitly. For example, with plain HTML, to prevent the default form behavior of submitting






## Tailwind CSS

Traditionally, whenever you need to style something on the web, you write CSS.

With Tailwind, you style elements by applying pre-existing classes directly in your HTML.

This approach allows us to implement a completely custom component design without writing a single line of custom CSS.

A common reaction to this approach is wondering, “isn’t this just inline styles?” and in some ways it is — you’re applying styles directly to elements instead of assigning them a class name and then styling that class.

But using utility classes has a few important advantages over inline styles:

- Designing with constraints.
- Responsive design.
- Hover, focus, and other states.

The biggest maintainability concern when using a utility-first approach is managing commonly repeated utility combinations.

This is easily solved by extracting components and partials, and using editor and language features like multi-cursor editing and simple loops.

Aside from that, maintaining a utility-first CSS project turns out to be a lot easier than maintaining a large CSS codebase, simply because HTML is so much easier to maintain than CSS. Large companies like GitHub, Netflix, Heroku, Kickstarter, Twitch, Segment, and more are using this approach with great success.


## Next.js

Next.js: The React Framework

- An intuitive page-based routing system (with support for dynamic routes)
- Pre-rendering, both static generation (SSG) and server-side rendering (SSR) are supported on a per-page basis
- Automatic code splitting for faster page loads
- Client-side routing with optimized prefetching
- Built-in CSS and Sass support, and support for any CSS-in-JS library
- Development environment with Fast Refresh support
- API routes to build API endpoints with Serverless Functions
- Fully extendable





