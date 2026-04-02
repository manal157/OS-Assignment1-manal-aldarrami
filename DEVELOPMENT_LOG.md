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
Entry 1 - [March 25, 2026, 4:00 PM]

What I did: GitHub Account Setup and Repository Forking.

Details:

Created a GitHub account using my university email (@std.psau.edu.sa) to avoid the grading penalty.

Forked the OS-Assignment1-Starter repository.

Renamed the repository to OS-Assignment1-[MyName] as required.

Cloned the repository to my local machine using VS Code.


Challenges: I initially forgot to verify my university email, which prevented me from forking.


Solution: Checked my university inbox, clicked the verification link, and then successfully forked the repo.

Time spent: 45 minutes.

Entry 2 - [March 26, 2026, 6:30 PM]

What I did: Personalization and Environment Setup.

Details:

Modified SchedulerSimulation.java at line 92 to replace the placeholder with my actual student ID.

Installed the Java Extension Pack in VS Code for debugging support.

Performed the first commit titled "Set my student ID: [ID]".


Challenges: The javac command was not recognized in the VS Code terminal.

Solution: Added the JDK bin folder to my system's PATH environment variable and restarted the IDE.

Time spent: 1 hour.

Entry 3 - [March 28, 2026, 3:00 PM]

What I did: Feature 1 Implementation - Process Priority.

Details:

Added a private int priority field to the Process class.

Updated the Process constructor and modified the process creation logic to generate random priorities (1-5).

Added logic to display the priority when a process enters the ready queue.

Challenges: The priority was not showing up in the console output despite being assigned.


Solution: I had to update the addProcessToQueue method in SchedulerSimulation.java to print the new priority field.

Time spent: 2 hours.

Entry 4 - [March 30, 2026, 8:00 PM]

What I did: Feature 2 & 3 - Context Switches and Waiting Time.

Details:

Implemented a static counter for context switches that increments every time a thread starts.

Used System.currentTimeMillis() to capture the start and end times for each process to calculate wait time.

Created the final summary table to display Process Name, Burst Time, and Waiting Time.


Challenges: The context switch counter was resetting every time a process was re-queued.


Solution: Moved the counter to a static variable in the SchedulerSimulation class so it persists throughout the entire simulation.

Time spent: 2.5 hours.

Entry 5 - [March 31, 2026, 5:00 PM]

What I did: Documentation and Video Demonstration.

Details:

Completed REFLECTION.md and ANSWERS.md with detailed explanations based on the Silberschatz textbook.

Recorded a 3-minute video showing the GitHub repo, code walkthrough, and a live execution of the simulation.

Uploaded the video to Google Drive and set permissions to "Anyone with the link".


Challenges: The video was too long (5 minutes) initially.


Solution: I re-recorded the session, focusing only on the specific requirements: code changes, execution, and the explanation of Thread.sleep().

Time spent: 3 hours.

Summary
Total time spent on assignment: 9.25 hours.


Most challenging part: Managing the waiting time calculation accurately, as I had to ensure the time spent actually running was subtracted from the total time the process existed in the system.


Most interesting learning: Seeing how the Round-Robin algorithm actually handles "fairness" by preempting threads that exceed their quantum, which I observed through the re-queueing messages in my console.


What I would do differently next time: I would start using Git branches for each feature to keep my development even more organized before merging them into the main branch.

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

### Entry 1 - [Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

### Entry 2 - [Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

### Entry 3 - [Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

### Entry 4 - [Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

### Entry 5 - [Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

### Entry 6 - [Optional - Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

## Summary

**Total time spent on assignment**: [X hours]

**Most challenging part**: 

**Most interesting learning**: 

**What I would do differently next time**: 
