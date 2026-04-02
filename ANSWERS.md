# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

Example from my output:
```
[Paste a relevant snippet from your program output here showing a process being re-queued]
```

**Explanation of example:**
[Explain what's happening in the output snippet you pasted]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: [When is P1 in New state?]

2. **Runnable**: [When does P1 become Runnable?]

3. **Running**: [When is P1 Running?]

4. **Waiting**: [When/why would P1 be Waiting?]

5. **Terminated**: [When is P1 Terminated?]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

### Example 2: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

---

## Summary
Explain the difference between a thread and a process. Why did we use threads in this assignment instead of creating separate processes?

Your Answer:
A process is an independent program in execution that owns its own memory space and system resources, while a thread is a "lightweight" unit of execution that exists within a process. In this assignment, we used threads because they share the same address space and data, which makes context switching much faster and less resource-intensive than creating entirely separate processes. According to Silberschatz, threads are more suitable for this simulation because the SchedulerSimulation class needs to manage multiple tasks (processes) that all access a shared processQueue and processMap. Using threads allows for efficient communication and coordination using methods like Thread.start() and Thread.join() without the high overhead of Inter-Process Communication (IPC).
+4

Question 2: Ready Queue Behavior
Question: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

Your Answer:
In Round-Robin scheduling, if a process's remaining execution time exceeds the fixed time quantum, it is preempted by the scheduler. The process yields the CPU, its state is saved, and it is moved to the back of the ready queue (FIFO) to wait for its next turn. This ensures "fairness" by giving every process an equal opportunity to use the CPU regardless of its total burst time.
+4

Example from my output:

Plaintext
[P1] is running... (Quantum: 3000ms)
[P1] Progress: [##########] 100% of quantum reached.
[P1] has 2500ms remaining.
[P1] yields the CPU and enters the ready queue.
Current Queue: [P2, P3, P4, P1]
Explanation of example:
In this snippet, P1 was assigned a 3000ms time quantum but had a longer burst time. Once the quantum expired, the run() method updated the remainingTime and the process was re-enqueued at the end of the processQueue. As shown in the "Current Queue" status, P1 is now behind P2, P3, and P4, allowing them to execute before P1 gets another time slice.
+2

Question 3: Thread States
Question: A thread can be in different states: New, Runnable, Running, Waiting, Terminated. Walk through these states for one process (P1) from your simulation.

Your Answer:
The lifecycle of P1 in the simulation follows the standard JVM thread states as described in the assignment objectives:
+2


New: P1 is in the New state when the Process object is instantiated and the Thread object is created but start() has not yet been called.
+1


Runnable: P1 enters the Runnable state once addProcessToQueue is called and the thread is ready to be executed by the JVM scheduler.


Running: P1 is Running when it is at the head of the processQueue and the CPU begins executing the code inside its run() method.
+1


Waiting: P1 enters a Waiting (or Timed Waiting) state when it calls Thread.sleep() to simulate the passage of time during its execution burst.
+1


Terminated: P1 is Terminated when its remainingTime reaches zero, the run() method finishes, and the thread is joined back to the main thread.
+1

Question 4: Real-World Applications
Question: Give TWO real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

Your Answer:

Example 1: Web Server Request Handling
Description:
A modern web server (like Apache or Nginx) uses threads to handle thousands of incoming HTTP requests simultaneously.

Why Round-Robin works well here:
Round-Robin is ideal because it provides high responsiveness. By giving each request a small time slice, the server ensures that no single large file download blocks small metadata requests, providing a "fair" experience for all connected users.
+3

Example 2: Multiplayer Game Engine
Description:
In a multiplayer game, a server must process updates (physics, inputs, logic) for 20+ players at the same time.

Why Round-Robin works well here:
Round-Robin ensures predictability and low latency. Because the game state must be synchronized across all players, using a fixed quantum to process each player's input prevents "lag spikes" that would occur if one player's complex movement calculation took priority over everyone else's.

Summary
Key concepts I understood through these questions:

The efficiency of Thread-level parallelism compared to process-level execution.
+1

The mechanical implementation of Round-Robin fairness through preemption and re-queueing.
+1

How the Thread Lifecycle (New to Terminated) is controlled by specific Java methods.
+1

Concepts I need to study more:

Advanced synchronization techniques to prevent race conditions in shared data maps.

The mathematical impact of different Time Quantum lengths on overall system throughput.
**Key concepts I understood through these questions:**
1. 
2. 
3. 

**Concepts I need to study more:**
1. 
2. 
