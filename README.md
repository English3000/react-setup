# react-setup

__(0)__ Create Project folder. `cd` into it.


__(1a)__ Run `npm init --yes`

__(1b)__ Run `npm install --save webpack react react-dom react-router-dom react-redux redux redux-logger redux-thunk babel-core babel-loader babel-preset-es2015 babel-preset-react`


__(2a)__ Create `webpack.config.js` file: https://github.com/appacademy/curriculum/blob/master/react/readings/webpack_configuration.md#sample-webpackconfigjs

__(2b)__ Create `/frontend` folder,
            `render.jsx` file (or `entry.jsx`),
            `index.html` file.
            
```js
// ./frontend/render.jsx

document.addEventListener('DOMContentLoaded', () => {
  const props = {/*...*/};
  ReactDOM.render(<MyApp props={props}/>, document.getElementById('app-display')); //OR 'root'
});
```

__(2c)__ Put `<script>` tag in `index.html` head.


__(3a)__ Add `"webpack": "webpack --watch"` to `package.json` *"scripts"* object.

__(3b)__ Create `.gitignore` file:
    https://github.com/appacademy/curriculum/blob/master/react/readings/webpack_configuration.md#gitignore


__(4a)__ Run `npm run webpack`

__(4b)__ Open `index.html` to confirm setup success!


__(5a)__ Create `/css` folder,
            `reset.css` file--
    https://github.com/appacademy/curriculum/blob/master/html-css/micro-projects/css-friends/css-friends-00/solution/css/00-reset.css
      --and `index.css` file.

__(5b)__ Put `<link>` tags in `index.html`


__(6a)__ Create parent (`app.jsx`) &
          children `{component}.jsx` files in `/frontend` folder.

__(6b)__ Skeleton each component.

```js
// ./frontend/my_app.jsx

import React from 'react';
import Child1 from './child1';

export default class MyApp extends React.Component {
  constructor(props) {
    super(props);
    this.state = {};
  }
  render() {
    return (
      <div>
        <Child1 props />
      </div>
    );
  }
  changeState() {
    this.setState({attr: new Value()});
  }
}
```

OR *as Functional Component:*

```js
export default const MyApp = () => (
  <div>
    <Child1 props />
  </div>
);
```

__(6c)__ Style each component's `<div>` (`.{component}-div`) & elements in `index.css`

__(6d)__ Code away!
