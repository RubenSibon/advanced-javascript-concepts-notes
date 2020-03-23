# Immutability

The principle to only mutate state when absolutely necessary. Most of the time it would be better to clone or return something new.

This could be memory inefficient at scale. That is why with FP architects ofthen choose to do **structural sharing**: only clone the parts of the data that have changed.

Next to do that memory is cheap these days, so using a bit more memory with the great benefits is not a bad tradeoff.
