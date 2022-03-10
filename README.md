
# React--Robofriends

This project is fully a react project where its fundaments such as ```components, props and its css``` and others linked are shown

## Demo

## Features

- Making of React components.
- Use of state related with props and others recently learned techniques such as destructuring and others.

## Lessons Learned

Few of the lessons learned are, how to start react app, the alerts it gives and how to break components and the use of props.

1. In index.js I changed the App.js to any other components I needed like the Card.js
2. I created the structure of Card.js & provided its HTML structure, these structure could be Hard coded but later on changed dynamic as per the properties passed in index.js which came from robots.js.
3. The respective Card.js will have its styling as well.
4. Then in index.js I came and passed the properties, and imported from robots.js and showed then per array values.
5. Same props need to pass into card.js with destrutring method to use them in this case and makes our life easier.

```
// Card.js
import React from 'react';

const Card = (props) => {
  const { name, email, id } = props
  return (
    <div className='tc bg-light-green dib br3 pa3 ma2 grow bw2 shadow-5'>
      <img src={`https://robohash.org/${id}?size=200x200`} alt='robots' />
      <div>
        <h2>{name}</h2>
        <p>{email}</p>
      </div>
    </div >


  )
};


export default Card;



// Index.js
import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import Card from './Card';
import 'tachyons';
import reportWebVitals from './reportWebVitals';
import { robots } from "./robots"

ReactDOM.render(
  <React.StrictMode>
    <div>
      <Card id={robots[0].id} name={robots[0].name} email={robots[0].email} />
      <Card id={robots[1].id} name={robots[1].name} email={robots[1].email} />
      <Card id={robots[2].id} name={robots[2].name} email={robots[2].email} />
    </div>
  </React.StrictMode>,
  document.getElementById('root')
);

// If you want to start measuring performance in your app, pass a function
// to log results (for example: reportWebVitals(console.log))
// or send to an analytics endpoint. Learn more: https://bit.ly/CRA-vitals
reportWebVitals();
```
### Stateless Functional Component
There are two ways to create a React component. The first way is to use a JavaScript ```function another is class Component```. Defining a component in this way creates a stateless functional component. The concept of state in an application will be covered in later challenges. For now, think of a stateless component as one that can receive data and render it, but does not manage or track changes to that data. 
To create a component with a function, you simply write a JavaScript function that returns either JSX
One important thing to note is that React 

```
const DemoComponent = function() {
  return (
    <div className='customClass' />
  );
};
```

### Class Components:
The other way to define a React component is with the ES6 class syntax. In the following example, Kitten extends React.Component:
```
class Kitten extends React.Component {
  constructor(props) {
    super(props);
  }

  render() {
    return (
      <h1>Hi</h1>
    );
  }
}
```
This creates an ES6 class Kitten which extends the React.Component class. So the Kitten class now has access to many useful React features, such as local state and lifecycle hooks. Don't worry if you aren't familiar with these terms yet, they will be covered in greater detail in later challenges. Also notice the Kitten class has a constructor defined within it that calls super(). It uses super() to call the constructor of the parent class, in this case React.Component. The constructor is a special method used during the initialization of objects that are created with the class keyword. It is best practice to call a component's constructor with super, and pass props to both. This makes sure the component is initialized properly. For now, know that it is standard for this code to be included. Soon you will see other uses for the constructor as well as props.

#### Parent & Child Component:

```
const ChildComponent = () => {
  return (
    <div>
      <p>I am the child</p>
    </div>
  );
};

class ParentComponent extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h1>I am the parent</h1>
        { /* Change code below this line */ }
<ChildComponent/>

        { /* Change code above this line */ }
      </div>
    );
  }
};
```
Rendering ES6 style class components within other components is no different than rendering the simple stateless functions components 

A full Funtional Componets also including the Render Method: 

```
class TypesOfFood extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h1>Types of Food:</h1>
        {/* Change code below this line */}
<Fruits />
<Vegetables />
        {/* Change code above this line */}
      </div>
    );
  }
};

// Change code below this line
ReactDOM.render(<TypesOfFood />, document.getElementById("challenge-node"));
```

### Props 

### State and its different features




## Optimizations


## Screenshots



## Tech Stack

**Client:** React, JS, CSS

## Documentation


# Notes 

