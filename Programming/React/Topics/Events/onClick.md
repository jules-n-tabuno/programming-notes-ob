#react

==In React, the `onClick` event handler is used to execute a function when an element is clicked. You assign it to an element, like a button, and pass a function that will run when the click occurs. This function can be defined inline or separately.==

**Example:**

`Card.jsx`
```
import React from 'react';

export const Card = ({name}) => {
	const printHello = () => {
		console.log('hello');
	};
	return <div onClick={printHello}>I'm A {name}<div>
}
```

`App.js`
```
import React from 'react';
import {Card} from './Card';

function App() {
	return (
		<div className="App">
			<Card name={`hello bob`} />
		</div>
	);
}

export default App;
```

**Expected Behavior:**

When you click on the rendered card, the `printHello` function will be executed, and "hello" will be logged to the console. The text "I'm A hello bob" will be displayed on the screen.

**Note:** While the `printHello` function is defined, it's not directly used to update the UI. It only logs a message to the console. To update the UI based on the click event, you would typically use state management or other techniques to trigger a re-render with updated content.


**Example 2:**

`Card.jsx`
```
import React from 'react';

export const Card = ({name, onClicked}) => {
	return <div onClick={onClicked}>I'm A {name}<div>
}
```

`App.js`
```
import React from 'react';
import {Card} from './Card';

function App() {
	const onCardClicked = () => {
		console.log('hello');
	}

	return (
		<div className="App">
			<Card name={`hello bob`} onClicked={onCardClicked} />
		</div>
	);
}

export default App;
```

**Expected Behavior:**

When you click on the card, the console will log the message "hello".

**Breakdown:**

1. **Card.jsx:**
    
    - Defines a reusable `Card` component that takes two props:
        - `name`: A string to display on the card.
        - `onClicked`: A function to be called when the card is clicked.
    - Renders a `div` with the provided `name` and an `onClick` handler that triggers the `onClicked` function.
2. **App.js:**
    
    - Defines an `onCardClicked` function that logs "hello" to the console.
    - Renders a `Card` component with the `name` prop set to "hello bob" and the `onClicked` prop set to the `onCardClicked` function.

**When you click the card:**

1. The `onClick` handler in the `Card` component is triggered.
2. This, in turn, calls the `onCardClicked` function passed from `App.js`.
3. The `onCardClicked` function logs "hello" to the console.

**Therefore, you should see "hello" printed in your browser's console when you click the card.**