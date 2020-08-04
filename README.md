# Concurency
- how to maintain data integrity while having multliple threads/processes that shares common access to the shared resources 
  - Thread synchronization is defined as a mechanism which ensures that two or more concurrent processes or threads do not simultaneously execute some particular program segment known as critical section. 
  - Processes' access to critical section is controlled by using synchronization techniques. When one thread starts executing the critical section (serialized segment of the program) the other thread should wait until the first thread finishes. 
  - If proper synchronization techniques are not applied, it may cause a **race condition** where the values of variables may be unpredictable and vary depending on the **timings of context switches** of the processes or threads.

## synchronization
- Process synchronization
  - refers to the idea that multiple processes are to join up or handshake at a certain point, in order to reach an agreement or commit to a certain sequence of action.
- Data synchronization 
  - refers to the idea of keeping multiple copies of a dataset in coherence with one another, or to maintain data integrity
  
