The three principles here are called the fundamental principles of redux and they describe the **redux** patterns.

1. > The state of your application stored in an object tree within a single store

	Maintain our application state in a single object which would be managed by the redux **store**.
	
2. > The only way to change the state is to emit an action, an object describing what happened

	State is **Read-only**. To update the state of our app, you need to let Redux know about that with in an **action**. We are not allowed to directly update the state.
	
3. > To specify how the state tree is transformed by actions, you write pure reducers

	Reducers are the pure functions that takes the state and the action as input and produces an updated state. To maintain predictability we use [[Pure Functions]]
	
	```js
	Reducer (previousState, action) => newState
	```
	
### Overview

- We have our app and redux store is outside of it.
- Our app is subscribed to redux store always
- we can't directly update the state, instead we dispatch the action and then the reducer updates the store by taking state and action.

	![[Basic Redux Setup.png]]