[![Download as PDF Button](https://img.shields.io/badge/Download%20as%20PDF-EF3939?style=flat-square&logo=adobeacrobatreader&logoColor=white&color=black&labelColor=ec1c24)](https://mdtopdf.up.railway.app/convertPdf?url=https://github.com/iqfareez/MCTE-4362-Robotic-Hardware/blob/main/Week1/ROV.md)
![Assignment completion](https://img.shields.io/badge/Status-Completed-green?style=flat-square)

# Remotely Operated Vehicle (ROV)

## Table of Contents

- [History of ROV](#history-of-rov)
- [Applications of ROV](#applications-of-rov)
- [Main components of the vehicle](#main-components-of-the-vehicle)
  - [Hull design](#hull-design)
  - [Propulsion](#propulsion)
  - [Navigation](#navigation)
  - [Data collection](#data-collection)
  - [Data transmission](#data-transmission)
  - [Power management](#power-management)

## History of ROV

In **1953**, ROV were first build by Dimitri Rebikoff. The name is the Poodle.

<img src="https://bluerobotics.com/wp-content/uploads/2019/09/poodle-rov.jpg" width="50%">

In **1960**, navy has deployed ROVs to recover torpedos, bombs, mines etc. The vehicle is used in dangerous places for sailors such as mine area.

The initial commercial vehicle for the offshore oil industry was introduced in **1975**.

Later, in **1980s**, ROVs are used by the offshore oil industry to asssist development.

Today, more than 90% of the remotely operated vehicles (ROVs) created have been designed for commercial offshore activities such as supporting oil and gas drilling, inspecting, burying, and repairing pipelines and telecommunications cables.

## Applications of ROV

ROV are used in several missions:

- Pipeline inspection in **O&G industry**

  [![Pipeline inspection](https://markdown-videos.deta.dev/youtube/L33ME1L0DYM)](https://youtu.be/L33ME1L0DYM)

- **Science:** To study deep-sea flora and fauna, sample water, and recover shipwrecks for underwater archaeology projects.

  [![Shipwrecks discovery](https://markdown-videos.deta.dev/youtube/SdU453gR2QI)](https://www.youtube.com/watch?v=SdU453gR2QI&t=219s)

  [NOAA](https://oceanexplorer.noaa.gov/facts/rov.html) said:

  > ROVs, allow us to explore the ocean without actually being in the ocean.

- **Military and law enforcement** (search and rescue): For surveillance, search and recovery missions, disposing of explosives, and detecting environmental hazards.
- **Film** and documentary

  [![Beijing Aquarium](https://markdown-videos.deta.dev/youtube/F-viWrQ-7nU)](https://youtu.be/F-viWrQ-7nU)

- **Maritime**: Allow vessel owners to detect and quickly fix problems with the vessel’s structure.

  [![Ship Hull Inspections](https://markdown-videos.deta.dev/youtube/fm8bwW9yRXM)](https://youtu.be/fm8bwW9yRXM)

## Main components of the vehicle

ROV systems come in a variety of sizes and designs, but they often share **common features** made up of some or all of the elements outlined in the following sections.

### Hull design

Common hull design is open frame or close hull.

|                   | Open frame hull                                                                                          | Frameless hull (close hull)                                                                                |
| ----------------- | -------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| **Example**       | ![BlueROV2](https://imgur.com/0verevp.png) <br> [BlueROV2](https://bluerobotics.com/store/rov/bluerov2/) | ![SEABER YUCO SCAN MICRO](https://imgur.com/8iyYbgr.png) <br> [SEABER YUCO SCAN MICRO](https://seaber.fr/) |
| **Advantages**    | Stable 3DOF translational motions based on large metacentre.                                             | Greater mobility/highly manoeuvre                                                                          |
|                   | Larger payloads and can carry object.                                                                    | Typically lightweight and portable                                                                         |
|                   | Easier to attach tools and equipment.                                                                    | More energy efficient                                                                                      |
| **Disadvantages** | Have difficulties with motions requiring more than 3DOFs                                                 | Smaller/no payload                                                                                         |
|                   |                                                                                                          | Not convenient for attaching tool or equipment                                                             |

### Propulsion

There are three types of propulsion systems in ROV; Electrical, Hydaulic, and Ducted Jet.

#### a) Electrical

It uses electric motors to power propellers that provide thrust to move the ROV. The electrical power is typically supplied by a cable that is connected to a power source on the surface.

<img src="https://imgur.com/GtnPTFx.png" width="50%">

**Advantages**

- Ease of control
- High efficiency

#### b) Hydraulic

It uses a hydraulic system to power propellers that provide thrust to move the ROV. The hydraulic power is typically supplied by a pump that is located on the surface.

**Advantages**

- High power output
- Precise control
- High reliability

#### c) Ducted Jet

It uses water jets that are directed through ducts to provide thrust to move the ROV.

<img src="https://imgur.com/0iMP7r8.png" width="50%">

**Advantages**

- High manueverability
- Compact size
- Low noise level

### Navigation

#### a) Thrusters

On BlueROV2 (Heavy), it have **8 thrusters** to control the vehicle.

**4 vertical** thrusters to control up and down motion.

Another **4 thrusters** in **vectored configuration** that face 45 degree angle in all directions. By varying thrust in each thruster, it can create thrust vectors that allows the ROV move in any direction.

![BlueROV navigation](https://user-images.githubusercontent.com/60868965/226113764-161e897e-58dd-4771-9d2a-afc9db2865b5.gif)

_Source: https://www.youtube.com/watch?v=uugmuZINbW0_

BlueROV2 have buoyancy foam to, well, control the buoyancy.

<img src="https://imgur.com/uLf3C2K.png" width="60%">

#### b) Architecture

In the electronics enclosure (top cylinder), it contains Navigator Flight Controller (it's [Pixhawk](https://pixhawk.org/) I believe and ArduSub) running BlueOS.

Overall architecture overview of the navigation system:

<img src="https://www.ardusub.com/images/hardware/Connection-Diagram-R1.png" width="70%"></img>

_Image source: https://www.ardusub.com/introduction/hardware-options/connection-diagrams.html_

It uses onboard sensors (like [IMU](https://www.advancednavigation.com/imu-ahrs)) to determine its altitude and heading to automatically stabilizes and control the vehicle based on the pilot inputs.

### Data collection

The BlueROV2 contains Raspberry Pi computer that coonnects to various sensors, input and outputs. Sensors can be added/expanded according to the user needs. Some of the sensors are:

- Bar 30 pressure/depth & Temperature sensor
- 1080p HD camera (with Hitec HS-5055MG servo to control the tilting angle)
- 3-DOF gyroscope
- 3-DOF accelerometer
- 3-DOF magnetometer
- Internal barometer
- Current & Voltage Sensing
- Leak detection

For example, the image below is additional sensor added to the ROV. I believed it is a [side scan sonar](https://deepvision.se/products/side-scan-sonars/) module by [DeepVision](https://deepvision.se/).

<img src="https://imgur.com/CIBrYD3.png" width="70%">

Various electronics is packed on the top cylinder enclosure.

<img src="https://imgur.com/lDQR2sP.png" width="50%">

Meanwhile, SEABER YUCO-SCAN equipped with side scan sonar module to map the ocean/river/lake floor.

<img src="https://imgur.com/bIhBudQ.png" width="60%">

### Data transmission

The BlueROV2 connect to the ethernet network to forward the video stream and data to the computer on the surface.

<img src="https://imgur.com/EkR370g.png" width="70%%">

Fathom X Tether Interface board is an important component because it can transform the ethernet connection into a long range connection tether cable.

On the surface, there will be another FXTI module (or FXTI box) to convert those signal received from the ROV. It have USB connector to connect to the computer.

<img src="https://user-images.githubusercontent.com/60868965/226114024-729e2618-191a-4b76-ae64-d426f72b0042.png" width="45%">

_Source: https://bluerobotics.com/store/rov/bluerov2-accessories/fxti-asm-r1-rp/_

The software used in [QGroundControl (QGC)](http://qgroundcontrol.io/), which is an [open-source](https://github.com/mavlink/qgroundcontrol) software, cross-platform ground control station for drones (Android, iOS, Mac OS, Linux, Windows)

Features of the software including:

- View live stream camera feed
- View and adjust any parameters of the ROV
- Interface with a gamepad or joystick controller to control the vehicle.
- and more.

On the other hands, SEABER YUDO-SCAN uses its software (I believe it's proprietery) to plan a mission (i.e., path planning for the ROV to follow) and control the ROV.

After its mission have completed, the pilot can use the remote control shown below to retrieve the ROV.

<img src="https://imgur.com/RKTqE1q.png" width="70%">

### Power management

BlueROV2 have battery unit stored in the battery enclosure (bottom cylinder). For battery capacity of **18Ah** usuallly can last for 2 hours under normal use (for light use, it can go up to ~6hours)

<img src="https://imgur.com/Xaz03KO.png" width="70%">

For SEABER YUCO-SCAN, they reported to have endurance for **6 hours** at 2.5 knots
