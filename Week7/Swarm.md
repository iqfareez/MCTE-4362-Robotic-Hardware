# Swarming Robots

[![Download as PDF](https://img.shields.io/badge/Download%20as%20PDF-EF3939?style=flat-square&logo=adobeacrobatreader&logoColor=white&color=black&labelColor=ec1c24)](https://mdtopdf.up.railway.app/convertPdf?url=https://github.com/iqfareez/MCTE-4362-Robotic-Hardware/blob/main/Week7/Swarm.md)
![Assignment completion](https://img.shields.io/badge/Status-completed-green?style=flat-square)

# Swarming Robots

## Table of Contents

- [Introduction](#introduction)
- [History](#history)
- [Applications](#applications)
- [Main components of the robot](#main-components-of-the-vehicle)
  - [Body design](#body-design)
  - [Locomotion](#Locomotion)
  - [Navigation](#navigation)
  - [Data collection](#data-collection)
  - [Communication](#communication)
  - [Power management](#power-management)

## Introduction

Swarm robotics is a field of robotics that studies the behavior of **large groups of relatively simple robots** that work together to perform some tasks.

Swarm robotics is inspired by **social insects** such as ants, bees, and termites. These insects are known for their collective behavior and **ability to perform complex tasks as a group**. For example, ants can work together to carry food that is much larger than their size. Bees can work together to build a hive and produce honey, etc.

Currently, **existing swarms** (either civilian or military domains), are still under research and development phases.

![Swarm robotics domain](https://www.mdpi.com/sensors/sensors-21-02062/article_deploy/html/images/sensors-21-02062-g001-550.jpg)

## History[^1]

- **1988**: Term 'swarm' used in robotics by G. Beni and Fukuda
- **1989**: Fukuda describes a swarm as a group of robots that work together like the cells of a human body
- **1989**: G. Beni and J. Wang introduce 'swarm intelligence' as a concept
- **1993**: C. Ronald Kube and Hong Zohng build a multi-robot system inspired by natural swarms
- **1993**: Gregory Dudek defines swarm robotics based on different features of the system
- Early swarm robotic systems explore swarming behaviors in natural species
- Many studies and researches emulate swarming behaviors like foraging, flocking, sorting, stigmergy, or cooperation
- **2004**: G. Beni defines a swarm more precisely as simple, identical, and self-organizing robots with scalable systems and only local communication

## Main components of the robot

### Body design

Usually small in size and simple in design, and low in cost. The body design is inspired by insects. Take a look at some examples below:

![swarm robotics insects example](https://imgur.com/hxhqOlu.png)

In swarm robotics, quantity is more important than quality. The more robots you have, the more tasks you can perform. The optimal size depends on the task/mission.

### Locomotion

Several locomotion systems are being used. Some examples including[^2]:

| Robot name     | Locomotion strategy | Propulsion system      |
| -------------- | ------------------- | ---------------------- |
| Khepera        | Wheeled             | DC Motors              |
| Alice          | Wheeled             | Bidirectional Motors   |
| S-bot          | Treeled             | DC Motors              |
| Jasmine        | Treeled             | DC Motors              |
| I-Swarm        | Slip-stick          | Piezoelectric Polymers |
| e-puck         | Wheeled             | Stepper motors         |
| Kobot          | Wheeled             | DC Motors              |
| :new: HoverBot | Low-friction        | Planar coils           |

So, extracting from the table above, there are three (3) locomotion strategies that are used in swarm robotics which are **wheeled**, **treeled** (tracks + wheels), and **slip-stick**.

<table>
  <tr>
    <th>Wheeled</th>
    <th>Treeled</th>
    <th>Slip-stick</th>
  </tr>
  <tr>
    <td><img src="https://imgur.com/j1FhQPv.png"/></td>
    <td>
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b7/Sbots.jpg/440px-Sbots.jpg"/>
    </td>
    <td>
    <img src="https://imgur.com/mGJ68K1.png"/>
    </td>
  </tr>
  <tr>
    <td>
      <ul>
      <li>Robot velocity: 25 cm/s</li>
      <li>Typically easy to design and control</li>
      </ul>
    </td>
    <td>
    <ul>
      <li>Hybrid between wheeled and tracked</li>
      <li>More traction and stability when moving over rough or uneven terrain</li>
    </ul>
    <td>
     <ul>
      <li>Robot velocity: 1 cm/s</li>
      <li>Needs Flat surface</li>
      <li> Inspired by the way snake moves</li>
      </ul>
    </td>
  </tr>
</table>

The **propulsion system** used is also varied. Some examples including DC motors, bidirectional motors, piezoelectric polymers, stepper motors, and planar coils.

| Propulsion system      | Description                                                                                                                                                                               | Example                                                                                                                        |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| DC Motors              | Simple, reliable, and efficient, and they can provide a wide range of speeds and torques.                                                                                                 | [Harvard RoboBees](https://wyss.harvard.edu/technology/robobees-autonomous-flying-microrobots/)                                |
| Bidirectional Motors   | a.k.a DC geared motors, are similar to DC motors but have a gearbox attached to the output shaft. This gearbox allows the motor to provide more torque at lower speeds.                   | [Alice](https://www.researchgate.net/publication/2363777_The_Autonomous_Miniature_Robot_Alice_from_Prototypes_to_Applications) |
| Piezoelectric Polymers | **Smart material** that can generate motion in response to an electrical signal. These materials are lightweight, flexible, and can provide high-speed motion with low power consumption. | [I-Swarm](https://www.youtube.com/watch?v=zul0y5yPOKM)                                                                         |
| Stepper motors         | Motor that rotates in discrete steps, making them useful for precise motion control.                                                                                                      |                                                                                                                                |

### Navigation

#### Sensors

The crucial aspect of navigation is the sensors used. Some examples used including:

- **Accelerometer**: To measure inclination, collision, free-fall, movement acceleration, etc.
- **IR Sensors**: To measure distance, bearings etc.
- **Wheel encoder**: To determine the distance traveled by a robot or the speed of the robot's movement.
- **Torque sensor**: For controlling the robot's movement and ensuring that it is operating within safe limits.
- **Gyroscope**: To determine the robot's orientation and movement in space.
- **Inclinometer**: To determine the robot's orientation relative to the ground or a reference plane.
- etc.

#### Behaviors[^3]

| Behavior                | Description                                                                                                          | Example                                                                                     |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| Collective exploration  | Navigation of the swarm of robots through the environment in order to explore it                                     | Searching for objects, establishing a communication network, or monitoring the environment  |
| Coordinated motion      | Moving the swarm of robots in a formation                                                                            | A line or flocking formation                                                                |
| Collective transport    | Enabling the swarm of robots to move heavy or large objects together                                                 | Moving furniture or other heavy objects                                                     |
| Collective localization | Helping robots in the swarm find their position and orientation relative to each other via a local coordinate system | Establishing a local coordinate system throughout the swarm to determine relative positions |

### Data Collection

Examples of data collected by swarm robots[^3]:

> Platypus, an autonomous swarm robotic boats, collects data about **water quality** (sanity, oxygen stratification etc.).

> SAGA (Swarm Robotics for Agricultural Applications) project39 targets a **distributed monitoring and mapping** scenario using a swarm of UAVs, which is a novelty in smart farming

> Hydromea is able to take water quality measurements at many **locations simultaneously** down to a depth of 300 m and create 3D data sets with high spatial and temporal resolution

> The project ROBORDER (Autonomous Swarm of Heterogeneous Robots for Border Surveillance) employs an autonomous swarm of heterogeneous robots (UGV, UAV, USV) equipped with multimodal sensors for sea and **land border surveillance**.

### Communication

The most common technologies for sending messages from robot to robot in swarms are Bluetooth, wireless LAN or infrared.

#### Control Architectures

Communication is important to coordinate the movements of each robot in space. Below are examples of control architecture that is typically used. [^4]

<table>
<thead>
<tr>
<th>Control Architecture</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>Centralized control
<img src="https://imgur.com/LwQI6Oe.png">
</td>
<td>
The commands go to the centralized controller, which,
in turn, distributes instructions to each robot in the swarm.
</td>
</tr>
<tr>
<td>Hierarchical control
<img src="https://imgur.com/ZKAsZOo.png">
</td>
<td>
The commands go to (one or) several “squad leaders”,
which, in turn, distribute instructions to the individual robots in their “squad".
</td>
</tr>
<tr>
<td>Ensemble-level control
<img src="https://imgur.com/x280WXh.png">
</td>
<td>
The commands are broadcast to the swarm as a
single group, after which the individual robots make decisions on how to action that
command.
</td>
</tr>
<tr>
<td>Behavioural control
<img src="https://imgur.com/8mYVdyw.png">
</td>
<td>
Each unit has a pre-programmed library of
behaviors. The human commands the swarm to execute a certain behavior.
</td>
</tr>
</tbody>
</table>

#### Important consideration[^5]

- **Communication Range** - If the communication range is too small, robots can't communicate or only if they are nearby. If the communication range is big, this means that communication can jam, because every robot has to listen to every message that was sent.
- **Length of Messages** - Short messages produce a large overhead due to the header information normally sent with every message (contains ID, target,...). Large messages tend to fail more often than short ones.
- **Propagation Time** - The time it takes to send a message through the whole swarm. This metric is important because it affects the ability of the swarm to coordinate its actions and respond to changes in the environment. In general, **shorter propagation times are better**, as they allow for more rapid and efficient communication among the swarm members.
- **Interferences** - Nearly every type of communication unit has to deal with interferences and other external influences. This can be signals from a nearby Wireless LAN, the sunlight or things like the infrared port of a laptop.

**Example**: Ocado robot transmits data between the robots and the cloud using **cellular technology**. The cloud server handles the vast amount of data to coordinate the robots using machine learning approaches

### Power Management

Keeping a large swarm charged up and running smoothly could be difficult without some automated method of charging and reprogramming. There are a few methods by which the swarm could be charged.

#### Charging Station[^6]

The simplest and lowest cost of the auto-stations only provides recharging functionality.

- Allows robot to autodock and recharge
- Simple regulated voltage source
- Two contacts to bot (Power, Gnd)
- Interconnects for ganging charging and maintenance stations together

![strip charging](https://imgur.com/bKVHXLc.png)
![2 strip charging station](https://imgur.com/Gzlfxbx.png)

#### Maintainance Station[^6]

This station has multiple functions, including **recharging, reprogramming, and communication** with the bot from a host computer. It also allows the bot to report new data etc.. The host can monitor the bots' activity and track their health, such as how many times the battery has been recharged or how many operational hours they have experienced.

- Allows the robot to autodock, recharge, reprogram, and communicate with a host
- Simple regulated voltage source for recharging and for powering bot
- I2C communication with the bot
- Four contacts to bot (Power, Gnd, Clk, & Data)
- Microcontroller to handle I2C communications
- USB or RS-232 communication with the host computer.

![Self aligning docking bay](https://imgur.com/Qqys3Ik.png)

#### Charging Robot[^7]

It would be challenging to maintain the optimal functionality of a vast number of robots without a portable charging station. To support a large swarm of robots, it would be **ideal to have several docking stations on the charging robot**. The ability to adapt to different charging scenarios is crucial, and therefore versatility is essential.

![Robot sensor](https://imgur.com/dlN71l8.png)

Similar metal strip as found in the figure above is installed on the charger robot sides. The charging robot will **employ comparable data packets as the swarm robots**, but with the distinction that it will incessantly transmit a message. If a mobile robot's battery level falls below a specific threshold and they cannot relocate themselves, they will send request messages to the mobile charging robot.

Connecting mobile robots to charger robot sides:

![Charging robot illustration](https://imgur.com/i7uvWjF.png)

Metal contacts for connecting to charger metal strip:

![robot strip](https://imgur.com/PQZi4il.png)

[^1]: https://roboticsbiz.com/advantages-and-history-of-swarm-robotics-sr-explained/
[^2]: https://www.frontiersin.org/articles/10.3389/frobt.2017.00055/full
[^3]: https://www.frontiersin.org/articles/10.3389/frobt.2020.00036/full
[^4]: https://www.unidir.org/publication/swarm-robotics-technical-and-operational-overview-next-generation-autonomous-systems
[^5]: http://www.swarmrobot.org/Communication.html
[^6]: http://www.swarmrobot.org/PowerDockingStation.html
[^7]: https://ieeexplore.ieee.org/document/5189756
