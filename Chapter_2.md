## Basic Thread Management

### waiting for thread to complete
- call .join() function 
- this ensures that the thread containing the current process will not terminate until the waited thread is finished

### running threads in the background 
- call .detach() function right after a thread is created to prevent forgetting to deal with the thread later
- once a thread is detached, there is no way to refer back to this thread 
