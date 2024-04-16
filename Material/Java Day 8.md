## OOPS Day 8

 @author Heeren

 **Topics Covered**
--------------
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

**Thread Priorities:**

- `MAX_PRIORITY`: Highest priority.
- `NORM_PRIORITY`: Normal priority (default).
- `MIN_PRIORITY`: Lowest priority.

**What is Thread Life Cycle?**

- The thread life cycle represents various states a thread can be in, including new, runnable, blocked, waiting, timed waiting, and terminated.
  
- ![lifecycle](https://github.com/codewithheeren/Java/assets/87074236/2e296a71-1cc2-4d7b-8b61-6e3671dd36e7)


**What is the Use of Join Method?**

  - When `join()` is called on a thread, the current thread(main thread) will wait until the specified thread completes its execution.

**What is the Use of Yield Method?**

- The `yield()` method causes the currently executing thread to pause temporarily and allow other threads to execute.

**What is Deadlock?**

- Deadlock occurs when two or more threads are blocked forever, waiting for each other to release the resources they need.

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

1. **New**: Thread is created.
2. **Runnable**: Thread is ready to run but not yet scheduled.
3. **Running**: Thread is executing (`run()` method is executing).
4. **Waiting (Block State)**: Thread is waiting for another thread (e.g., waiting on `sleep()` or waiting for I/O).
5. **Timed Waiting**: Thread waits for a specific period to avoid starvation.
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

- The thread scheduler in Java is responsible for determining which threads should run or wait based on their priority and state.

**What is the Difference Between `start()` and `run()` Method Call?**

- `start()`: Creates a new thread and executes the `run()` method on the new thread.
- `run()`: Executes the `run()` method on the current thread itself without creating a new thread.

**Can We Overload `run()` Method?**

- Yes, the `run()` method can be overloaded, but the original `run()` method of the `Thread` class must be overridden to provide custom behavior.

**What Will Happen if We Don’t Override the `Thread` Class `run()` Method?**

- If the `run()` method is not overridden, the default `run()` method of the `Thread` class does nothing (no execution logic).

**What Happens When We Call `run()` Method Explicitly?**

- Calling the `run()` method explicitly treats it like a normal method call without creating a new thread. The `run()` method runs on the calling thread (usually the main thread).


--------------
