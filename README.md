## Counter Lab
_Introduction_
In this lab, you will build a react app that includes a clich handler, a button, and a piece of mutable state.


### Deliberable
The finished app will include a welcome message, a Number `counter` value, and a button for incrementing the counter.  Time permitting, write simple styles for the app


### Set up
- Initialize a new React project: `create-react-app clicker`
- `cd` into `clicker` and remove the boilerplate inside `App.js`
- create a `components` directory under `src`
- run `npm start` and verify that the app opens in the browser

### A Welcome Component
- To get warmed up, make a `Welcome` component inside the `components` directory.  Make sure to put it inside a file called `Welcome.jsx`
- The `Welcome` component should have a background, a font-family other than the default, and a welcome message for the app.  Perhaps `The Counter App`
- export the component at the bottom of `Welcome.jsx` and import it inside `App.js`
- Add the `Welcome` component to the jsx within the `render` method of `App.js`
- Verify that the component displays in the browser

### The Button
- Add a button to the jsx inside the `App` component's `render` method that has a value `Increment Counter`
- Write a method `incrementCounter` inside `App` that, for now, just `console.log`'s a helpful message
- Add a `constructor` method to the `App` component and call `super()` at the top of the method
- At the bottom of the `constructor` method, `bind` `incrementCounter`.
- Lastly, pass `incrementCounter` as the value of `oncClick` for the `button`

At this point, you should be able to click the button and see the helpful message from before appear in the console

### The Counter State Variable
- inside the `constructor` method in the `App` component, initialize a state object with a single key `counter` with an initial value of `0`
- inside `incrementCounter`, `console.log` `this.state.counter`
- also inside `incrementCounter` use `setState` to increment the counter variable by 1.  Don't forget to use the `prevState` pattern since the new value of `counter` depends on the previous value.

At this point, if you click on the button, you should see the value of `counter` increase with every click.

### The Counter Component
- Add a `Counter` inside `components`
- `Counter` should take a single prop, `counterValue` and display it
- import the `Counter` component inside `App.js`
- Add the `Counter` component to the `render` method of the `App` component, and pass it `this.state.counter` as the value of the `counterValue` prop
- Remove the `console.log` statement from `incrementCounter`

Now, you should be able to click the button, and see the counter change as it is displayed from the `Counter` component


#### Bonus

Style everything like a boss