### Folder Structure
Follow - Feature based or redux concept based

### Steps
1. Define `ActionCreators` in a seperate file.
2. Create Action Constants in a file and export it.
3. Create Reducers for the actions
4. Create Redux Store - `createStore()`
5. Pass the store to the root component using `Provider`

### Usage of Connect

To access the store and dispatch the actions, you need `connect()` from **react-redux.**
1. create a method `mapStateToProps` that will take the `state` and return the object with the selectors you need.
2. create a method `mapDispatchToProps` that will take dispatch and return an object with multiple dispatches you want to use,
3. Finally connect the both `mapStateToProps` and `mapDispatchToProps` with `connect` and access using props.

Example:
	
```js
import React from 'react'
import { connect } from 'react-redux'
import { buyCake } from '../redux'

// actual component
function CakeContainer (props) {
  return (
    <div>
      <h2>Number of cakes - {props.numOfCakes} </h2>
      <button onClick={props.buyCake}>Buy Cake</button>
    </div>
  )
}

// access the state using props
const mapStateToProps = state => {
  return {
    numOfCakes: state.cake.numOfCakes
  }
}

// access dispatchers using props
const mapDispatchToProps = dispatch => {
  return {
    buyCake: () => dispatch(buyCake())
  }
}

// connect redux store with component
export default connect(
  mapStateToProps,
  mapDispatchToProps
)(CakeContainer)

```