#react 

==Props, short for properties, allow data to be passed from one component to another in React. They enable a parent component to pass information to its child components, which is crucial for dynamic application behavior. Understanding how to manipulate and use props is essential for rendering interactive UIs.==

**Example:**

`Card.jsx`
```
import React from 'react';

export const Card = (props) => {
	return <div>I'm A {props.name}</div>;
}
```

`App.js`
```
import React from 'react';
import { Card } from './Card';

function App() {
	return (
		<div className="App">
			<Card name="hello" />
		</div>
	);
}
```

**RESULT:**
==I'm A hello==

# Props Object Deconstruction

==Object destructuring in React props allows you to extract specific properties directly within the function's parameter list, making the code cleaner and more readable.==


**Example:**

`Card.jsx`
```
import React from 'react';

export const Card = ({name}) => {
	return <div>I'm A {name}</div>;
}
```

`App.js`
```
import React from 'react';
import { Card } from './Card';

function App() {
	return (
		<div className="App">
			<Card name={`hello bob`} />
		</div>
	);
}
```

**RESULT:**
==I'm A hello bob==

