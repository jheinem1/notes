
## Thread concepts

- Multiple threads on multiple processors
    - ```mermaid
    flowchart TD
        C1[CPU 1] --- T1[Thread 1]
        C2[CPU 2] --- T2[Thread 2]
        C3[CPU 3] --- T3[Thread 3]
    ```
    - This is the faster approach, but does not handle shared resources well.
- Multiple threads on single processor
    - ```mermaid
    flowchart TD
        C1[CPU 1] --- T1[Thread 1]
        C1[CPU 1] --- T2[Thread 2]
    ```
    - This approach allows for guaranteed ordering of threads and shared data without worrying about concurrency.

## Thread class

```java
public interface Thread {
    public static void sleep(long millis);
    public void start();
    public boolean isAlive();
    public void setPriority(int priority);
    public void join();
    public void yield();
    public void interrupt();
}
```

## Threading in Java

First, a class implementing `Runnable` is created to represent a thread or unit of work.

```java
public class TaskExample implements Runnable {
    public void run() {
        // run some code
    }
}
```

Next, a `Thread` object is created and given a `TaskExample` object to run.

```java
...
TaskExample task = new ThreadExample();

Thread thread = new Thread(task);

thread.start();
...
```

## Yielding in Java

The `System.yield()` method is used to yield the current thread to another thread.

```java
public void run() {
    for (int i = 0; i < 10; i++) {
        System.out.println("Thread " + Thread.currentThread().getName() + ": " + i);
        System.yield(); // yield the current thread to another thread
    }
}
```

## Deferred execution in Java

The `Thread.sleep()` method is used to suspend the current thread for a specified amount of time.

```java
public void run() {
    for (int i = 1; i <= 10; i++) {
        System.out.println("Thread " + Thread.currentThread().getName() + ": " + i);
        try {
            Thread.sleep(1000); // suspend the current thread for 1 second
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
    }
}
```

## Waiting for a thread to finish

The `Thread.join()` method is used to wait for a thread to finish.

```java
...
Thread thread = new Thread(new TaskExample());
thread.start();
try {
    thread.join(); // wait for the thread to finish
} catch (InterruptedException e) {
    e.printStackTrace();
}
...
```

## Checking if a thread is alive

The `Thread.isAlive()` method is used to check if a thread is alive. It returns `true` if a thread is ready, blocked, or running. It returns `false` if a thread has not started or finished.

```java
...
Thread thread = new Thread(new TaskExample());
thread.start();

System.out.println("Thread " + thread.getName() + " is alive: " + thread.isAlive()); // Thread [Thread Name] is alive: true
...
```

## Interrupting a thread

The `Thread.interrupt()` method is used to interrupt a thread.

If the thread is currently ready or running, it will be interrupted. However, if a thread is blocked, it will revert to the ready state and throw a `java.io.InterruptedException`.

```java
...
Thread thread = new Thread(new TaskExample());
thread.start();

System.out.println("Thread " + thread.getName() + " is alive: " + thread.isAlive()); // Thread [Thread Name] is alive: true
thread.interrupt(); // interrupt the thread
System.out.println("Thread " + thread.getName() + " is alive: " + thread.isAlive()); // Thread [Thread Name] is alive: false
...
```

The `isInterrupted()` method is used to check if a thread has been interrupted.

```java
...
thread.interrupt(); // interrupt the thread
System.out.println("Thread " + thread.getName() + " is interrupted: " + thread.isInterrupted()); // Thread [Thread Name] is interrupted: true
...
```

## Stop, suspend, and resume methods

While the `Thread` class provides the `Thread.stop()`, `Thread.suspend()`, and `Thread.resume()` methods, these are deprecated and should not be used.

Instead of using these methods to indicate a thread is stopped, you can simply assign the thread variable to `null`.

## Thread priority

Java assigns a priority to each thread (set by default to `Thread.NORM_PRIORITY`). This can be manually set to an integer between `1` and `10` using the `Thread.setPriority()` method.

There are also provided constants for the priority levels...

- `Thread.MIN_PRIORITY` (1)
- `Thread.NORM_PRIORITY` (5)
- `Thread.MAX_PRIORITY` (10)

## Thread synchronization

If multiple threads attempt to access a shared resource, the order in which (or if) the resource is accessed is not guaranteed. If multiple threads attempt to write to a shared resource, it is possible that data will be corrupted/overwritten.

```java
public void run() {
    var balance = bankAccount.getBalance();
    setBalance(balance + 1);
}
```

For example, if the above task is run on two threads, the two threads will both get the same balance and attempt to add 1 to the original balance, leaving the balance at `balance + 1` (instead of `balance + 2`).

It's recommended to either ensure threads wait for each other to finish, or to make a copy of the shared resource before writing to it.