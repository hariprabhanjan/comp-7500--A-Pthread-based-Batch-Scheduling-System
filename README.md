# COMP7500-A-Pthread-based-Batch-Scheduling-System

Project AUbatch-A Batch Scheduling System

Dr.Qin

HariPrabhanjan Lakshminarayana

COMP 7500 Advanced Topics in Operating Systems


AUbatch is made up of two distinct and collaborating threads: the scheduling thread and the dispatching
thread. The main goal of the project is to create a CPU scheduler using the p-thread library. The system's
fundamental functionality is that jobs are submitted by the user and the system is designed to execute
those jobs based on three policies (FCFS, SJF, Priority), and the scheduler loads the jobs into the buffer,
and the dispatcher takes the scheduled jobs present in the buffer and executes them. This system uses
condition variables and mutexes to achieve synchronization. In addition, job performance is evaluated in
the system.
1) Design Dataflow diagram


2. A Performance Evaluation
2.1 Metrics – Average turnaround time, Average wait time, Throughput
After implementing the three scheduling policies (i.e., FCFS, SJF, and Priority), we compare the
performance of these algorithms under various workload conditions.
 Average Response Time = waiting time
 Throughput
3. User Interface
AUbatch commands are.
(1) help,
(2) run,
(3) list,
(4) change scheduling.
Figure below shows the sample dialog for help command.
 Help: Gives a list of commands that can be used to interact with the system and it says how to
use them.
 Run: It is to submit the jobs into the buffer. It takes the 2 arguments to run the
microbenchmark along with the burst time and priority of the job.
 List: Displays the submitted jobs and their details.
4. Three Scheduling Policies/Algorithms
• FCFS: It schedules the jobs in the buffer with FCFS policy
• SJF: It schedules the jobs in the buffer with SJF policy
• Priority: It schedules the jobs in the buffer with this policy
• Quit: quits the system with the performance evaluated results.
Command priority This command changes the scheduling policy to priority.
Command fcfs This command changes the scheduling policy to FCFS
Command sjf This command changes the scheduling policy to SJF.
5. Performance metrics
A function is called in dispatcher to evaluate the execution of jobs submitted by the user, waiting
time, time at which the job is executed, and completion time via timestamps, to calculate the
average turnaround time, average waiting time, and throughput of the job execution.
6. Performance Evaluation
FCFS: This policy performed the worst of the three, but only marginally worse than priority.
SJF: This policy outperformed the others by having the shortest average waiting time and
turnaround time.
Priority: This policy performed marginally better than FCFS however I believe it could easily be
the other way around as priority is arbitrarily assigned to each process
7. Lessons from this project
I learned working with threads - Mutex and condition variable implementation - microbenck,
PThread Library, Conditional Variables, A good bit of programming, and fork. Which I really
feel is useful for my interviews.
8. Future Improvements
. we must implement test modules, If the user changes the policy, all the jobs in my current
implementation will be deleted, and new jobs will be organized according to the selected policy
type. The obvious decision needs some work.
. should make it be able to read benchmarks.
. It is necessary to implement the automated performance evaluation.
