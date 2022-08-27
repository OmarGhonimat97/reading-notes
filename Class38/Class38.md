# Readings: React 2

## Conditional Rendering
Conditional rendering in React works the same way conditions work in JavaScript. Use JavaScript operators like if or the conditional operator to create elements representing the current state, and let React update the UI to match them.

You can use variables to store elements. This can help you conditionally render a part of the component while the rest of the output doesn’t change.

You may embed expressions in JSX by wrapping them in curly braces. This includes the JavaScript logical && operator. It can be handy for conditionally including an element.

Another method for conditionally rendering elements inline is to use the JavaScript conditional operator ```condition ? true : false```.

In rare cases you might want a component to hide itself even though it was rendered by another component. To do this return null instead of its render output.

## Lists & Keys

You can build collections of elements and include them in JSX using curly braces {}.

Usually you would render lists inside a component.

Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity.
The best way to pick a key is to use a string that uniquely identifies a list item among its siblings. Most often you would use IDs from your data as keys.

We don’t recommend using indexes for keys if the order of items may change. This can negatively impact performance and may cause issues with component state.

Keys used within arrays should be unique among their siblings. However, they don’t need to be globally unique. We can use the same keys when we produce two different arrays.



## Forms

HTML form elements work a bit differently from other DOM elements in React, because form elements naturally keep some internal state.

In HTML, form elements such as ```<input>, <textarea>, and <select>``` typically maintain their own state and update it based on user input. In React, mutable state is typically kept in the state property of components, and only updated with setState().

We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a “controlled component”.

In React, a ```<textarea>``` uses a value attribute instead. This way, a form using a ```<textarea>``` can be written very similarly to a form that uses a single-line input

When you need to handle multiple controlled input elements, you can add a name attribute to each element and let the handler function choose what to do based on the value of event.target.name.

Specifying the value prop on a controlled component prevents the user from changing the input unless you desire so. If you’ve specified a value but the input is still editable, you may have accidentally set value to undefined or null.

It can sometimes be tedious to use controlled components, because you need to write an event handler for every way your data can change and pipe all of the input state through a React component. This can become particularly annoying when you are converting a preexisting codebase to React, or integrating a React application with a non-React library. In these situations, you might want to check out uncontrolled components, an alternative technique for implementing input forms.


## Lifting State

There should be a single “source of truth” for any data that changes in a React application. Usually, the state is first added to the component that needs it for rendering. Then, if other components also need it, you can lift it up to their closest common ancestor. Instead of trying to sync the state between different components, you should rely on the top-down data flow.

Lifting state involves writing more “boilerplate” code than two-way binding approaches, but as a benefit, it takes less work to find and isolate bugs. Since any state “lives” in some component and that component alone can change it, the surface area for bugs is greatly reduced. Additionally, you can implement any custom logic to reject or transform user input.

If something can be derived from either props or state, it probably shouldn’t be in the state.


## Composition vs Inheritance

Some components don’t know their children ahead of time. This is especially common for components like Sidebar or Dialog that represent generic “boxes”.
We recommend that such components use the special children prop to pass children elements directly into their output.

Sometimes we think about components as being “special cases” of other components.

In React, this is also achieved by composition, where a more “specific” component renders a more “generic” one and configures it with props.

Props and composition give you all the flexibility you need to customize a component’s look and behavior in an explicit and safe way. 


## Thinking in React

1. Break The UI Into A Component Hierarchy
2. Build A Static Version in React
3. Identify The Minimal (but complete) Representation Of UI State
4. Identify Where Your State Should Live
5. Add Inverse Data Flow

