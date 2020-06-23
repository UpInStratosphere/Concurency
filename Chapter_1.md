## 1.1 What is concurrency
- having two or more separate activities happening at the same time
### 1.1.1
- task switching: doing bits of one task then a bit of another. This gives the illusion of concurrency
- even with multicore processor and multiprocessor computing, task switching (hardware threads) in a single core processor is still the most important metric because there are always more tasks running than the hardware can run in parallel.


### 1.1.2 approaches to concurrency
- concurrency with multiple processes
  - divide the application into multiple separate single threaded processes that can be ran at the same time, and separate processes can pass message to each other via comm channels (sockets, files, etc) 
  - safer data access but larger overhead, complicated to set up and slow.
- concurrency with multiple threads
  - run multiple threads of a single process. All threads share the same memory space and most of the data can be accessed directly from all threads.
  - less overhead but more chance of unintentional data change from one thread to corrupt the other threads since there is no protection of the data access by different threads
  - therefore, must ensure that the data accessed by each thread is consistent whenever it is accessed (for example, data accessed by thread A at the *current time* is changed by thread B the moment it is accessed by the thread A. thus, thread A's accessed data state is inconsistent with the real data's state)
  
## 1.2 why use concurrency
### 1.2.1 separation of concerns
- different threads are designed this way because of their purpose is to implement different logic that are unrelated to each other in the process. (example : playing data from DVD and taking in instructions from the remote control)
### 1.2.2. concurrency for performance
- task parallelism
  - different tasks in a single process that are de-coupled from each other - little dependency on each other
- data parallelism
  - classic case of divide and conquer => same operation is performed on different data OR different operations are performed on the same piece of data, and the result of each dataset does not depends on the result of other datasets. Hence no need to and run different threads in sequential manner
  
