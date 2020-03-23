# Parallel, Sequence and Race

## Parallel: `.all()`

Create **parallel** promises that returns once all promises have been fulfilled. The promises are all called at the same time (in parallel).

## Race: `.race()`

The first promise in a set/array that returns something wins.

## Sequence `await` each promise

In sequences each promise cannot be called until the previous one has been fulfilled. Therefore it would take longer than parallel if they call the same promises.
