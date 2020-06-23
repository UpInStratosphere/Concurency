## Synchronous vs Asynchronous 
- synchronization refers to two or more processes' start and end points, NOT their executions. 
  - usually important in multithreading concurrency where multiple threads share the same data, and different threads can both read and write on the data. 

- Synchronous processes need to wait for another process to complete a task before it can starts:

                    SYNCHRONOUS
                    |--------A--------|
                                      |--------B--------|
                                         
- Asynchronous processes do not need to wait:

                    ASYNCHRONOUS
                       |--------A--------|
                             |--------B--------|


