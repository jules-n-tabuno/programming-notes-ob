#react

==In React, the `onChange` event handler is a crucial tool for managing user input in form elements. It triggers whenever the value of an input element changes, allowing you to capture and update state or perform other actions based on the user's input.==

`onChange = event handler used primarily with form elements. Example: <input>, <textarea>, <select>, <radio>. Triggers a function every time the value of the input changes.`

**Example:**

`MyComponent.jsx`
```
import React, {useState} from 'react';

function MyComponent() {
	const [name, setName] = useState("Guest");
	const [quantity, setQuantity] = useState(1);

	function handleNameChange(event) {
		setName(event.target.value);
	}

	function handleQuantityChange(event) {
		setQuantity(event.target.value);
	}

	return (<div>
		<input value={name} onChange={handleNameChange} />
		<p>Name: {name}</p>

		<input value={quantity} onChange={handleQuantityChange} type="number" />
		<p>Quantity: {quantity}</p>
	</div>)
}
export default MyComponent
```

**Expected Output:**

When you run this code, you'll see a user interface with:

- An input field initially displaying "Guest".
- A paragraph below it saying "Name: Guest".
- A number input field displaying "1".
- A paragraph below it saying "Quantity: 1".

**Interaction:**

- As you type in the name input field, the `handleNameChange` function gets triggered continuously, updating the `name` state and reflecting the changes in the UI (both the input field and the paragraph).
- Similarly, when you change the value in the quantity input field, the `handleQuantityChange` function updates the `quantity` state, and the UI displays the new selected quantity.

This component demonstrates a common pattern in React applications where user input is captured, managed in state, and reflected in the UI for a dynamic user experience.