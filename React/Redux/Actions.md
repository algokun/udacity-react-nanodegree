An **action** is nothing but an event that changes in the state of an application

- The actions are the only way your app can interact with the store.
- Carry some information from your app to the redux store
- These are nothing but plain javascript objects
- Have a `type` property to indicate the type of action being done
- The `type` property is typically defined as string constants

Example:

```js
const action = {
  type: ORDER_PIZZA,
  pizza: {
    id: 833121,
    name: "Veg Forest",
    size: "regular",
    toppins: ["cheeze", "mushroom", "corn"],
  },
};
```
