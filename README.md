# Self-Driving-Car

A course by Professor Steven Waslander, Dr. Jonathan Kelly and Professor Paul Newman involving Vehicle Dynamics, Perception, Planning - mapping and controller as well as its firmware design aspects.  

### Tech Stack

 1. Forward Kinematics
 2. System Dynamics
 3. State-space equations and Laplace Transfer Function of LTI systems
 4. Feedforward Controllers
 5. PID, LQR and MPC controllers
 6. Geometric path tracking controller - Pure pursuit, Stanley controller, receeding horizon control
 7. [CARLA simulator](https://d3c33hcgiwev3.cloudfront.net/2tyroyDyEem9HA6xGGaRfg_daf207a020f211e990ff73ab14e458cc_CARLA--An-Open-Urban-Driving-Simulator.pdf?Expires=1617753600&Signature=LV43aNf3VjLhLmBcFZCgFSrgdGJVT2lUsvEVGr5ZVXfnHIqLnbR~GX2QomzchUJkEepQmFxKDhki6mDsFHqmhrhzxQL5TW3VBZ8~x12Bsc9P8yUAzjH6lfX5jFZm7i4aUO2jozftdfsJ33bZ92g9uxuoyNS6MuDcEoWa3CTeCm4_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A)
 8.  

## Description of files in this repository

 * __Kinematic_Bicycle_Model.ipynb__ - This files generates a **Forward Kinematic model** for a 4 wheeled vehicle, approximated to be a simple 2 wheeled bycycle model. We generate random trajectories and analyse the controller performance for the same. 
 * __Longitudinal_Vehicle_Model.ipynb__ - The model accepts throttle inputs and steps through the longitudinal dynamic equations. Once implemented, you will be given a set of inputs that drives over a small road slope to test your model.
 * __Cruise_control.py__ - Cruise Control based on Fuzzy Logic.
 * __Vehicle-Path-Control__ - Implemented a controller for the CARLA simulator where the goal is to control the vehicle to follow a race track by navigating through preset waypoints. The vehicle needs to reach these waypoints at certain desired speeds, so both longitudinal and lateral control will be required.
 * 

---

# The following section contains a brief of informative notes that I had made during my learning. 

Some shortforms:
  * OEDR - Object and Evet Detection and Response
  * ODD - Operational Design Domain
  * ACC - Adaptive Cruise Control
  * Ego - A term to express the notion of self, which is used to refer to the vehicle being controlled autonomously, as opposed to other vehicles or objects in the scene.
  * FMEA - Failure Mode and Effects Analysis
  * GNSS - Global Navigation Satellite System
  * HAZOP - Hazard and Operability Study
  * IMU - Inertial Measurement Unit
  * Lidar - Light Detection and Ranging

## Sensors 

A sensor is any device that measures or detects some property of the environment, or changes to that property over time. Sensors are broadly categorized into two types, depending 
on what property they record. If they record a property of the environment they are **exteroceptive**. Extero means outside, or from the surroundings. On the other hand, if the 
sensors record a property of the ego vehicle, they are **proprioceptive**. Proprios means internal, or one's own.

Some of the main sensors used for perception of a car:
 1. Camera
 2. Lidar
 3. Radar
 4. Ultrasonic
 5. GPS
 6. IMU
 7. Wheel Odometry

To learn more about sensing requirements for automated vehicles for highway and rural environments, check out [K.J. Bussemaker's master's thesis](https://repository.tudelft.nl/islandora/object/uuid:2ae44ea2-e5e9-455c-8481-8284f8494e4e).

## Software Stack 

  * environment perception, 
  * environment mapping, 
  * motion planning, 
  * vehicle control, 
  * system supervisor.

## Maps

 * Lidar Map generation
 * Occupancy Grid map for static objects
 * Hybrid map using process software for dynamic obstacles
