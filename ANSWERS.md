# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

[A process is an independent program in execution with its own memory space and system resources. A thread is a smaller unit of execution within a process that shares the same memory and resources. One key difference is that processes do not share memory, while threads share memory, making communication between threads faster. Another difference is that processes have higher creation and context switching overhead compared to threads. Threads are lighter and more efficient in terms of resource usage. In this simulation, threads are more suitable because they allow multiple tasks to run concurrently within the same program with better performance.]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

[In Round-Robin scheduling, if a process does not finish within its time quantum, it is preempted and moved to the end of the ready queue. This allows other processes to get CPU time before it runs again. The scheduler then selects the next process in the queue. When the process reaches the front again, it resumes execution for another time quantum. This cycle continues until the process completes]

Example from my output:
```
[Process P1 executed for 2 units
Time quantum expired for P1
P1 moved to end of ready queue]
```

**Explanation of example:**
[
In this example, P1 used its full time quantum but did not finish execution. It was moved to the end of the ready queue so other processes can run. Later, P1 will get another turn, ensuring fairness among all processes.]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[A thread goes through several states during its lifecycle. In this simulation, process P1 starts in the New state when it is created. It becomes Runnable after calling Thread.start(), meaning it is ready to be scheduled. When the CPU selects it, P1 enters the Running state and executes its task. If P1 is paused (for example using Thread.sleep()), it enters the Waiting state temporarily. Finally, once it finishes execution, it enters the Terminated state.]

1. **New**: [P1 is in the New state when it is first created but before start() is called.]

2. **Runnable**: [P1 becomes Runnable after Thread.start() is called and is ready to run.]

3. **Running**: [P1 is Running when the scheduler assigns CPU time to it.]

4. **Waiting**: [P1 enters Waiting when it is paused, such as during Thread.sleep().]

5. **Terminated**: [P1 is Terminated after it finishes execution]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Web Server]

**Description**: 
[A web server handles multiple user requests at the same time using threads.]

**Why Round-Robin works well here**: 
[Round-Robin ensures each request gets a fair share of CPU time, preventing any single request from blocking others and improving responsiveness.]

### Example 2: [Media Player]

**Description**: 
[A media player runs multiple tasks like playing audio, loading data, and updating the UI simultaneously.]

**Why Round-Robin works well here**: 
[Round-Robin allows smooth switching between tasks, ensuring responsiveness and preventing delays in playback or user interaction.]

---

## Summary

**Key concepts I understood through these questions:**
1. The difference between a process and a thread in terms of memory sharing and performance.
2. How Round-Robin scheduling works and how processes are re-queued after the time quantum expires.
3. The lifecycle of a thread (New, Runnable, Running, Waiting, Terminated) and how it changes during execution.

**Concepts I need to study more:**
1. 
2. 
