## **1. Simple Functional Component with JSX**
```jsx
import React from "react";

const Welcome = () => {
  return <h1>Hello, Welcome to React!</h1>;
};

export default Welcome;
```
> **Explanation:**  
- A simple **functional component** named `Welcome`.  
- It returns **JSX** containing an `<h1>` element.

---

## **2. Functional Component with Props**
Props allow passing data to a component.

```jsx
const UserGreeting = (props) => {
  return <h2>Hello, {props.name}!</h2>;
};

const App = () => {
  return <UserGreeting name="John" />;
};

export default App;
```
> **Explanation:**  
- `UserGreeting` takes `props.name` and displays a greeting.  
- `App` component passes `"John"` as the prop value.

---

## **3. Functional Component with Multiple JSX Elements**
Using **React Fragments (`<> </>`)** to return multiple elements.

```jsx
const Profile = () => {
  return (
    <>
      <h1>John Doe</h1>
      <p>Software Developer</p>
    </>
  );
};

export default Profile;
```
> **Explanation:**  
- Instead of wrapping elements in a `<div>`, we use `<> </>` (React Fragment).  
- This helps prevent unnecessary extra elements in the DOM.

---

## **4. Functional Component with Click Event**
Handling events inside a functional component.

```jsx
const ClickButton = () => {
  const handleClick = () => {
    alert("Button Clicked!");
  };

  return <button onClick={handleClick}>Click Me</button>;
};

export default ClickButton;
```
> **Explanation:**  
- `onClick` triggers `handleClick()`, which shows an alert when the button is clicked.

---

## **5. Functional Component with Conditional Rendering**
Rendering content based on conditions.

```jsx
const ShowMessage = ({ isLoggedIn }) => {
  return <h2>{isLoggedIn ? "Welcome Back!" : "Please Log In"}</h2>;
};

export default ShowMessage;
```
> **Explanation:**  
- Uses a **ternary operator** to display different messages based on `isLoggedIn`.

---

## **6. Functional Component with List Rendering (`map()`)**
Rendering an array of items.

```jsx
const FruitsList = () => {
  const fruits = ["Apple", "Banana", "Cherry"];

  return (
    <ul>
      {fruits.map((fruit, index) => (
        <li key={index}>{fruit}</li>
      ))}
    </ul>
  );
};

export default FruitsList;
```
> **Explanation:**  
- The `map()` function dynamically generates a list of fruits.

---
