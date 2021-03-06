# Machine Improvement Proposals

A simulation in C using queues and linked lists<br>
written by: Kurt King 2015

## I. Overview
Server 1 is a bottleneck and does many things. Its step 1 takes an average of 20 time units and its step 2 
takes an average of 15 time units. It can only process one widget at a time. While a widget is on step 2, 
no widgets can be serviced on step 1.    

##### Alternative A.
Add a new server (server 2) that only does "step 2" functions. Server 1 will then become a "step 1"-only server.
This means widgets go to server 1 (for step 1) and then server 2 for step 2. Different widgets can be processed 
on both servers at the same time.

##### Alternative B.
Upgrade server 1. The upgrade will reduce the average processing time for step 1 from 20 tu to 15 tu. The step 2
time will not be changed. Server 1 is still processing both steps. While a widget is on step 2, no widgets can be 
serviced on step 1.

The downtime to reconfigure is expected to be the same for both alternatives so it isn't a factor.  

## II. File List
------------
| File Name | File Description |
| --------- | ---------------- |
| simulation.h | Header file - contains typedefs, constants, and function prototypes |
| simulation.c | Bottleneck simulation functions |
| simulationDriver.c | Driver file - contains main function and functions to handle input | 
| p4ACinput.txt | Input for running simulations A and C |
| p4Binput.txt | Input for running simulation B |
| sim | Executable produced when using makefile |
| Makefile | Compiles and links appropriate files to create the executable to run the bottleneck simulation |

## III. General Purpose
This program takes widgets from a file and runs simulations on them. The output of the program
shows the statistics for each simulation. Judging by the statistics, the user would be able to
specify which simulation is the most efficient.

## IV. Key Functions
coming soon

## V. Important Typedefs
coming soon

## VI. Input/Output
coming soon

## VII. Makefile
There is a general Makefile for the simulation.

    Once changes have been made to a file, simple run:
        $ make sim

    This will create the executable sim in your current directory
    Refer to running simulation to execute program
