 ==Functional components are the fundamental building blocks of React applications. Unlike class components, functional components are simpler and allow the use of hooks for managing state and lifecycle methods. Each component is essentially a JavaScript function that returns JSX, making applications modular and maintainable.==


**Example:**

`Card.jsx`
```
import React from 'react';

export const Card = () => {
	return <div>I'm a CARD</div>;
};
```

Import the `Card.jsx` component into `App.js`

`App.js`
```
import React from 'react';
import { Card } from './Card';

function App() {
	return (
		<div className="App">
			<Card />
		</div>
	);
}
```