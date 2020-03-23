# Pure functions

A **pure function** has the following characteristics:

- Given the same input you always get the same output;
- There are no side effects.

The first principle is also called **referential transparency** or **idempotency**.

Not everthing can be pure in the philosophical sense that something pure will not do anything: there is no affect on the outside world. Somewhere, somehow you want/need to have side effects in order to change something in the "outside world".

The idea of pure functions is however that you minimize and cluster the area's where your code has side effects and is thus "tightly coupled" with data and views.
