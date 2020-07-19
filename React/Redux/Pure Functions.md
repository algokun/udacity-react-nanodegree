### What are Pure Functions?
Pure functions are integral to how state in **Redux** applications is updated. By definition, pure functions:

- Return the same result if the same arguments are passed in
- Depend solely on the arguments passed into them
- Do not produce side effects, such as API requests and I/O operations

### Why Pure Functions Are Great
For our purposes, the most important feature of a pure function is that it's **predictable**. If we have a function that takes in our state and an action that occurred, the function should (if it's pure!) return the exact same result every single time.

You're going to be sick of this by the end ;-) but this course (and Redux!) are all about predictability!