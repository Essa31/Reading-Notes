# React - Conditional Rendering

In React, you can create distinct components that encapsulate behavior you need. Then, you can render only some of them, depending on the state of your application.

# React - Lists & Keys 

In order to render an array/list of elements, the array method `map()` is used:

ex: 

    const numbers = [1, 2, 3, 4, 5];
    const listItems = numbers.map((number) =>
    <li>{number}</li>
    );

But React needs a key reference for each one of the elments, so thats why we need to add a key to each element:

ex: 

    function NumberList(props) {
        const numbers = props.numbers;
        const listItems = numbers.map((number) =>
            <li key={number.toString()}>
            {number}
            </li>
        );
        return (
            <ul>{listItems}</ul>
        );
    }

# React - Forms
- In React, mutable state is typically kept in the state property of components, and only updated with setState().
- you can use the values inside the forms inputs by targeting their name to get th values 
  - `event.target.name of the element.value`
- Alternatives to Controlled Components
  - It can sometimes be tedious to use controlled components,because you need to write an event handler for every way your data can change and pipe all of the input state through a React component.
  - This can become particularly annoying when you are converting a preexisting codebase to React, or integrating a React application with a non-React library.
  - In these situations, you might want to check out uncontrolled components, an alternative technique for implementing input forms.
- Fully-Fledged Solutions 
  - If you’re looking for a complete solution including validation, keeping track of the visited fields, and handling form submission
  - `Formik` is one of the popular choices. 
    

# React - Lifting State
Often, several components need to reflect the same changing data. We recommend lifting the shared state up to their closest common ancestor. Let’s see how this works in action.

In this section, we will create a temperature calculator that calculates whether the water would boil at a given temperature.

We will start with a component called BoilingVerdict. It accepts the celsius temperature as a prop, and prints whether it is enough to boil the water:

function BoilingVerdict(props) { if (props.celsius >= 100) { return

The water would boil.

; } return

The water would not boil.

; }

 
# React - Composition vs Inheritance

- Containment
  - Some components don’t know their children ahead of time.
  - This is especially common for components like `Sidebar` or `Dialog` that represent generic `boxes`
- Specialization 
  - achieved by composition, where a more “specific” component renders a more “generic” one and configures it with props
- Inheritance
  - Props and composition give you all the flexibility you need to customize a component’s look and behavior in an explicit and safe way.
  - reuse non-UI functionality between components
    - extracting it into a separate JavaScript module
    - The components may import it and use that function, object, or a class, without extending it

# Thinking in React
- Steps : 
  - Break The UI Into A Component Hierarchy 
    - The first thing you’ll want to do is to draw boxes around every component (and subcomponent) in the mock and give them all names.
  - Build A Static Version in React
    - The easiest way is to build a version that takes your data model and renders the UI but has no interactivity.
  - Identify The Minimal (but complete) Representation Of UI State
    - it is the time to think of the minimal set of mutable state that your app needs 
  - Identify Where Your State Should Live
    - dentify which component mutates, or owns, this state
  - Add Inverse Data Flow
    -  support data flowing the other way: the form components deep in the hierarchy need to update the state in `FilterableProductTable`.


## Things I want to know more about

None.

## Resources

[sources1](https://reactjs.org/docs/conditional-rendering.html)

[sources2](https://reactjs.org/docs/lists-and-keys.html)

[sources3](https://reactjs.org/docs/forms.html)

[sources4](https://reactjs.org/docs/lifting-state-up.html)

[sources5](https://reactjs.org/docs/composition-vs-inheritance.html)

[sources6](https://reactjs.org/docs/thinking-in-react.html)

