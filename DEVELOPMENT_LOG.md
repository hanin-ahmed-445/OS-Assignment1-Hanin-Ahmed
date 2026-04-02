# Development Log

## Instructions
Document your development process as you work on the assignment. Add entries showing:
- What you worked on
- Problems you encountered
- How you solved them
- Time spent

**Requirements**: Minimum 5 entries showing progression over time.

---

## Example Entry Format:

### Entry 1 - [April 1, 2026, 2:30 PM]
**What I did**: Forked the repository and set up my student ID

**Details**: 
- Created GitHub account with university email
- Forked the starter repository
- Changed student ID on line 92 to my actual ID (441234567)
- Compiled and ran the program successfully

**Challenges**: Had to install JDK first because javac wasn't recognized

**Solution**: Downloaded JDK 17 from Oracle website and set PATH variable

**Time spent**: 30 minutes

---
*** مهم ***
واجهتني مشكلة بنسختي الاولى واضطريت اني احذفها واسوي نسخه ثانيه لضيق الوقت وعدم الخبره لذلك ال commit اوقاتها متقاربه جدا بحيث اني كنت اعرف الاجابه من قبل وحالته بس حذفته انا كاتبه الوقت الحقيقي اللي استغرقته في حلها في المثال بالاسفل وجب التوضيح عشان في تناقض باجابتي سويت commit ورا بعض لكن استغرقت وقت كثير في الايام السابقه لحله

## Your Development Log:

### Entry 1 - [April 2, 2026, 12 PM]
**What I did**: set up GitHub

**Details**: 
1- create account
2- forked Dr.mahdi repository
3- Editing the fork

**Challenges**: i was a beginner and didn't know how to do it on my first time 

**Solution**: i watched many video and ask my sis

**Time spent**: 30 min

---

### Entry 2 - [April 2, 2026, 12 PM]
**What I did**: Code Review and Logic Mapping

**Details**: examining the fundamental elements of the simulation, particularly the integration between SchedulerSimulation and the Process class. I was able to see the concurrency model in action and successfully draw out the Round-Robin scheduling mechanism. In order to track the dispatch and execution of threads, I also carried out step-by-step debugging.

**Challenges**: Complexity in understanding thread-to-queue synchronization and interaction.

**Solution**: Conducted a deep dive into the code while applying OS principles regarding queue management.

**Time spent**: 1;30 hour

---

### Entry 3 - [April 2, 2026, 12:30 PM]
**What I did**: Added priority-based scheduling to the Process class.

**Details**: I updated the Process class by adding a priority attribute and enhanced the SchedulerSimulation logic to sort the queue by importance, ensuring through rigorous testing that high-priority threads are executed before lower ones.

**Challenges**: lack of experience

**Solution**: searched online

**Time spent**: 2 hours

---

### Entry 4 - [April 2, 2026, 1:10 PM]
**What I did**: Implemented a Context Switch Counter to monitor scheduler performance.

**Details**: In order to monitor thread transitions and assess the overhead and effectiveness of the scheduling method across multiple test runs, I incorporated a Context Switch Counter into the SchedulerSimulation.

**Challenges**: Determining the exact location in the code to trigger the counter for each process change.

**Solution**: Placed the counter increment right after polling a new thread from the ready queue.

**Time spent**: 3 hour

---

### Entry 5 - [April 2, 2026, 2:12 PM]
**What I did**: Implemented Waiting Time calculation for each process.

**Details**: In order to enable the system to compute individual and average waiting times by taking into account the amount of time a thread spends idling in the ready queue, I added logic to track arrival and finish times for each process.

**Challenges**:  I didn't know how to calculate the waiting time correctly when a process is interrupted and sent back to the queue.

**Solution**:  I searched for the formula and found that I should subtract the Burst Time from the Total Time spent in the system.

**Time spent**: 1 hour

---

### Entry 6 - [Optional - Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

## Summary

**Total time spent on assignment**: [About 8 hours]

**Most challenging part**: As a beginner, I found it very difficult to follow the code logic. My limited experience made it hard to understand how the scheduler and threads work together at the same time.

**Most interesting learning**: I found it most fascinating to observe how the computer truly "thinks" and handles jobs. Even though I'm just getting started with programming, it was a wonderful feeling to realise that I could comprehend and even alter how the scheduler operates.

**What I would do differently next time**: The next time, I would plan ahead and sketch the reasoning before writing any code. As a novice, I discovered that comprehending the flow first makes the programming portion more simpler and less perplexing.
