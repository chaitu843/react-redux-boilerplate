========================================================================================================================================================================

## Simple Steps to go on with your application --

1. Create your initial state structure in src/store.js

2. Create the required reducers in src/Reducers and combiner them in src/Reducers/index

3. Inorder to trigger an action based on an event from the component,

    1. Declare the action type in src/actions/types.js
    2. Now define a function in src/actions/actions.js which will do the required operations and finally dispatch the action to the store
    3. Now add a case in relevant reducer inorder to manipulate state
    4. Now pass the actionHandler to your component js using connect, and then call the function through component props on user's choice (Event triggering, etc..)

========================================================================================================================================================================
### Creating a React-Redux template

## Steps Involved -->

1. Create the React app using create-react-app

2. Install dependencies required for Redux
 
   redux --> Redux Library
   react-redux --> To use redux with react
   redux-thunk --> Middleware function from redux ( helps in using dispatch function from event handlers)

3. Folder Structure

   src/Components --> All React Components
   src/store.js --> the whole application level store
   src/Actions --> types.js and actions.js
   src/Reducers --> index.js and {reducerName}.js as required

========================================================================================================================================================================

## Functionalities handled by Individual files

# store.js
    Creates Store using redux while supplying state, reducer functions and middleware required

# Actions/types.js
    Contains constants describes types of actions which are to be dispatched

# Actions/actions.js
    Contains all the action dispatchers which are to be triggered upon any events as per user choice

# Reducers/index.js
    Import all the other reducer functions and combine them using combineReducers as required

# Reducers/{reducerName}.js
    Contains the reducer function regarding to a specific part of state as per user's choice

========================================================================================================================================================================
    Store with initialState,

    Action dispatchers and

    Reducers are Ready
========================================================================================================================================================================

## Enabling Redux Dev tools chrome extension

1. Need to add this as a Middleware while creating store inorder for Redux dev tools to work

compose(
        applyMiddleware(...middleware),
        window.__REDUX_DEVTOOLS_EXTENSION__ && window.__REDUX_DEVTOOLS_EXTENSION__()
    )

Just use this enhancer while creating a store which helps us in adding chrome dev tools and thunk

========================================================================================================================================================================

## Integrating Reducers and Store with our application (steps) --

1. Import the Store and provide it to the parent Element using Provided component provided by react-redux

2. Connect the state and actionDispatchers to the respective components --> connect from 'react-redux' helps in doing so

3. Mention a function which convert state to compoonent props and also the action dispatchers required while using connect
    --> outcome state and action dispatchers are available as component props

========================================================================================================================================================================

========================================================================================================================================================================

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br>
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br>
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.<br>
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br>
Your app is ready to be deployed!
