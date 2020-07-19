The three core concepts of redux are:
- [[Store]]
- [[Actions]]
- [[Reducers]]

## Example

Imagine you went to domino's and you were to order pizza and here is the complete scenario

### Entities
- Pizza Shop
	- Stores pizza on the shelf
- The Guy who serves pizza
	- waiting for you to serve an order
- Customer
	- Yeah its you

### Activities
- Customer
	- Buy a Pizza
- The Pizza guy
	- Serves an order for you by removing it from the shop
	- Gives you receipt of the order

| Pizza Shop Scenario | Redux   | Purpose                                |
| ------------------- | ------- | -------------------------------------- |
| Shop                | Store   | Holds the state of your application    |
| Buy a pizza         | Action  | Describes what has happened - an event |
| The Pizza guy       | Reducer | Ties the store and actions together    |

### Summary
- A **store** that holds the state of your entire application
- An **action** is nothing but an event that  changes in the state of an application
- A **reducer** which actually ties the state and actions together, in other words it will take the state and action to perform and return us new state.