A **reducer** which actually ties the state and actions together.
- Reducers specify how the app's state changes in response to actions sent to the store.
- It will take the state and action to perform and return us new state.
- (previousState, action) => newState

Example:
```js

const placePizzaOrder = (previousState, action) => {
  switch (action.type) {
    case ORDER_PIZZA:
      return Object.assign({}, previousState, {
        pizzaCount: previousState.pizzaCount - 1,
      });

    default:
      return previousState;
  }
};

```

### How to use Multiple Reducers?

1. Create two reducers for one state object or for two seperate state objects (Note: The store has both the state objects combined)
2. Let's say i have a reducer `placePizzaOrder` for placing pizza order and `placeCokeOrder` for placing coke order.
3. Create a root reducer by using `combineReducers`

Example : 

```js

const rootReducer = combineReducers({
	pizza : placePizzaOrder,
	coke : placeCokeOrder
});

```