---
layout: post
title:  "Multithreading in Java"
date:   2017-09-20 23:45:00 -0700
categories: Java
---

### Processes and Threads
In concurrent programming, there are two basic units of execution: processes and threads. **In the Java programming language, concurrent programming is mostly concerned with threads.** However, processes are also important.

A computer system normally has many active processes and threads. This is true even in systems that only have a single execution core, and thus only have one thread actually executing at any given moment. **Processing time for a single core is shared among processes and threads through an OS feature called time slicing.**

It's becoming more and more common for computer systems to have multiple processors or processors with multiple execution cores. This greatly enhances a system's capacity for concurrent execution of processes and threads — **but concurrency is possible even on simple systems, without multiple processors or execution cores.**

### Processes
**A process has a self-contained execution environment. A process generally has a complete, private set of basic run-time resources; in particular, each process has its own memory space.**

**Processes are often seen as synonymous with programs or applications. However, what the user sees as a single application may in fact be a set of cooperating processes.** To facilitate communication between processes, most operating systems support Inter Process Communication (IPC) resources, such as pipes and sockets. IPC is used not just for communication between processes on the same system, but processes on different systems.

**Most implementations of the Java virtual machine run as a single process.** A Java application can create additional processes using a ProcessBuilder object. Multiprocess applications are beyond the scope of this lesson.

### Threads
Threads are sometimes called lightweight processes. Both processes and threads provide an execution environment, but creating a new thread requires fewer resources than creating a new process.

**Threads exist within a process** — every process has at least one. **Threads share the process's resources, including memory and open files.** This makes for efficient, but potentially problematic, communication.

Multithreaded execution is an essential feature of the Java platform. Every application has at least one thread — or several, if you count "system" threads that do things like memory management and signal handling. **But from the application programmer's point of view, you start with just one thread, called the main thread.** This thread has the ability to create additional threads, as we'll demonstrate in the next section.

### Thread Priorities
Every Java thread has a priority that helps the operating system determine the order in which threads are scheduled.

Java thread priorities are in the range between MIN_PRIORITY (a constant of 1) and MAX_PRIORITY (a constant of 10). By default, every thread is given priority NORM_PRIORITY (a constant of 5).

Threads with higher priority are more important to a program and should be allocated processor time before lower-priority threads. **However, thread priorities cannot guarantee the order in which threads execute and are very much platform dependent.**

### Defining and Starting a Thread
An application that creates an instance of Thread must provide the code that will run in that thread. There are two ways to do this:
#### 1. Providing a Runnable object
The Runnable interface defines a single method, run, meant to contain the code executed in the thread. The [Runnable](https://docs.oracle.com/javase/8/docs/api/java/lang/Runnable.html) object is passed to the Thread constructor, as in the HelloRunnable example:
```java
public class HelloRunnable implements Runnable {

    public void run() {
        System.out.println("Hello from a thread!");
    }

    public static void main(String args[]) {
        (new Thread(new HelloRunnable())).start();
    }

}
```

#### 2. Subclass Thread.
 The Thread class itself implements Runnable, though its run method does nothing. An application can subclass Thread, providing its own implementation of run, as in the HelloThread example:
```java
 public class HelloThread extends Thread {

    public void run() {
        System.out.println("Hello from a thread!");
    }

    public static void main(String args[]) {
        (new HelloThread()).start();
    }

}
```

Notice that both examples invoke `Thread.start` in order to start the new thread.

#### Which of these idioms should you use? 
**The first idiom, which employs a Runnable object, is more general, because the Runnable object can subclass a class other than Thread. The second idiom is easier to use in simple applications, but is limited by the fact that your task class must be a descendant of Thread. This lesson focuses on the first approach, which separates the Runnable task from the Thread object that executes the task. Not only is this approach more flexible, but it is applicable to the high-level thread management APIs covered later.**


<br>
<br>
### Reference Links:

 - [The Java™ Tutorials](https://docs.oracle.com/javase/tutorial/essential/concurrency/procthread.html)
 - [Java - Multithreading](https://www.tutorialspoint.com/java/java_multithreading.htm)
 - [Class Thread](https://docs.oracle.com/javase/7/docs/api/java/lang/Thread.html)
 - [The Simple Threads Example](https://docs.oracle.com/javase/tutorial/essential/concurrency/simple.html)

