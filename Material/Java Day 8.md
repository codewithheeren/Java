## OOPS Day 8

 @author Heeren

 **Topics Covered**
--------------
- What is Process and What is Thread and Their Differences?
- What is Multithreading?
- What is the Advantage of Multithreading?
- How Many Ways Can We Create a Thread?
- Which Approach is Better?
- Can We Run the Same Thread Twice?
- What is Thread Priority?
- What is Thread Life Cycle?
- What is the Use of Join Method?
- What is the Use of Yield Method?
- What is Deadlock?
- What is Thread Scheduler in Java?
- What is the Difference Between start() and run() Method Call?
- Can We Overload run() Method?
- What Will Happen if We Don’t Override the Thread Class run() Method?
- Can We Override start() Method of Thread Class?
- What Happens When We Call run() Method Explicitly?
- SINGLETON DESIGN PATTERN
- Synchronization
- Method Synchronization
- Synchronized Block
- Can a Thread Acquire Multiple Locks Simultaneously?
- Wait() Method
- Difference Between User Thread and Daemon Thread
- Calling the run() Method of a Thread Class
- Ensuring main() is the Last Thread to Finish in Java Program
- Why Thread sleep() and yield() Methods are Static?
- Inter Thread Communication
- wait, notify, and notifyAll Methods
- Difference Between wait() and sleep() Method
- Difference Between notify() and notifyAll() Methods
- Volatile Keyword
- Executor Framework
- Thread Pool
- Difference between Callable and Runnable Interface
- When Do You Get InterruptedException?
---

### Multithreading

**What is Process and What is Thread and Their Differences?**

- **Process**: A process is an executing instance of a program. 
  
- **Thread**: A thread is a lightweight process within a process. Threads share the same memory space and resources of the process they belong to. Multiple threads can exist within a single process and share the process's data.

**What is Multithreading?**

- Multithreading is a programming concept where multiple threads within a single process execute independently and concurrently. It allows concurrent execution of tasks to utilize CPU time effectively.

**What is the Advantage of Multithreading?**

- **Concurrency**: Multiple tasks can be performed simultaneously, improving overall performance and responsiveness.
- **Resource Sharing**: Threads within the same process can share resources like memory, data, and files.
- **Efficiency**: Utilizes CPU time efficiently by minimizing idle time.

**How Many Ways Can We Create a Thread?**

- Threads can be created in Java by extending the `Thread` class or implementing the `Runnable` interface.

**Which Approach is Better?**

- Implementing the `Runnable` interface is often preferred as it separates the thread's behavior from the class hierarchy, allowing for better design flexibility.

**Can We Run the Same Thread Twice?**

- No, a thread cannot be started (run) more than once. Attempting to start a thread that has already been started will result in a `java.lang.IllegalThreadStateException`.

**What is Thread Priority?**

- Thread priority determines the order in which threads are scheduled for execution by the thread scheduler.

**What is Thread Priority?**

- Thread scheduler schedules the threads according to their priority.
- We have 3 priorities:
  - `MAX_PRIORITY`: Highest priority (value of 10).
  - `NORM_PRIORITY`: Normal priority (default, value of 5).
  - `MIN_PRIORITY`: Lowest priority (value of 1).
- `setPriority()` method is used to set the priority for a thread (e.g., `thread.setPriority(10)`).
- Priority values range from 1 to 10.
- By default, every thread has normal priority.
- Priority must be set before calling the `start()` method.
- The main thread also has a default normal priority.

**What is Thread Life Cycle?**

