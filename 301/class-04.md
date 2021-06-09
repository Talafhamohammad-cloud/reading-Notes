## What is a ‘Controlled Component’?

In React, mutable state is typically kept in the state property of components, and only updated with setState(). We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a “controlled component”.

## Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why

Since the value attribute is set on our form element, the displayed value will always be this.state.value, making the React state the source of truth. Since handleChange runs on every keystroke to update the React state, the displayed value will update as the user types.

With a controlled component, the input’s value is always driven by the React state. While this means you have to type a bit more code, you can now pass the value to other UI elements too, or reset it from other event handlers.

## How do we target what the user is entering if we have an event handler on an input field?

If you’re looking for a complete solution including validation, keeping track of the visited fields, and handling form submission, Formik is one of the popular choices. However, it is built on the same principles of controlled components and managing state.

*-------------------------------------------------------------------*

## Why would we use a ternary operator?

Shorten your if statements into one line of code with the conditional operator

## Rewrite the following statement using a ternary statement

  if(x===y){
 console.log(true);
  } else {
 console.log(false);
  }

  ***sol: x===y ? console.log(true) : console.log(false)***
