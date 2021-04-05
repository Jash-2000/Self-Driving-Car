## Trajectory path to be followed
![Trajectory_Path](https://github.com/Jash-2000/Self-Driving-Car/blob/main/Vehicle-Path-Control/trajectory.png)

In this project, I have implemented a controller for the CARLA simulator. The goal is to control the vehicle to follow a race track by navigating through preset waypoints. 
The vehicle needs to reach these waypoints at certain desired speeds, so both longitudinal and lateral control will be required. The file **controller2d.py** class file, is where 
the controller has been implemented.

The controller provides you with the following relevant information required for its implementation. All units are in SI (meters, seconds, radians), and CARLA works in the 
left-handed coordinate system (due to the Unreal Engine adopting the left-handed coordinate system). This generally shouldn't be an issue for this assignment since the controller 
operates in the x, y and yaw space. The waypoints variable is a Python list of waypoints to track where each row denotes a waypoint of format [x, y, v], which are the x and y 
positions as well as the desired speed at that position, respectively. An example of accessing the third waypoint's y position is: 
```python
  waypoints[2][1] # Remember that Python's indexing begins at 0
```

Along with the other variables, the waypoints will update on each simulation step - so please do not assume the waypoint variable never changes. Here the waypoints are a linearly
interpolated (for location and speed) subset of the entire set of waypoints (from racetrack_waypoints.txt). In other words the waypoints variable is an enhanced (finer resolution)
portion of the entire set of waypoints that is near the vehicle. This is done to reduce the computation time and the performance of the controller.

To modify the reference path and speed, edit the "racetrack_waypoints.txt" file. This file will contain the path and reference speed for each waypoint in the path. The rows of the
txt file is each waypoint in sequence, and the columns are in the following format: "X position (meters), Y position (meters), reference speed (meters per second". You may modify 
the reference speed by changing the third column of the file, and the path by modifying the path by changing the first and second columns.

---

## Design of the controller

  1. 
