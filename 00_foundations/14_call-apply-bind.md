# call(), apply(), bind()

## `call()`

Under the hood all functions use `call()` when they run. Every function gets this method attached to it.

## `apply()`

`apply()` does the same thing as `call()`.

## `call(obj, args...)` and `apply(obj, [args...])`

With call and apply you can borrow methods from other objects and "apply" them to an object that does not have that method. You can also pass in extra parameters.

## `bind()`

Also allows us to use other object's methods, but with the difference that bind returns a new function. It basically copies it for later use without calling the function immediately. 

