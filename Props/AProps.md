### 1. What are props in React, and how are they used to pass data between components? Provide a simple example.

In React, "props" (short for properties) are a mechanism for passing data from a parent component to a child component. They allow for the communication and sharing of information between different parts of a React application.

#### Example:

```jsx
// ParentComponent.jsx
import React from 'react';
import ChildComponent from './ChildComponent';

const ParentComponent = () => {
  const dataToPass = "Hello from Parent";

  return (
    <div>
      <ChildComponent passedData={dataToPass} />
    </div>
  );
};

// ChildComponent.jsx
import React from 'react';

const ChildComponent = (props) => {
  return <p>{props.passedData}</p>;
};

export default ChildComponent;
