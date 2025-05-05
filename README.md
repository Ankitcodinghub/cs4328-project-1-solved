# cs4328-project-1-solved
**TO GET THIS SOLUTION VISIT:** [CS4328: Project #1 Solved](https://www.ankitcodinghub.com/product/cs4328-project-1-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;49149&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;4&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (4 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS4328: Project #1 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (4 votes)    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
<span style="font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue', sans-serif;">1 Overview</span>

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
In this project, we are going to build a discrete-time event simulator for a number of CPU schedulers on a single CPU system. The goal of this project is to compare and assess the impact of different schedulers on different performance metrics, and across multiple workloads.

1.1 CPU Scheduling Algorithms

We are going to implement the following scheduling algorithms that we discussed in class: 1. First-Come First-Served (FCFS)

2. Shortest Remaining Time First (SRTF)

3. Highest Response Ratio Next (HRRN)

4. Round Robin, with different quantum values (RR)

1.2 Performance Metrics

We are interested to compute the following metrics, for each experiment: • The average turnaround time

• The total throughput (number of processes done per unit time) • The CPU utilization

• The average number of processes in the ready queue

2 The Simulator

The simulator needs to generate a list of processes. For each process, we need to generate its arrival time and its requested service time. We can assume that processes arrive with an average rate λ that follows a Poisson process (hence exponential inter-arrival times). The service times are generated according to an exponential distribution. We will vary λ to simulate different loads while keeping the average service time fixed. The simulator should stop after processing 10,000 processes to completion (without stopping the arrival process), then it should output the statistics (i.e., the metrics above).

Events (e.g., process arrival, process completion, time-slice) that occur causes the simulator to update its current state (e.g., cpu busy/idle, number of processes in the ready queue, etc.) To keep track and process events in the right order, we keep events in a priority queue (called “Event Queue”) that describes the future events and is kept sorted by the time of each event. The simulator keeps a clock the represents the current time which takes the time of the first event in the Event Queue. Notice that when an event is processed at its assigned time, one or more future events may be added to the Event Queue. For example, when a process gets serviced by the CPU, another process can start executing (if one is waiting in the ready queue)

</div>
</div>
<div class="layoutArea">
<div class="column"></div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
&nbsp;

</div>
</div>
<div class="layoutArea">
<div class="column">
and under FCFS, we know exactly when this process would finish (since FCFS is non-preeptive), so we can schedule a departure event in the future and place it in the event queue. Notice that time hops between events, so you would need to update your simulator clock accordingly.

The simulator should take few command-line arguments. The first is to indicate the scheduler, a 1 through 4 value based on the list above. Also, it should take other arguments such as the average arrival rate, the average service time and the quantum interval (for RR). Running the simulator with no arguments, should display the parameters usage.

Each scheduler would need to maintain a queue (the “Process Ready Queue”) for the ready processes that are waiting for the CPU. A scheduler will select a process to run next based on the scheduling policy. Clearly, this queue should not be confused with the Event Queue that is used to hold events to be processed in the future.

3 The Runs

We will vary the average arrival rate, λ, of processes from 1 process per second to 30 processes per second (based on a Poisson process). The service time is chosen according to an exponential distribution with an average service time of 0.06 sec.

For each value of λ, we need to compare the performance of each scheduler, based on the metrics above. It is recommended that you write a simple batch file that would run those experiments and put the results in a file (that you can later import into a spread sheet and plot the values).

#!/bin/bash

rm sim.data

for ((i = 1; i &lt; 31; i++)); do

<pre>   ./sim 1 $i 0.06 0.01
</pre>
<pre>   cp sim.data /data/1-$i-006.data
done
</pre>
This will run the simulator using FCFS (indicated by the value 1 in the first argument) for 30 different values of λ using 0.06 as the average service time and a quantum value of 0.01 (which is ignored in all algorithms, except round robin). Then, the script will move the sim.data file to a safe place.

With the Round Robin algorithm, an argument is supplied to indicate the quantum used. Use 2 different values of quantum; 0.01 and 0.2. Clearly, if a process finishes before its quantum expires, the CPU will schedule the next process right away.

4 Submission details

Submissions are done through TRACS. Submissions will include the code and how to compile and run the simulator on one of the CS servers, along with a report containing the results and their interpretation.

The report will include the results of the experiments along with a description. We will run 5 different algorithm (since the round-robin will have 2 different settings for quantum values), each for 30 different values of λ. A total of 150 runs! The report should include a single plot for each one of the above metrics. The plot on the x-axis will vary λ and represent the metric on the y-axis with different line color for each scheduler.

You can write your simulator in any of these languages (C, C++, Python or Java), however, it is your responsibility to ensure it runs under the CS Linux servers with a command line – nothing graphical. Please indicate clearly how to compile and run your simulator.

</div>
</div>
</div>
