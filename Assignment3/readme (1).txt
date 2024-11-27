Project Overview
This project includes two tasks:

Drone Communication System (Task 1): A monitoring and control system for a fleet of autonomous drones, handling control commands, telemetry data, and file transfers.
Weather Monitoring System (Task 2): A real-time weather monitoring system for a large city, with a central server and multiple weather stations transmitting data such as temperature, humidity, and air pressure.
Task 1: Drone Communication System
How to Build
Compile the server and client programs:

sh
g++ -o server1 server1.cpp -lpthread
g++ -o client1 client1.cpp -lpthread
Run the server in the background:

sh
./server1 
Run the client:

For each drone client, execute:

sh
./client1 droneId
Task 1 Features
Handles control commands, telemetry data, and file transfers between the central server and drones.
Ensures reliable communication with error handling and reconnection mechanisms.



Task 2: Weather Monitoring System
How to Build
Compile the server and client programs:

sh
g++ -o server server.cpp -pthread -lz
g++ -o client client.cpp -lz
Run the server in the background:

sh
./server > server_output.log 2>&1 &
Run the client:

For each weather station, execute:

sh
./run_clients.sh
Task 2 Features
Implements TCP Reno for congestion control to adjust the data transmission rate.
Simulates a limited network environment with constrained bandwidth and server capacity.
Supports dynamic data compression to optimize data transmission without overloading the server.
