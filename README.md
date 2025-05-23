# Air Traffic Monitoring System

This C program simulates an air traffic monitoring system, managing arrival, departure, and emergency landing queues for planes. It uses a priority queue based on a minimum heap to prioritize planes based on their arrival or departure times and whether they have an emergency. The simulation tracks total planes, arriving planes, departing planes, total runways, total time, average wait time for arrival and departure, largest wait time for arrival and departure, and idle time.


## Key Data Structures
Plane_type struct:
id: plane ID.
time: time of request (arrival/departure).
action: 0 for arrival, 1 for departure.
emergency: true if it's an emergency landing.

## Heaps:

arrivalQueue: heap for normal arriving planes.
departureQueue: heap for departing planes.
emergencyLandingQueue: heap for emergency landings (highest priority).
Each queue uses a min-heap based on:
earliest time (lower time = higher priority),
emergency status (true > false),
lower id in case of tie.

## Simulation Process
1. Initialization (startSimulation)
Takes totalRunways and totalPlanes as input.

Fills and separates planes into relevant queues.

2. Run the simulation (runSimulation)
Manages runway assignment:

Emergency landings are given first priority.

Compares delay for arrivals and departures:

If arrival delay is significantly worse, prioritize landing.

Otherwise, allow takeoff.

Updates statistics like:

waitingTimeForArrival / waitingTimeForDeparture

avgWaitTimeForArrival / avgWaitTimeForDeparture

largestWaitTime...

idleTime when no planes are ready.

3. Ending the simulation (endSimulation)
Prints:

Total planes handled

Runways used

Timing statistics

## Heap Operations
enQueuePlane: Inserts plane into the heap.

deQueuePlane: Removes top-priority plane.

min_heapify, mnheapify: Maintain heap order.







