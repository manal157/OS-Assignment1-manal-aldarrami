# Reflection Questions

## Instructions
Answer the following questions about your learning experience. Each answer should be **at least 5-7 sentences** and show your understanding.

---

## Question 1: What did you learn about multithreading?

**Your Answer:**

[Write your answer here. Discuss specific concepts like thread creation, thread states, how threads execute concurrently, what surprised you, etc.]

---

## Question 2: What was the most challenging part of this assignment?

**Your Answer:**

[Describe the specific challenge. Was it understanding the code? Implementing a feature? Using Git? Explain what made it difficult and how it relates to the course concepts.]

---

## Question 3: How did you overcome the challenges you faced?

**Your Answer:**

[Describe your problem-solving approach. Did you read documentation? Ask for help? Debug systematically? What resources did you use? What strategies worked?]

---

## Question 4: How can you apply multithreading concepts in real-world applications?

**Your Answer:**

[Give specific examples from real applications you use (web browsers, games, mobile apps, etc.). Explain why threads are useful in those scenarios. Connect to what you learned in this assignment.]

---

## Additional Reflections (Optional)

### What would you like to learn more about?

[Any topics related to threading, concurrency, or operating systems that you're curious about?]

---

### How confident do you feel about multithreading concepts now?
Through this assignment, I developed a solid understanding of how multithreading allows a single process to execute multiple sequences of instructions concurrently by sharing the same address space. I learned that threads are "lightweight" compared to processes because they share resources like memory and files, which significantly reduces the overhead of context switching. Working with the Runnable interface showed me how to define a task, while methods like Thread.start() and Thread.join() taught me how to manage the thread lifecycle and coordinate execution. I was particularly surprised by how the JVM scheduler handles preemption in a Round-Robin system, ensuring that no single thread can starve others of CPU time. Overall, I now see multithreading as an essential tool for creating responsive systems that can perform background tasks without freezing the main execution flow.

Question 2: What was the most challenging part of this assignment?
Your Answer:
The most challenging aspect was implementing Feature 3: Track Waiting Time, as it required a precise understanding of the difference between a process's total time in the system and its actual execution time. Initially, it was difficult to determine where to capture the "start time" and how to accumulate waiting intervals every time a process was preempted and sent back to the ready queue. This challenge directly relates to the course concept of CPU Scheduling metrics, specifically the distinction between turnaround time and waiting time. Additionally, managing the shared state of the contextSwitchCount across multiple threads required careful placement of the increment logic to avoid race conditions or inaccurate counts. This forced me to think critically about the flow of the SchedulerSimulation loop and how the scheduler interacts with the thread pool.

Question 3: How did you overcome the challenges you faced?
Your Answer:
To overcome these technical hurdles, I adopted a systematic debugging approach, using System.out.println statements to trace the exact moment a thread entered the "Running" vs. "Waiting" states. I heavily relied on the Silberschatz textbook (10th Edition) to clarify the theoretical definitions of thread states (New, Runnable, Running, Waiting, Terminated) before attempting to code them. When I struggled with Git integration in VS Code, I followed the recommended video tutorials to learn how to stage and commit changes feature-by-feature rather than in one bulk update. I also utilized online documentation for Java’s System.currentTimeMillis() to ensure I was capturing time stamps with enough precision for the simulation. Testing each feature independently before moving to the next allowed me to isolate errors early and maintain a functional codebase throughout the project.

Question 4: How can you apply multithreading concepts in real-world applications?
Your Answer:
Multithreading is a fundamental concept used in almost every modern application I interact with, such as Web Browsers and Multimedia Players. In a web browser like Chrome, one thread might be responsible for rendering the user interface while other background threads fetch data from a server or execute JavaScript, preventing the page from becoming unresponsive. Similarly, in a video streaming app, one thread handles the high-definition video decoding while another manages audio synchronization and a third monitors network buffering. This assignment’s focus on Round-Robin scheduling is particularly relevant to Game Engines, where the server must give every player a "fair" slice of processing time to ensure consistent latency across the network. Learning how threads yield the CPU and return to a ready queue has given me a much clearer picture of how operating systems maintain smooth performance in multitasking environments.

Additional Reflections (Optional)
What would you like to learn more about?
I am curious about Thread Synchronization and Locks (like Mutexes and Semaphores). While this assignment focused on scheduling, I want to learn more about how to prevent multiple threads from accessing the same data simultaneously to avoid "Race Conditions."

How confident do you feel about multithreading concepts now?
Rating: Intermediate
I feel confident in creating threads, managing their lifecycle, and understanding the basic logic of scheduling algorithms. However, I believe I need more practice with complex concurrency problems and advanced Java thread-pooling techniques.

Feedback on the assignment
This assignment was very helpful because it bridged the gap between theoretical OS concepts and practical Java programming. The visual progress bars and color-coded output made it much easier to see the Round-Robin algorithm in action.
[Rate yourself and explain: Beginner / Intermediate / Confident]

[Explain your rating - what do you understand well? What needs more practice?]

---

### Feedback on the assignment

[Any comments about the assignment? Was it helpful? Too easy/hard? Suggestions for improvement?]
