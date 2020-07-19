Redux is a predictable state container for your javascript applications.

- State Container
	**Redux** stores the *state of your application*
	The state of the application simply means state of entire individual components of an application.
- Predictable
	In **redux** the state of your application is predictable, because you can track all the state **transitions** 
	
### Problem with default state management
Imagine a component tree of our application and it might look something like this.

![[Component Tree.png]]

If any two siblings want to share state, we need to lift the state to their parent component and if all the siblings, needs a shared state -- we need to **lift** the whole state to app component and pass it down to the components as **props**.

So to avoid this **redux** helps us to store the state of our entire application **outside** and allows every component interact with it.

## Agenda

- [[Core concepts]]
	Store, Actions and Reducers
- [[Three Principles]]
	Fundamental Principles to describe the redux patterns
- [[Middleware]]
	Extending Redux with custom functionality 
- [[ReactRedux]]
	Combining react and redux.