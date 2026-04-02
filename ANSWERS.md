# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

[A thread is a smaller, lighter unit of execution that works inside a process and shares its resources, while a process is an independent program in operation that runs in its own dedicated memory space. While threads are quicker to construct and can readily interact through shared memory, processes are resource-intensive and necessitate complicated communication. In contrast to employing separate processes, this project's usage of threads allowed for the effective simulation of several concurrent tasks within a single program, greatly lowering system overhead.]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

[A process is preempted (temporarily stopped) and moved to the end of the ready queue in Round-Robin scheduling if it does not complete within the allotted time quantum. After that, the CPU moves on to the following process in the queue. Only when every process in front of it has had a turn will the process be given another opportunity to run.]

Example from my output:
```
? P1 executing quantum [4000ms] 
? P1 completed quantum 4000ms │ Overall progress: 49%
   Remaining time: 4069ms
? P1 yields CPU for context switch

? P1 added to ready queue

Ready Queue:
[P3 ? P4 ? P5 ? ... ? P16 ? P1]
```

**Explanation of example:**
[In this example, process P1 started execution with a burst time of 8069ms, but the time quantum is only 4000ms. After using its full quantum, it still has 4069ms remaining, so it cannot finish.

Because of that:

P1 is stopped (preempted) after its quantum expires
It yields the CPU to allow another process to run
Then it is placed at the end of the ready queue]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: [P1 is in the New state when it is first created and added to the system, as shown when it appears in the output with its burst time and priority. At this stage, the process has been created but has not started execution yet.]

2. **Runnable**: [P1 enters the Runnable state when it is placed in the Ready Queue. In the output, this is shown when P1 is added to the ready queue and waits with other processes. At this point, it is ready to run and waiting for CPU scheduling.]

3. **Running**: [P1 is in the Running state when the CPU starts executing it. This is clearly shown in the output when P1 is executing its time quantum (e.g., executing 4000ms). Here, the process is actively using the CPU.]

4. **Waiting**: [P1 enters the Waiting state when it does not finish within its time quantum. In the output, after completing part of its execution, it yields the CPU and is added back to the ready queue. During this time, it waits for its next turn while other processes execute.]

5. **Terminated**: [P1 reaches the Terminated state when it finishes execution completely. In the output, this is shown when P1 completes its final small remaining time and the remaining time becomes 0ms. At this point, the process has finished and will not run again.]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Web Server Handling Multiple Client Requests]

**Description**: 
[Numerous incoming client requests (such as loading webpages and API queries) are processed by a web server. Multiple users may access the server at once, and each request is managed by a different thread.]

**Why Round-Robin works well here**: 
[Every request is given an equal amount of CPU time thanks to round-robin scheduling. Because no single request may take up all of the processor, overall responsiveness is enhanced, which is crucial for interactive users. Additionally, it avoids hunger and offers consistent performance, which makes it perfect for systems with numerous brief, independent tasks.]

### Example 2: [Online Gaming Server]

**Description**: 
[In online gaming servers (such as pubg or Call of Duty), many players are connected and sending commands simultaneously. Each player’s actions (like movement, shooting, or state updates) are handled by threads.]

**Why Round-Robin works well here**: 
[Round-Robin ensures that each player’s thread gets CPU time in a fair and cyclic manner. This prevents any single player from monopolizing resources, maintaining fairness and smooth gameplay. It also keeps the server responsive and reduces lag, even when the number of active players is high]

---

## Summary

**Key concepts I understood through these questions:**
1. The distinction between threads and processes, as well as the reasons why threads are more effective when handling multiple activities at once within a single program.
2. Preemption, time quantum, and ready queue behaviour are all aspects of Round-Robin scheduling.
3. The statuses New, Runnable, Running, Waiting, and Terminated as well as how threads transition between them are all part of a thread's lifespan.

**Concepts I need to study more:**
1. More sophisticated scheduling algorithms than Round-Robin include Multilevel Queue Scheduling and Priority Scheduling.
2. the effects on concurrent programs of thread synchronisation and shared resource management (such as semaphores and mutexes).
