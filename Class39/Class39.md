# Readings: React 3

## Assets, Metadata, and CSS

### Assets

Next.js can serve static assets, like images, under the top-level public directory. Files inside public can be referenced from the root of the application similar to pages.

Next.js also has support for Image Optimization by default. This allows for resizing, optimizing, and serving images in modern formats like WebP when the browser supports it. This avoids shipping large images to devices with a smaller viewport. It also allows Next.js to automatically adopt future image formats and serve them to browsers that support those formats.
Automatic Image Optimization works with any image source. Even if the image is hosted by an external data source, like a CMS, it can still be optimized.

Instead of optimizing images at build time, Next.js optimizes images on-demand, as users request them. Unlike static site generators and static-only solutions, your build times aren't increased, whether shipping 10 images or 10 million images.

Images are lazy loaded by default. That means your page speed isn't penalized for images outside the viewport. Images load as they are scrolled into viewport.

Images are always rendered in such a way as to avoid Cumulative Layout Shift, a Core Web Vital that Google is going to use in search ranking.

### Metadata

Third-party JavaScript refers to any scripts that are added from a third-party source. Usually, third-party scripts are included in order to introduce newer functionality into a site that does not need to be written from scratch, such as analytics, ads, and customer support widgets.

next/script is an extension of the HTML ```<script>``` element and optimizes when additional scripts are fetched and executed.

### CSS Styling

CSS modules allow you to locally scope CSS at the component-level by automatically creating unique class names. This allows you to use the same CSS class name in different files without worrying about class name collisions.

In addition to CSS modules, you can style your Next.js application in a variety of ways, including:

- Sass which allows you to import .css and .scss files.
- PostCSS libraries like Tailwind CSS.
- CSS-in-JS libraries such as styled-jsx, styled-components, and emotion


## React Context for Beginners

React context is an essential tool for every React developer to know.

> What is React context?

React context allows us to pass down and use (consume) data in whatever component we need in our React app without using props.

In other words, React context allows us to share data (state) across our components more easily.

> When should you use React context?

React context is great when you are passing data that can be used in any component in your application.

- Theme data (like dark or light mode)
- User data (the currently authenticated user)
- Location-specific data (like user language or locale)

Data should be placed on React context that does not need to be updated often.

Why? Because context was not made as an entire state management system. It was made to make consuming data easier.

> What problems does React context solve?

React context helps us avoid the problem of props drilling.

Props drilling is a term to describe when you pass props down multiple levels to a nested component, through components that don't need it.

> How do I use React context?

Context is an API that is built into React, starting from React version 16.

This means that we can create and use context directly by importing React in any React project.

There are four steps to using React context:

1. Create context using the createContext method.
2. Take your created context and wrap the context provider around your component tree.
3. Put any value you like on your context provider using the value prop.
4. Read that value within any component by using the context consumer.

> What is the useContext hook?

Instead of using render props, we can pass the entire context object to ```React.useContext()``` to consume context at the top of our component.

The benefit of the useContext hook is that it makes our components more concise and allows us to create our own custom hooks.

You can either use the consumer component directly or the useContext hook, depending on which pattern you prefer.

> You may not need context

If possible, we want to avoid passing multiple props through components that don't need it.

Instead of immediately resorting to context because we are prop drilling, we should better compose our components.

> Does React context replace Redux?

For many React beginners, Redux is a way of more easily passing around data. This is because Redux comes with React context itself.

However, if you are not also updating state, but merely passing it down your component tree, you do not need a global state management library like Redux.

> React context caveats

While it is possible to combine React context with a hook like useReducer and create a makeshift state management library without any third-party library, it is generally not recommended for performance reasons.

The issue with this approach lies in the way that React context triggers a re-render.

If you are passing down an object on your React context provider and any property on it updates, what happens? Any component which consumes that context will re-render.

This may not be a performance issue in smaller apps with few state values that are not updated very often (such as theme data). But it is a problem if you will be performing many state updates in an application with a lot of components in your component tree.


