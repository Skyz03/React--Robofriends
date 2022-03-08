
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


## Optimizations


## Screenshots

![image](https://user-images.githubusercontent.com/42742924/152200433-95c274ce-328b-4eeb-baf6-0d4b4cfff5ff.png)


## Tech Stack

**Client:** React, JS, CSS

## Documentation


# Notes 

