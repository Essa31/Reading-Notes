#  Next.js 

## What is Next.js?

Next.js is a flexible React framework that gives you building blocks to create fast web applications.

But what exactly do we mean by this? Let’s spend some time expanding on what React and Next.js are and how they can help.

Building Blocks of a Web Application
There are a few things you need to consider when building modern applications. Such as:

User Interface - how users will consume and interact with your application.

Routing - how users navigate between different parts of your application.
Data Fetching - where your data lives and how to get it.

Rendering - when and where you render static or dynamic content.
Integrations - what third-party services you use (CMS, auth, payments, etc) and how you connect to them.

Infrastructure - where you deploy, store, and run your application code (Serverless, CDN, Edge, etc).

Performance - how to optimize your application for end-users.

Scalability - how your application adapts as your team, data, and traffic grow.

Developer Experience - your team’s experience building and maintaining your application.

For each part of your application, you will need to decide whether you will build a solution yourself or use other tools such as libraries and frameworks.

## What is React?

React is a JavaScript library for building interactive user interfaces.

By user interfaces, we mean the elements that users see and interact with on-screen.


By library, we mean React provides helpful functions to build UI, but leaves it up to the developer where to use those functions in their application.

Part of React’s success is that it is relatively unopinionated about the other aspects of building applications. This has resulted in a flourishing ecosystem of third-party tools and solutions.

It also means, however, that building a complete React application from the ground up requires some effort. Developers need to spend time configuring tools and reinventing solutions for common application requirements.


    

# Take into consideration: 
- Code has to be bundled using a bundler like webpack and transformed using a compiler like Babel.
- You need to do production optimizations such as code splitting.
- You might want to statically pre-render some pages for performance and SEO. You might also want to use server-side rendering or client-side rendering.
- You might have to write some server-side code to connect your React app to your data store.



# built-in features in next.js 
- An intuitive page-based routing system (with support for dynamic routes)
- Pre-rendering, both static generation (SSG) and server-side rendering (SSR) are supported on a per-page basis
- Automatic code splitting for faster page loads
- Client-side routing with optimized prefetching
- Built-in CSS and Sass support, and support for any CSS-in-JS library
- Development environment with Fast Refresh support
- API routes to build API endpoints with Serverless Functions
- Fully extendable
 


# Assets & Metadata & CSS styling 
- Next.js can serve static assets, like images, under the top-level public directory. Files inside public can be referenced from the root of the application similar to pages.
- `title` is part of the `head` HTML tag, so let's dive into how we can modify the `head` tag in a Next.js page 
  - this will help you in the CEO for search engine performance
- CSS modules allow you to locally scope CSS at the component-level by automatically creating unique class names.



# React Context 
It is a method od passing and using any kind of data without using props.

When should you use React context?

It is useful when the passed data is going to be used by any component in the application. Some examples on these kinds of data would be: 

- Theme data( dark/white mode)
- Authenticated user data
- Location specific data




# Props drilling
- is a term to describe when you pass props down multiple levels to a nested component, through components that don't need it.



# How do I use React context? 

Context is an API that is built into React, starting from React version 16.

This means that we can create and use context directly by importing React in any React project.

There are four steps to using React context:

Create context using the createContext method.

Take your created context and wrap the context provider around your component tree.

Put any value you like on your context provider using the value prop.

Read that value within any component by using the context consumer.




# What is the useContext hook ? 

Another way of consuming context became available in React 16.8 with the arrival of React hooks. We can now consume context with the useContext hook.





# React Context VS Redux 
- Redux is a way of more easily passing around data. This is because Redux comes with React context itself. 
- Instead of using render props we can use `React.useContext()`


# WHAT CAN YOU BUILD WITH NEXT.JS?
- With Next.js you can build a number of digital products and interfaces such as:
  - MVP (Minimum Viable Product)
  - Jamstack websites
  - Web Portals
  - Single web pages
  - Static websites
  - SaaS products
  - eCommerce and retail websites
  - Dashboards
  - Complex and demanding web applications
  - Interactive user interfaces

## Things I want to know more about

None.

## Resources

[sources1](https://nextjs.org/learn/basics/getting-started)

[sources2](https://www.freecodecamp.org/news/react-context-for-beginners/)

[sources3](https://www.youtube.com/watch?v=rtgbaKBhdkk)

[sources4](https://www.youtube.com/watch?v=5LrDIWkK_Bc)



