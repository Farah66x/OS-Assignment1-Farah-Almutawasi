# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer: A thread is a smaller unit of execution, but a process is a separate program with its own memory and resources.Because threads share memory, they can communicate with each other more quickly. Compared to threads, processes are slower to construct and demand more resources. Because threads are lightweight and effective at emulating CPU scheduling, we used them in this project. There would have been needless overhead if procedures had been used.**

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer: When a process does not finish within its time quantum, it is moved to the end of the ready queue. This ensures fairness so that all processes get equal CPU time. The process waits for its next turn and continues execution later.**



Example from my output:
```
⚡ Quantum progress: [███████████████] 100%
⏸ P5 completed quantum 5000ms │ Overall progress: [█████████░░░░░░░░░░░] 45%
Remaining time: 5986ms
↻ P5 yields CPU for context switch

➕ P5 added to ready queue │ Burst time: 10986ms
┌─ Ready Queue ─────────────────────────────────────────────────────────────────
│ [P7 → P8 → P9 → P10 → P11 → P1 → P3 → P4 → P5]
└───────────────────────────────────────────────────────────────────────────────
```

**Explanation of example:**
In this instance, process P5 had remaining time (5986 ms) because it did not complete inside its time quantum (5000 ms). The scheduler triggered a context switch and halted its execution. P5 was then placed back at the end of the ready line. This implies that it won't restart until all other processes have finished. This behavior demonstrates how Round-Robin scheduling guarantees process equity.

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

 1.	  New:
P1 is in the New state when it is first created using new Thread(process) before being added to the ready queue.
	2.	Runnable:
P1 becomes Runnable when it is added to the ready queue:
➕ P1 added to ready queue │ Burst time: 10483ms │ Priority: 1
3.	Running:
P1 enters the Running state when the scheduler selects it and starts execution:
▶️ P1 executing quantum [5000ms]
4.	Waiting:
P1 goes into a Waiting state during execution when the thread is temporarily paused using Thread.sleep():
⚡ Quantum progress: [███████████████] 100%
5.	Terminated:
P1 reaches the Terminated state when it finishes execution completely:
✓ P1 finished execution!
Explanation:
The output shows how P1 moves through different thread states during execution. It starts as a new thread, becomes runnable when added to the queue, then runs when selected by the scheduler. During execution, it waits briefly due to Thread.sleep() which simulates processing time. Finally, it terminates when its remaining time reaches zero and it completes execution.

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: web server

**Description**: 
Multiple user requests are handled simultaneously by a web server.

**Why Round-Robin works well here**: 
It guarantees equity and keeps any one request from taking too long.

### Example 2: Operating System CPU Scheduling

**Description**: Processes are scheduled by the OS for CPU execution.


**Why Round-Robin works well here**: 
It increases responsiveness and allots equal time to each task.

---

## Summary

**Key concepts I understood through these questions:**
1. The distinction between processes and threads, as well as the reasons why threads work better in simulations such as CPU scheduling.
2. How Round-Robin scheduling operates, particularly how unfinished operations are added back to the ready queue.
3. How a thread appears during program execution and its lifespan (New, Runnable, Running, Waiting, Terminated).

**Concepts I need to study more:**
1. sophisticated thread synchronization and preventing race situations.
2. Additional CPU scheduling strategies include Shortest Job First and Priority Scheduling.
