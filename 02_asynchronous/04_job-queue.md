# Job Queue

In order to introduce promises there had to be some modifications to JavaScript engines or how the **Event Loop** worked.

Next to the **Callback Queue** (also known as the **Task Queue**) there had to be another queue: this became the **Job Queue** (or: **Microtask Queue**).

The Job Queue has a higher priority than the Callback Queue because the Event Loop always checks that one first en then the callback queue.
