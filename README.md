# PathFindingForDroneUsingAlgorithm

Drone Delivery System

Overview
--------
This project simulates a drone delivery system that accounts for obstacles such as buildings and no-fly zones while calculating optimal paths for package deliveries. The system uses a Rapidly-exploring Random Tree (RRT*) algorithm to navigate the drone through a grid-like map, considering a weight limit for each delivery round and ensuring collision-free paths.

Features
--------
- Random Map Generation: Creates a map with randomly placed buildings and no-fly zones.
- Package Delivery: Simulates delivering packages to specified points while avoiding obstacles.
- RRT* Pathfinding: Uses RRT* algorithm to plan paths that avoid collisions and minimize travel distance.
- Multiple Rounds: Packages are grouped into rounds based on weight limits, and each round is handled separately.
- Visualization: The map is visualized using matplotlib, with paths, buildings, and no-fly zones clearly marked.

Installation
------------
To run this project, you need to have the following Python libraries installed:

- numpy: For mathematical operations and vector handling.
- matplotlib: For visualizing the delivery routes and obstacles.
- random: For generating random numbers, particularly for random map generation.

You can install the required dependencies using the following command:

    pip install numpy matplotlib

Usage
-----
Steps
1. Prepare the Environment:
   Make sure you have the required libraries installed. If not, install them using the command mentioned above.

2. Run the Script:
   After installing the dependencies, run the Python script to simulate the drone deliveries. The script will:
   - Generate a map with random buildings and no-fly zones.
   - Calculate delivery paths using the RRT* algorithm.
   - Display a plot showing the delivery paths, obstacles, and delivery points.

3. Output:
   - The total distance covered by the drone will be printed to the console.
   - A plot will display the final delivery map, with buildings, no-fly zones, and the drone's travel paths for each delivery round.

Example
-------
    python drone_delivery.py

The drone will start at the coordinates (0, 0) and attempt to deliver packages to the locations specified in the `delivery_points` list. Each round will handle a set of deliveries, ensuring the total weight does not exceed the specified `weight_limit`.

Key Functions
-------------
- generate_random_map(): Generates a random map with buildings and no-fly zones.
- RRTStar: Class implementing the RRT* pathfinding algorithm to plan safe routes.
- deliver_packages(): Main function for executing the delivery rounds.
- plot_results(): Visualizes the map and delivery routes.

License
-------
This project is open-source and available under the MIT License.
