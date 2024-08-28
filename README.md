# Air Traffic Monitoring System

This C program simulates an air traffic monitoring system, managing arrival, departure, and emergency landing queues for planes. It uses a priority queue based on a minimum heap to prioritize planes based on their arrival or departure times and whether they have an emergency. The simulation tracks total planes, arriving planes, departing planes, total runways, total time, average wait time for arrival and departure, largest wait time for arrival and departure, and idle time.

## Getting Started

To compile and run the program, use a C compiler such as GCC:

gcc -o air_traffic_simulation air_traffic_simulation.c