- The thread life cycle represents various states a thread can be in, including new, runnable, blocked, waiting, timed waiting, and terminated.
  
  ![lifecycle](https://github.com/codewithheeren/Java/assets/87074236/2e296a71-1cc2-4d7b-8b61-6e3671dd36e7)

1. **New**: Thread is created.
2. **Runnable**: Thread is ready to run but not yet scheduled.
3. **Running**: Thread is executing (`run()` method is executing).
4. **Waiting (Block State)**: Thread is waiting state for another thread (using sleep() or wait() method).
6. **Terminated**: Thread completes its execution.


**What is the Use of Join Method?**

- The `join()` method is used to wait for a thread to complete its execution before proceeding with the current thread.
- The current thread pauses and waits for the specified thread to finish.

**What is the Use of Yield Method?**

- The `yield()` method allows the currently executing thread to pause temporarily and give a chance to other waiting threads of the same priority to execute.
- If no waiting threads or all waiting threads have lower priority, the same thread continues execution.

**What is Deadlock?**

- Deadlock is a situation where a set of processes are blocked because each process is holding a resource and waiting for another resource held by some other process, resulting in a circular waiting condition.

**What is Thread Scheduler in Java?**

- The thread scheduler is responsible for determining which threads should run, pause, or resume execution based on thread priorities and states.

**What is the Difference Between start() and run() Method Call?**

- `start()`: Used to start a new thread and execute its `run()` method asynchronously.
- `run()`: Defines the entry point for the thread's execution. It's called when `start()` is invoked or can be called directly, but this runs synchronously in the current thread.

**Can We Overload `run()` Method?**

- Yes, we can overload the `run()` method, but the original `run()` method of `Thread` class must be overridden to provide the custom behavior.

**What Will Happen if We Don’t Override the Thread Class run() Method?**

- If the `run()` method is not overridden, the `Thread` class's default `run()` method will be executed, which does nothing.

**Can We Override start() Method of Thread Class?**

- No, we should not override the `start()` method of the `Thread` class as it's responsible for starting a new thread and performing necessary actions.

**What Happens When We Call run() Method Explicitly?**

- Calling `run()` method explicitly will execute the `run()` method synchronously in the current thread, without starting a new thread.

**SINGLETON DESIGN PATTERN**

- Ensures that only one instance of a class is created.

**Synchronization**

- `Synchronized` keyword is used to define a method or block as synchronized.
- A synchronized method or block allows only one thread to operate on the given object at a time.
- It prevents data inconsistency problems.
- JVM manages acquiring and releasing locks automatically.
- Lock is acquired when a synchronized method or block starts executing and released when it completes its execution.
- Multiple synchronized methods cannot execute concurrently if they are called for the same object lock.

**Method Synchronization**

- **Object Level Lock**:
  - Every object in Java has a unique lock.
  - When using `synchronized` keyword, the lock concept comes into play.
  - If a thread wants to execute a synchronized method on a given object, it first needs to acquire the lock of that object.
  - Once the thread acquires the lock, it can execute any synchronized method on that object.
  - Lock is released automatically after method execution completes.

- **Static Synchronization (Class Level Lock)**:
  - Every class in Java has a unique lock (class level lock).
  - If a thread wants to execute a static synchronized method, it requires the class level lock of that class.
  - Thread acquiring the class level lock cannot execute any other static synchronized method of that class until it releases the lock after method execution.

**Synchronized Block vs Method**
- **Synchronized Method**
 - Allows only one thread to access the method at a time.
 - Ensures data consistency but may lead to performance overhead.

- **Synchronized block**
- provides better performance and reduces waiting time for other threads.
  - Syntax:
     - `synchronized(this)` (locks on the current instance of the class)
     - `synchronized(any reference variable)` (locks on the specified object referenced by `any reference variable`)   
  - Examples:
    ```java
    Synchronized(this)  //current class object lock
     {
    ----
     }

   Temp temp = new Temp();
   Synchronized(temp) 
   {
     —---------
   }

   Synchronized(Temp.class) 
   {
   —---------
   }

   int x= 10;
   Synchronized(x)  //will not work with primitive types 
   {
    —---------
    —-------------
   }

    ```
      
- **Limitations of `synchronized`**:
  - `synchronized(x)`: Cannot use primitive types (`x` must be an object reference).

**Can a Thread Acquire Multiple Locks Simultaneously?**

- Yes, a thread can acquire multiple locks in nested synchronized blocks.

**Wait() Method**

- Releases the lock of the current thread.
- When a thread calls `wait()`, it goes into a waiting state and remains there until the same object is notified or `notifyAll()` is called, after which the thread can resume execution.

**Sleep()**   

can be used to pause the execution of current thread for specified time in milliseconds.

**Difference Between User Thread and Daemon Thread**

- **User Thread**: Continues to run until the application terminates.
- **Daemon Thread**: Supports the application's main thread and terminates if all user threads are finished.

**Calling the `run()` Method of a Thread Class**

- Directly calling `run()` method doesn't create a new thread and executes in the calling thread's stack.

**Ensuring `main()` is the Last Thread to Finish in Java Program**

- Use `Thread.join()` method to wait for all created threads to complete before the main function finishes.

**Why Thread `sleep()` and `yield()` Methods are Static?**

- These methods apply to the current executing thread and are not specific to any thread object. They are common for all threads.

**Inter Thread Communication and Wait/Notify**

- **Inter Thread Communication**: Mechanism where threads communicate with each other.
- **Wait, Notify, and NotifyAll**:
  - `wait()`: Causes the current thread to wait until another thread invokes `notify()` or `notifyAll()` on the same object.
  - `notify()`: Wakes up a single waiting thread.
  - `notifyAll()`: Wakes up all waiting threads.

**Difference Between `wait()` and `sleep()` Method**

- `wait()`: Releases the lock and waits until notified.
- `sleep()`: Pauses the thread's execution for a specified amount of time.

**Difference Between `notify()` and `notifyAll()`**

- `notify()`: Wakes up a single waiting thread.
- `notifyAll()`: Wakes up all waiting threads.

**Volatile Keyword**

- `volatile`: Indicates that a variable's value will be modified by different threads.
- Ensures visibility and prevents caching of variable value in threads.

**Executor Framework**

- **Java Concurrency API** provides interfaces for concurrent programming.
-  Executor Framework in Java provides a higher-level abstraction for managing and controlling the execution of asynchronous tasks using thread pools.
-  Different implementation of Executor framework are FixedThreadPool,SingleThreadPool,SchedularExecutor etc. 

**Thread Pool**

- **Thread Pool**: Manages a pool of worker threads to execute tasks concurrently.
- **Executor Service**: Controls the pool of threads and manages their lifecycle.
  
![threadpool](https://github.com/codewithheeren/Java/assets/87074236/77be82b9-428c-4c5e-af47-de0c1801be9c)

**When Do You Get InterruptedException?**

- `InterruptedException` is thrown when a thread is waiting, sleeping, or doing I/O operations and gets interrupted by another thread.

**Runnable Vs Callable**

The run() method is used for implementing the Runnable, whereas the call() method is used for implementing the Callable. The run() method doesn't return anything, whereas the call() method returns a result of completion.
The call() method can throw an exception, whereas the run() method cannot.
--------------
