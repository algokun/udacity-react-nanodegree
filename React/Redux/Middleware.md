Middleware in redux helps us to extend redux by adding custom functionality.
- It provides a third-party extension point between dispatching an action and the moment it reaches the reducer.
- We can use Middleware for
	- Logging
	- Crash Reporting
	- Performing Asynchronous Tasks

1. Import your middleware
2. Pass it to the store -- with `applyMiddleware()`
3. It'll take care of everything

Refer
[[Thunk]]