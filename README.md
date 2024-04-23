# 6-axis_assembly_station_for_thrust_microbearings
Project for laboratory of Micromechanics and Photonics at Warsaw University of Technology. 

## Table of Contents
- [Detailed Description](#detailed-description)
- [Work at laboratory](#Work-at-laboratory)
- [Micro robotic gripper](#Micro-robotic-gripper)
  - [Aim of the project](#Aim-of-the-project)
  - [3D model](#3D-model)
  - [Arduino control](#Arduino-control)
- [6-axis control](#6-axis-control)
  - [Aim of the project](#Aim-of-the-project)
  - [3D model](#3D-model)


## Detailed Description

At my second job, I was involved in an international scientific research project called UVIPOM2 (ULTRA-EFFICIENT WIRELESS POWERED MICRO-ROBOTIC JOINT FOR HEALTH APPLICATIONS). I served as the main person responsible for producing 3D printed components. One of the most challenging tasks I was given involved developing the assembly method of the shafts of the micro-thrust bearings. The difficulty in assembly arose from the fact that the shafts we used had a diameter of no more than 100 micrometers, while the entire bearings could have a diameter of up to 1 mm. 

#### The micro-thrust bearing:

<img src="https://github.com/majkel808/6-axis_assembly_station_for_thrust_microbearings/assets/163661382/c73c7dba-c05d-4856-ab6c-74845dcf5921" alt="20230615_115629" width="800">

Until that time, the shaft assembly was done by hand, it was extremely difficult task. My goal was to develop a device that not only facilitates everyone's work but also allows for achieving greater precision in assembly than was previously possible.

## Work at laboratory 
During my work in the laboratory, I participated in conducting tribological research on miniature ball bearings. For this purpose, we utilized highly precise force and torque measurement systems. Among my tasks were also:

- Developing a methodology for measuring the influence of magnetic force acting on the bearing
- Conducting friction force tests on bearings
- Upgrading assembly and measurement equipment
- 3D modeling and 3D printing (FDM)
- Creating technical documentation for manufacturing
- Testing and servicing equipment (CNC milling machine, 3D printer, CO2 laser)
- Electroplating coatings
- Investigating the influence of coatings on friction force
- Data analysis
- Making controllers for stepper motors used in different project in the laboratory

I was given opportunity for representing Wasraw Univesity of Technology on 16th International Invention and Innovation Show INTARG® 2023. 

<img src="https://github.com/majkel808/6-axis_assembly_station_for_thrust_microbearings/assets/163661382/f4a25a28-bc2e-48ef-8acb-0a01e834ac4d" alt="20230524_103632" width="500">

## Micro-robotic gripper

### Aim of the project

Design a device that will precisely pick up the micro-shaft of the thrust bearing and allow for an easier assembly process of the entire bearing. I aimed for it to be easily controlled, the optimal choice for that would a joystick due to its intuitive control interface and the built-in button that would allow for additional functionality if needed. The micro-robotic gripper would be attached to the Cartesian XYZ robot with a high-precision linear actuators, as shown below.

#### Laboratory Setup for Assembly and Testing of Micro-Bearings

<img src="https://github.com/majkel808/6-axis_assembly_station_for_thrust_microbearings/assets/163661382/71054e6f-62f4-4fe4-a1bf-7e601fa82f09" alt="20230619_171729" width="550">

### 3D model

I have decided to utilize a small and precise linear stepper motor to control the positioning of the endpoints of the small tweezers. With this setup, it would be possible to achieve a precision of 10 to 20 microns for the grip. The device would have the following functionalities:
- mechanical angular position adjustmet of the gripper
- automatic control of the tweezer grip
- easy to use controller
- the device is compact in size, so that it would be possible to use it under the microscope

I've designed the device in Autodesk Inventor. And manufactured the part with 3D printing. The 3D model and the final assebmly has been shown in the pictures below.

<img src="https://github.com/majkel808/6-axis_assembly_station_for_thrust_microbearings/assets/163661382/6854386e-3bc3-43aa-a90a-38046c744e5b" alt="Zrzut ekranu 2024-04-23 210503" width="550">

<img src="https://github.com/majkel808/6-axis_assembly_station_for_thrust_microbearings/assets/163661382/df55c0cd-f335-4f46-b267-513800c004ee" alt="dddd" width="550">

### Arduino control

To controll the robotic micro-gripper I've designed the stepper motor controller, based on the Arduino Nano. The user imput was given via joystick:
- moving left/ right -> fast travel endpoints of the tweezers
- moving up/ down -> slower and precise movement
- using the button -> moving by one step of the motor, motor rotates in according of the last fast or slow movement
  
#### Arduino stepper motor controller 

<img src="https://github.com/majkel808/6-axis_assembly_station_for_thrust_microbearings/assets/163661382/5efaf860-a713-4fd5-92f1-a8770a7a73ef" alt="Controller" width="400">

## 6-axis control

The culmination of the assembly station modernization was a project of mine, undertaken as part of my coursework at university. I wanted to designe a machine that would allowed for full 6-axis position control of the shaft relative to the one of the disk that the bearing was made of. With this device, it would be posible, not only to asseble it atomaticly but with full control of the eccentricity and skewness of the shaft relative to the disk. 

### Aim of the project

Design the station with three additional degrees of freedom for positional control, ensuring very high angular precision. The automatic controll woudl be achived with the feedback loop from the computer vision software and from 3 digital microscopes. This part of the project was only conceptual. 

### 3D model


Three degrees of freedom were already available via the XYZ robot, so the only additional device needed would be for angular position control. I chose to design a Stewart platform with high-precision linear actuators. The most crucial mechanical aspect of the design, which would have the greatest impact on precision, was the selection of angular bearings. After conducting some research, I opted to use kinematic coupling between the platform and the actuators to achieve the highest possible precision. 

#### The model created with Autodesk Inventor:

<img src="https://github.com/majkel808/6-axis_assembly_station_for_thrust_microbearings/assets/163661382/4a211ad1-1a01-4e11-ab0a-d355538f4339" alt="Controller" width="650">

<img src="https://github.com/majkel808/6-axis_assembly_station_for_thrust_microbearings/assets/163661382/affc2a53-6123-4d51-a6b6-261d2738f85f" alt="Controller" width="650">


