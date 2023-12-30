# Promises

Promises in JavaScript are objects that represent the eventual completion or failure of an asynchronous operation, and its resulting value. They are a way to handle asynchronous operations without blocking the rest of your code.

A Promise is in one of these states:

Pending: The Promise's outcome hasn't yet been determined, because the asynchronous operation that will produce its result hasn't completed yet.
Fulfilled: The asynchronous operation has completed, and the Promise has a resulting value.
Rejected: The asynchronous operation failed, and the Promise will never be fulfilled. In the rejected state, a Promise has a reason that indicates why the operation failed.
Here's a basic example of a Promise:

```jsx
let promise = new Promise(function(resolve, reject) {
  // a mock async action using setTimeout
  setTimeout(function() {
    resolve('Done!');
  }, 1000);
});

promise.then(function(value) {
  console.log(value);
  //=> 'Done!'
});
```

In the above example, new Promise is used to create a new Promise. The Promise constructor takes a function as an argument, and that function takes two parameters: resolve and reject, which are both functions. If the operation was successful, resolve is called with the result. If not, reject is called with an error message. The then method is used to schedule code that will run when the Promise is resolved.
