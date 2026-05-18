# Voice-Coil-Actuators-and-Vibration-Isolation-Platform
Hardware documentation and design files for a 6-DOF hybrid active-passive vibration isolation platform using voice coil actuators in a Stewart platform configuration

## Goal of the project: 
Develop an in-house voice coil actuator and build a stewart platform based vibration isolation platform using these actuators. We intend to make a hybrid, table top vibration isolation platform. This paltform should be able to hold about 100kg and damp out vibrations in the 1-10Hz range (for now)

## System architecture: 
passive layer (negative stiffness module) → active layer (6x VCA) → sensing for closed feedback loop (LVDT per leg) → control

## Current status: 
- servo prototype
- design of VCA with integrated LVDT
- machined VCA and LVDT

## Immediate steps:
- wounding of the machined parts with appropriate wire
- testing all the required parameters of the VCA and LVDT 
- building a 1 DOF vibration isolation system with the current VCA and LVDT prototype
- try to prototype stewart platform with linear actuators

## Repo structure:
- /active isolation --- brief overview with explanation of VCA and LVDT
- /QZS --- research summary of QZS
- /cad --- cad files and notes about current design
- /references

## Where to start:
A vibration isolation platform would involve a base plate that is exposed to the vibrations and a top one that stays stable throughout (isolates the vibrations). The system that transcends between the both plates is where the actual engineering comes in play.
To begin understanding the project, we can start with understanding the basis of a stewart platform. The basic premise of a stewart platform involves a parallel manipulator that uses six linear actuators to attain 6 DOF. To make a vibration isolation platform, each leg of the platform is planned to be structured as follows: passive layer (negative stiffness module) → active layer → sensing for closed feedback loop (LVDT). 
Each layer is further explained in its respective folder of the repo.

## Hardware inventory:
1. machined parts - innovation lab (C06)
2. ferrite rods - innovation lab (C06): 9, IPTIF (D03): 1
3. linear bearings - innovation lab (C06): 2, B03: 4
4. magnets - innovation lab (C06): 1, B03: rest
5. piston - innovation lab (C06): 1
6. off the shelf VCA (mounted) - innovation lab (C06)
