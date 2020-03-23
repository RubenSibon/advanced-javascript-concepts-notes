# Idempotence

Given the same input a functions always return the same output.

Functions with `Math.random()` can never be idempotent for example.

Also deleting an entry from a database cannot be idempotent, because you can not delete the same entry again. The function will not give the same result.
