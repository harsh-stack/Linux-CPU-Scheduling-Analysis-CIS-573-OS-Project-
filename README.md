# Linux-CPU-Scheduling-Analysis-CIS-573-OS-Project-
CIS-573 Operating Systems team project with Saquib Hashmi. Data-driven analysis of Linux Completely Fair Scheduler (CFS) using live pidstat, ps, top monitoring + Python simulation of FCFS, SJF, Priority, Round-Robin algorithms on real process workloads.

## 🎯 Project Goals
Measure real Linux scheduling + compare theoretical algorithms:

1. Live Data Collection: pidstat (30/40/60/80s intervals), ps, top

2. Python Simulation: FCFS/SJF/Priority/RR on Kaggle CPU workload dataset

3. Metrics: Waiting time, turnaround time, response time, CPU utilization

4. Visualization: Algorithm comparison, CFS vs. theory
​
5. Analysis: Scheduler fairness, preemptive behavior
​

## 📊 Key Deliverables
Component	Status	Files
Proposals	✅ Complete	OS-Project-proposal.pdf 
​
Milestones	✅ Complete	OS-milestone-project-3.pdf 
​
Live Data	✅ 4 Intervals	pidstat_*_output-*.txt
Analysis Script	✅	analyze_pidstat-4.py 
​
Process Snapshots	✅	ps_output-10.txt, top_output-11.txt 
CPU Plot	✅	cpu_usage_plot-2.jpg 
​
## 🛠️ Methodology
​
text
1. DATA COLLECTION
   • pidstat -u 1 30/40/60/80 → CPU%, PID, command
   • ps -eo pid,ppid,cmd,%cpu,%mem → Process tree
   • top → Real-time resource snapshot

2. SIMULATION (Python)
   • Load Kaggle dataset (JobID, Burst, Arrival, Priority)
   • Implement FCFS, SJF, Priority, RR (preemptive/non)
   • Calculate: Wait Time, Turnaround, Response Time

3. ANALYSIS
   • Compare Linux CFS vs. algorithms
   • Visualize: CPU trends, wait time Gantt charts
   • Metrics: Fairness, throughput, starvation
## 📈 Results Preview
Total CPU Usage Over Time (pidstat analysis)
​

Sample pidstat Output (30s interval):

# Results:
23:19:14   UID       PID    %usr %system  %guest   %CPU   CPU  Command
23:19:15   1000    12345   2.50   0.75    0.00   3.25     0  firefox
23:19:16   1000    67890   1.25

23:19:14   UID       PID    %usr %system  %guest   %CPU   CPU  Command
23:19:15   1000    12345   2.50   0.75    0.00   3.25     0  firefox
23:19:16   1000    67890   1.25
