# Self-Driving-Car

A course by Professor Steven Waslander, Dr. Jonathan Kelly and Professor Paul Newman involving Vehicle Dynamics, Perception, Planning - mapping and controller as well as its firmware design aspects.  

## Description of files in this repository

 * __Kinematic_Bicycle_Model.ipynb__ - This files generates a **Forward Kinematic model** for a 4 wheeled vehicle, approximated to be a simple 2 wheeled bycycle model. We generate random trajectories and analyse the controller performance for the same. 
 * __Longitudinal_Vehicle_Model.ipynb__ - The model accepts throttle inputs and steps through the longitudinal dynamic equations. Once implemented, you will be given a set of inputs that drives over a small road slope to test your model.
 * 

---

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

---

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

---

## Software Stack 

  * environment perception, 
  * environment mapping, 
  * motion planning, 
  * vehicle control, 
  * system supervisor.

---

## Maps

 * Lidar Map generation
 * Occupancy Grid map for static objects
 * Hybrid map using process software for dynamic obstacles
