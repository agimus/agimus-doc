# Agimus

## Description

Agimus is a software framework aimed at controlling robot motions in manipulation tasks, automatically instanciating visual servoing on sections of the planned trajectory where the robot is about to grasp an object or to put an object on a plane surface.

The input to Agimus is a reference manipulation motion planned by [HPP](https://humanoid-path-planner.github.io/hpp-doc) to manipulate an object. Based on information about the object and grippers (whether they display apriltags) that enable them to be localized by a camera, the software instantiates visual servoing task:
  1. between the gripper and the object to grasp in pregrasp phase,
  2. between a contact surface and an object when the robot is about to put the object on the surface or lift it from the surface.

An example of manipulation motion planned by HPP is available [here](https://peertube.laas.fr/w/5txLFLLz7SbBP8C98roh26). The execution by Agimus is displayed [here](https://www.youtube.com/watch?v=rhKZ6PyLazk).

## Software

Agimus is composed of the following packages

  - [agimus](https://github.com/agimus/agimus): implements the finite-state machine that triggers the right controller at the right time,
  - [agimus-hpp](https://github.com/agimus/agimus-hpp): connection between HPP and Agimus,
  - [agimus-sot](https://github.com/agimus/agimus-sot): implementation of visual servoing controller into the [Stack-of-Tasks](https://stack-of-tasks.github.io/).
