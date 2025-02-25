Here's the **full code** for each example, including the **main `App.js` file** to render the components properly.

---

### **1. Simple Functional Component with JSX**
#### **File Structure:**
```
/react-app
  ├── src
  │   ├── components
  │   │   ├── Welcome.js
  │   ├── App.js
  │   ├── index.js
  ├── package.json
```

#### **`src/components/Welcome.js`**
```jsx
import React from "react";

const Welcome = () => {
  return <h1>Hello, Welcome to React!</h1>;
};

export default Welcome;
```

#### **`src/App.js`**
```jsx
import React from "react";
import Welcome from "./components/Welcome";

const App = () => {
  return <Welcome />;
};

export default App;
```

#### **`src/index.js`**
```jsx
import React from "react";
import ReactDOM from "react-dom";
import App from "./App";

ReactDOM.render(<App />, document.getElementById("root"));
```

---

### **2. Functional Component with Props**
#### **`src/components/UserGreeting.js`**
```jsx
import React from "react";

const UserGreeting = (props) => {
  return <h2>Hello, {props.name}!</h2>;
};

export default UserGreeting;
```

#### **`src/App.js`**
```jsx
import React from "react";
import UserGreeting from "./components/UserGreeting";

const App = () => {
  return <UserGreeting name="John" />;
};

export default App;
```

---

### **3. Functional Component with Multiple JSX Elements**
#### **`src/components/Profile.js`**
```jsx
import React from "react";

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

#### **`src/App.js`**
```jsx
import React from "react";
import Profile from "./components/Profile";

const App = () => {
  return <Profile />;
};

export default App;
```

---

### **4. Functional Component with Click Event**
#### **`src/components/ClickButton.js`**
```jsx
import React from "react";

const ClickButton = () => {
  const handleClick = () => {
    alert("Button Clicked!");
  };

  return <button onClick={handleClick}>Click Me</button>;
};

export default ClickButton;
```

#### **`src/App.js`**
```jsx
import React from "react";
import ClickButton from "./components/ClickButton";

const App = () => {
  return <ClickButton />;
};

export default App;
```

---

### **5. Functional Component with Conditional Rendering**
#### **`src/components/ShowMessage.js`**
```jsx
import React from "react";

const ShowMessage = ({ isLoggedIn }) => {
  if (isLoggedIn) {
    return <h2>Welcome Back!</h2>;
  } else {
    return <h2>Please Log In</h2>;
  }
};

export default ShowMessage;
```

#### **`src/App.js`**
```jsx
import React from "react";
import ShowMessage from "./components/ShowMessage";

const App = () => {
  return <ShowMessage isLoggedIn={true} />;
};

export default App;
```

---

### **6. Functional Component with List Rendering (`map()`)**
#### **`src/components/FruitsList.js`**
```jsx
import React from "react";

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

#### **`src/App.js`**
```jsx
import React from "react";
import FruitsList from "./components/FruitsList";

const App = () => {
  return <FruitsList />;
};

export default App;
```

---
