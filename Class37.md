# ES6 Syntax and Feature Overview 

- ECMAScript 2015, also known as ES6, introduced many changes to JavaScript.

- `let` keyword, which allows for block-scoped variables which cannot be hoisted or redeclared
- `const` keyword, which cannot be redeclared or reassigned, but is not immutable.
- Arrow functions
  - The arrow function expression syntax is a shorter way of creating a function expression
  - Arrow functions do not have their own this, do not have prototypes, cannot be used for constructors, and should not be used as object methods.
- `return` keyword is implied and can be omitted if using arrow functions without a block body.
- `class` syntax on top of the prototype-based constructor function.
- `extends` keyword creates a subclass.

## React

React is a free and open-source front-end JavaScript library for building user interfaces based on UI components. 

### Introducing JSX

**JSX** is a syntax extension to JavaScript, used within **React** to describe how the UI should look like.

**JSX** allows users to embed expressions within markup language. ex:

    const name = 'Mike';
    const element = <h1>Hello, {name}</h1>;

The main reason behind using **JSX** is to combine using markup language and Javascript.

### Some things that React allows us to do:

- **Rendering Elements into DOM**. ex: 

        const root = ReactDOM.createRoot(
            document.getElementById('root')
        );
        const element = <h1>Hello, world</h1>;
        root.render(element);

- **Creating components and props**. ex: 

        function Welcome(props) {
            return <h1>Hello, {props.name}</h1>;
        }

        class Welcome extends React.Component {
            render() {
                return <h1>Hello, {this.props.name}</h1>;
            }
        }



## React - Components & Props
- Components let you split the UI into independent, reusable pieces, and think about each piece in isolation
- The simplest way to define a component is to write a JavaScript function:
- Example
```
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```
- This function is a valid React component because it accepts a single `props`, `(which stands for properties)`
- Class based example
```
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```
- React is pretty flexible but it has a single strict rule:
- **All React components must act like pure functions with respect to their props.**



## React - State & Lifecycle
- we need to add “state” to the `Clock` component
- State is similar to props, but it is private and fully controlled by the component.
- Converting a Function to a Class 
  - Create an ES6 class, with the same name, that extends React.Component.
  - Add a single empty method to it called render().
  - Move the body of the function into the render() method.
  - Replace props with this.props in the render() body.
  - Delete the remaining empty function declaration.
- Using State Correctly 
  - Do Not Modify State Directly
  - State Updates May Be Asynchronous
  - State Updates are Merged
- **Each Clock sets up its own timer and updates independently.**


### React - Handling Events
- Handling events with React elements is very similar to handling events on DOM elements. There are some syntax differences 
  - React events are named using camelCase, rather than lowercase.
  - With JSX you pass a function as the event handler, rather than a string.
- Passing Arguments to Event Handlers
- Example
```
<button onClick={(e) => this.deleteRow(id, e)}>Delete Row</button>
<button onClick={this.deleteRow.bind(this, id)}>Delete Row</button>
```
- The above two lines are equivalent, and use arrow functions and Function.prototype.bind respectively 
- the e argument representing the React event will be passed as a second argument after the ID
- With an arrow function, we have to pass it explicitly, but with bind any further arguments are automatically forwarded.

## Kinds of projects that will get benefits from ReactJS:

Enterprise Web Apps or Large-Scale Projects Web Applications That Require Dynamic Page Updates Complex UI Progressive Web Applications (PWAs) ReactJs is a Facebook-developed framework that is used by over 8000 enterprises. Because of the features that ReactJs provides, even Netflix, Uber, Airbnb, and other large organizations use it for web development. It is one of the greatest JavaScript frameworks and is ranked among the top three. Now that you've decided which firms to hire for the creation of your ReactJs web project, simply click on the link to learn about the top 10 web development companies.



## Next.js

Next.js is an open-source web framework that builts on top of Node.js, for the sole reason of allowing React web applications to do the followig:

* Server-side rendering.
* Generating static websites.

## Things I want to know more about

None.

## Resources

[sources1](https://reactjs.org/docs/introducing-jsx.html)

[sources2](https://reactjs.org/docs/rendering-elements.html)

[sources3](https://reactjs.org/docs/state-and-lifecycle.html)

[sources4](https://nextjs.org/learn/basics/create-nextjs-app)