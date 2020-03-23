# Pros and cons for FP & OOP

## FP

- Many operations on fixed data
- Stateless
- Pure functions: no side effects and always same output given same input
- More declarative
- Separate data and behaviour

Works with many different processes and many operations (parallelism)

## OOP

- Few operations on common state
- Stateful
- Side effects
- More imperative
- Combining data and behaviour

For more self-contained apps like games OOP might make more sense as you have fewer operations (less or no parallelism) and stateful (you know exactly what kind of state you want to create and work with)
