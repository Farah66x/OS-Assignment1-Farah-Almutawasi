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

## Your Development Log:

### Entry 1 - [March 25, 2026, 2:30 PM]

**What I did**: Started working on the assignment and explored the provided code

**Details**:
- Opened the project in VS Code
- Read and understood the structure of the code (Process class and SchedulerSimulation)
- Learned how Round-Robin scheduling works in the program
- Ran the program for the first time and observed the output
- Noticed how processes move in the ready queue and how context switching happens

**Challenges**: At first, it was confusing to understand how threads execute and how the scheduling loop works

**Solution**: Carefully read the code step by step and re-ran the program multiple times to understand the flow
**Time spent**: 4 hours
---

### Entry 2 - [March 26, 2026, 5:30 PM]

**What I did**: Studied the starter code and understood the scheduling logic

**Details**:
- Analyzed the Process class and SchedulerSimulation
- Understood how Round-Robin scheduling works
- Observed how threads are created and executed
- Traced the program output step by step
- Understood how processes move in the ready queue

**Challenges**: I found it difficult to understand how threads interact with the queue and how scheduling is controlled

**Solution**: Re-read the code carefully and linked it with OS concepts from lectures and notes

**Time spent**: 1 hour
---

### Entry 3 - [march 28, 2026 ]
**What I did**: Implemented Feature 1 (Process Priority)

**Details**:
- Added a priority field to the Process class
- Modified the constructor to include priority as a parameter
- Generated random priority values for each process (1–5)
- Updated the addProcessToQueue method to display priority in the output
- Verified that each process shows its priority correctly in the ready queue

**Challenges**: I was unsure where exactly to add the priority variable and how to pass it correctly between classes

**Solution**: Followed the structure of existing variables like burstTime and carefully updated the constructor and method calls

**Time spent**: 2 hours
---

### Entry 4 - [March 28, 2026, 6:00 PM]

**What I did**: Implemented Feature 2 (Context Switch Counter)

**Details**:
- Added a static variable to count context switches
- Incremented the counter inside the scheduler loop each time a process is executed
- Ensured the counter increases whenever a new thread starts execution
- Printed the total number of context switches at the end of the simulation

**Challenges**: I was unsure where exactly to increment the counter to accurately reflect context switching

**Solution**: Placed the increment right after selecting the next thread from the queue, ensuring each switch is counted correctly

**Time spent**: 1.5 hours
---

### Entry 5 - [March 29, 2026, 9:00 PM]

**What I did**: Implemented Feature 3 (Waiting Time Calculation)

**Details**:
- Added creation time and total waiting time variables to the Process class
- Used System.currentTimeMillis() to track when each process waits
- Updated waiting time before each execution of the process
- Calculated total waiting time for each process
- Displayed waiting time in the final process summary

**Challenges**: Understanding how to correctly calculate waiting time during multiple executions was confusing

**Solution**: Broke the problem into steps by tracking time before execution and updating the total waiting time incrementally

**Time spent**: 1.5 - 2 hours

---

### Entry 6 - [Optional - Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

## Summary
Total time spent on assignment: 5 days (approximately 8–10 hours total)

Most challenging part:
Understanding how the scheduler loop works and how processes move between execution and the ready queue. It was also challenging to track when to update values like remaining time and waiting time correctly.

Most interesting learning:
Learning how Round-Robin scheduling works in practice and seeing how threads simulate real CPU scheduling. Watching processes take turns and re-enter the ready queue helped me understand OS concepts more clearly.

What I would do differently next time:
I would start earlier and break the assignment into smaller parts from the beginning. I would also spend more time planning before coding to avoid confusion and reduce debugging time.
