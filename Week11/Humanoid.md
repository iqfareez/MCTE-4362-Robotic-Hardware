[![Download as PDF](https://img.shields.io/badge/Download%20as%20PDF-EF3939?style=flat-square&logo=adobeacrobatreader&logoColor=white&color=black&labelColor=ec1c24)](https://mdtopdf.up.railway.app/convertPdf?url=https://github.com/iqfareez/MCTE-4362-Robotic-Hardware/blob/main/Week11/Humanoid.md)
![Assignment completion](https://img.shields.io/badge/Status-Completed-green?style=flat-square)

# Humanoid Robots

## Table of Contents

- [Introduction](#introduction)
- [History](#history)
- [Main components](#main-components)
  - [Body design](#body-design)
  - [Locomotion](#locomotion)
  - [Navigation](#navigation)
  - [Data Collection](#data-collection)
  - [Data Communication](#data-communication)
  - [Power Management](#power-management)

## Introduction

Humanoid robots are remarkable creations that **closely resemble the human form**, featuring an array of advanced technologies and capabilities. With their human-like appearance and ability to perform intricate tasks, humanoid robots have the potential to revolutionize various industries, from healthcare and entertainment to manufacturing and personal assistance. These robots possess articulated limbs, sophisticated sensors, and artificial intelligence algorithms, enabling them to navigate complex environments, interact with humans, and mimic human gestures and expressions.

![humanoid robots](https://github.com/iqfareez/MCTE-4362-Robotic-Hardware/assets/60868965/f60ae85a-0565-4407-b578-84e538f9d252)

**[⬆ Back to top](#humanoid-robots)**

## History [^1]

| Year & Robot Name                    | Description                                                                                                                                                                                                                                                                                                                                                       |                                                                                                 Image                                                                                                  |
| :----------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| **1495 - Leonardo’s Robot**          | An inventor Leonardo da Vinci designed a suit of armour that moved as if there was a real person inside. It was operated by a series of pulleys and cables, it could do various human-like movements. The goal was merely to amuse Milanese royalty, but modern recreations of the device have shown that it was fully functional.                                |                                       ![leonardo image](https://upload.wikimedia.org/wikipedia/commons/thumb/4/45/Leonardo-Robot3.jpg/440px-Leonardo-Robot3.jpg)                                       |
| **1774 - The Jacquet-Droz Automata** | Pierre Jacquet-Droz, his son Henri-Louis, and Jean-Frédéric Leschot created three automata that are still operational today. One is a female robot musician who plays an organ with her fingers, another is a child robot artist capable of drawing four different images, and the third is a child robot writer who can write up to 40 characters using a quill. |                          ![robot image](https://images.squarespace-cdn.com/content/v1/58bb0536893fc04255997b40/1534602058526-D1HXFNZSNJGU0IVWX0G5/Jaquet+Droz+History+4.jpg)                           |
| **1970 - WABOT-1**                   | The first digitally controlled anthropomorphic robot was built at Waseda University in Tokyo. It had a limb-control system with tactile sensors for walking and gripping, a vision system that could measure distances, and a conversation system that could communicate in Japanese.                                                                             |                                                ![image](https://bostonglobalforum.org/aiwsin/wp-content/uploads/sites/18/2021/01/c7d5b.179.large_.jpg)                                                 |
| **2000 - Asimo**                     | Honda designed and developed Asimo as a multi-functional mobile assistant that could help people with poor mobility.                                                                                                                                                                                                                                              | ![asimo robot](https://www.cnet.com/a/img/resize/eda639c60821807e9759bb305152838b58ff5c3e/hub/2014/04/17/94b3b33e-eda0-459d-a5e2-7a75c7b3e80a/485318345.jpg?auto=webp&fit=crop&height=1200&width=1200) |
| **2016 - Sophia**                    | A humanoid robot capable of expressing emotions and holding conversations. It was designed to look like Audrey Hepburn, and has been granted citizenship in Saudi Arabia and the United Arab Emirates.                                                                                                                                                            |                         ![sophia robot](https://upload.wikimedia.org/wikipedia/commons/1/1e/Sophia_at_the_AI_for_Good_Global_Summit_2018_%2827254369347%29_%28cropped%29.jpg)                          |
| **2022 - Tesla Bot aka Optimus**     | Create a general purpose, bi-pedal, autonomous humanoid robot capable of performing unsafe, repetitive or boring tasks via AI.                                                                                                                                                                                                                                    |                                           ![tesla bot](https://media.wired.com/photos/611ffa5d042dfa2291227da2/1:1/w_1799,h_1799,c_limit/Gear-Tesla-Bot.jpg)                                           |

[^1]: https://www.howwegettonext.com/a-history-of-humanoids

**[⬆ Back to top](#humanoid-robots)**

## Main Components

### Body design

A robot resembling the **human body** in shape. Below is example of ASIMO Robot:[^2]

![Asimo Robot height](https://asimo.honda.com/images/im_specschart.jpg)

_ASIMO stands for **Advanced Step in Innovative Mobility**._

Lightweight materials, like a **magnesium alloy** structure, combined with powerful computers and **34 servo motors** throughout its body help ASIMO move smoothly with ease.

For it to have the flexibility to move like a human, Honda engineers created ASIMO with **34 Degrees** of Freedom. _One Degree of Freedom is the ability to move right and left or up and down._ Below is the breakdown of the degrees of freedom for human joints for the robot:

| Parts     | Joints                                               | DOFs       |
| --------- | ---------------------------------------------------- | ---------- |
| HEAD      | Neck joint (Up/Down, Left/Right Rotation)            | 3 DOF      |
| ARMS      | Shoulder joints (Forward/Backward, Up/Down Rotation) | 3 DOF      |
|           | Elbow joints (Forward/Backward)                      | 1 DOF      |
|           | Wrist joints (Up/Down, Left/Right, Rotation)         | 14 DOF     |
| HANDS     | 4 fingers (to grasp objects) / Thumb                 | 26 DOF     |
| HIP       | Rotation                                             | 2 DOF      |
| LEGS      | Crotch joint (Forward/Backward, Left/Right Rotation) | 3 DOF      |
|           | Knee joints (Forward/Backward)                       | 1 DOF      |
|           | Ankle joints (Forward/Backward, Left/Right Rotation) | 12 DOF     |
| **TOTAL** |                                                      | **57 DOF** |

More examples of other robots body design:

![examples](https://media.springernature.com/lw685/springer-static/image/art%3A10.1007%2Fs43154-021-00050-9/MediaObjects/43154_2021_50_Fig1_HTML.png)

**[⬆ Back to top](#humanoid-robots)**

### Locomotion

#### Legged locomotion

Most humanoid robot that are designed to move use **legged type locomoation**. Legged locomotion is more versatile and can be used in many different environments. However, legged locomotion is **more complex** than wheeled locomotion, for example.

Example below shows a **3-DoF leg** composed of three links: thigh, shank and hoof, connected through the hip, knee and fetlock joints. The **damper** is also installed on the hip joint to absorb the impact force when the hoof hits the ground.

![image](https://github.com/iqfareez/MCTE-4362-Robotic-Hardware/assets/60868965/6610b7da-5e09-4baf-ac5d-77badf474eec)

| Actuator        | Usage                      |
| --------------- | -------------------------- |
| Electric motor  | Generating leg movement    |
| Hydraulic       | Powering joint movements   |
| Pneumatic       | Controlling leg extension  |
| Servo motor     | Adjusting leg position     |
| Linear actuator | Enabling linear leg motion |
| Force sensor    | Detecting leg force        |

#### Face, limbs and hands

For some robots, they also equipped with limbs (arms etc) and moveable faces. Below are some examples of actuators used in robot Sophia: [^3]

| Location     | Actuators                                                                                                                                                                                                                                                                         |
| :----------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Arm          | Joint angle sensors, force sensors & touch sensors                                                                                                                                                                                                                                |
| Head & face  | Five [Dynamixel XM430](https://emanual.robotis.com/docs/en/dxl/x/xm430-w350/) servos and 23 [Xpert](https://www.xpert-rc-us.com/) servos.                                                                                                                                         |
| Eyes         | Two [Hitec HS-65MG](https://hitecrcd.com/products/servos/analog/micromini/hs-65mg/product) servos                                                                                                                                                                                 |
| Arms & hands | Two [Dynamixel MX64](https://emanual.robotis.com/docs/en/dxl/mx/mx-64/) servos, one [Dynamixel MX106](https://emanual.robotis.com/docs/en/dxl/mx/mx-106/) servo, four Dynamixel XM430 servos, six [Xpert](https://www.xpert-rc-us.com/) servos, and two MKS servos (per arm/hand) |

**Specifications of Dynamixel XM430 servo:**

![servo image](https://emanual.robotis.com/assets/images/dxl/x/x_series_product.png)

| Item                   | Specifications                                                                                                                                                                                                    |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| MCU                    | ARM CORTEX-M3 (72 [MHz], 32Bit)                                                                                                                                                                                   |
| Position Sensor        | Contactless absolute encoder (12Bit, 360 [°])                                                                                                                                                                     |
| Motor                  | Coreless                                                                                                                                                                                                          |
| Baud Rate              | 9,600 [bps] ~ 4.5 [Mbps]                                                                                                                                                                                          |
| Control Algorithm      | PID control                                                                                                                                                                                                       |
| Resolution             | 4096 [pulse/rev]                                                                                                                                                                                                  |
| Operating Modes        | Current Control ModeVelocity Control Mode<br>Position Control Mode (0 ~ 360 [°])<br>Extended Position Control Mode (Multi-turn)<br>Current-based Position Control Mode<br>PWM Control Mode (Voltage Control Mode) |
| Weight                 | 82 [g]                                                                                                                                                                                                            |
| Dimensions (W x H x D) | 28.5 x 46.5 x 34 [mm]                                                                                                                                                                                             |
| Gear Ratio             | 353.5 : 1                                                                                                                                                                                                         |
| Operating Temperature  | -5 ~ +80 [°C]                                                                                                                                                                                                     |
| Input Voltage          | 10.0 ~ 14.8 [V] (Recommended : 12.0 [V])                                                                                                                                                                          |
| Command Signal         | Digital Packet                                                                                                                                                                                                    |
| Physical Connection    | RS485 / TTL Multidrop Bus TTL<br>Half Duplex Asynchronous Serial Communication<br>RS485 Asynchronous Serial Communication with 8bit, 1stop, No Parity                                                             |
| Feedback               | Position, Velocity, Current, Realtime tick, Trajectory, Temperature, Input Voltage, etc                                                                                                                           |
| Case Material          | Metal (Front, Middle), Engineering Plastic (Back)                                                                                                                                                                 |
| Gear Material          | Full Metal Gear                                                                                                                                                                                                   |
| Standby Current        | 40 [mA]                                                                                                                                                                                                           |

**[⬆ Back to top](#humanoid-robots)**

### Navigation

Imitating human ability to walk, jump and run is a challenging task for engineers to design it. The robot must be able to **sense its environment** and **adapt to it**. The robot must also be able to **plan its path** and **avoid obstacles**.

In Sophia robot, her base has **WiFi** and **two cell modems**, so it can be driven using a **handheld controller**, much like a remote control car.

Below are some aspects that are involved in navigation:

#### Sensing

The robot must be able to sense its environment. This can be done using **sensors** such as **cameras**, **radars**, **ultrasonic sensors**, **infrared sensors**, **laser sensors** and **GPS**.

#### Planning

The robot must be able to plan its path. This can be done using **algorithms** such as **A\***, **Dijkstra's algorithm**, and so on.

Example: Tesla Bot sensing environement with the power of AI

![Environemnt discovery memorization](https://github.com/iqfareez/MCTE-4362-Robotic-Hardware/assets/60868965/f34f440d-2c72-47fb-97fd-49bf255b880b)

#### Inverse Kinematics

The robot must be able to calculate the **joint angles** required to move the robot to a specific position. The smooth and dynamic robot movement can uses inverse kinematics algorithm. Within robot motion pattern, positioning actuator angle of robot's legs will be determined by the amount of steps in X axis, Y axis, and Z axis robot.

#### Balance Model

Balance controller uses two types of sensors, **accelerometer** and **gyroscope**.

Both sensors are placed parallel to the transverse plane of robot on robot trunk. Gyroscope will _measures angular velocity of the movement of robot body_, and accelerometer will _measures the linear acceleration of robot_. Both sensors are filtered using [Moving Averaging Filter](https://www.analog.com/media/en/technical-documentation/dsp-book/dsp_book_ch15.pdf) to refine the sensor readings.

**[⬆ Back to top](#humanoid-robots)**

### Data collection

Humanoid robot are still in development stage. Therefore, data collection is important to improve the robot's performance.

#### Data collection sensors example

| Sensor type                     | Usage                                                                                                                                                                             |
| ------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Camera                          | Collecting visual data. _For example, in Sophia robot, she equipped with Intel RealSense camera. Custom wide-angle 1080p on her chest and two custom 720p HD camera on her eyes._ |
| Microphone                      | Collecting audio data                                                                                                                                                             |
| Lidar                           | Capturing 3D depth information of the surroundings                                                                                                                                |
| Inertial Measurement Unit (IMU) | Collecting data on acceleration, orientation, and angular velocity of the robot                                                                                                   |
| GPS                             | Providing global positioning data for outdoor navigation                                                                                                                          |
| Force/Torque Sensor             | Measuring contact forces and torques during interactions                                                                                                                          |
| Pressure Sensor                 | Detecting pressure changes or variations in the environment                                                                                                                       |
| Proximity Sensor                | Sensing the presence or proximity of objects or obstacles                                                                                                                         |
| Range Sensor                    | Measuring distances to objects or surfaces                                                                                                                                        |

Example: Tesla Bot uses various sensors to control the motor torque based on the surface.

![Tesla Torque Control](https://github.com/iqfareez/MCTE-4362-Robotic-Hardware/assets/60868965/8578c5e2-478f-4fb7-b362-b6b78283ef28)

**[⬆ Back to top](#humanoid-robots)**

### Data Communication

Data communication is important for humanoid robot to communicate with other devices. This can be done using typical **wireless communication** such as **WiFi**, **Bluetooth**, **Zigbee**, **RFID**, **NFC**, **IR**, and so on.

For example, Asimo robot can communicate with IC Communication to such various things as shown below.

![IC Communication Card ASIMO Robot](https://github.com/iqfareez/MCTE-4362-Robotic-Hardware/assets/60868965/5f43e1a9-05ac-4b4b-af4a-a40d5e05d726)

[[_Source_]](https://asimo.honda.com/downloads/pdf/asimo-technical-information.pdf)

**[⬆ Back to top](#humanoid-robots)**

### Power management

Humanoid robot requires a lot of power to operate. Therefore, power management is important to ensure the robot can operate for a long time. This can be done using **batteries** and **power management system**.

ASIMO robot is powered by a **51.8 V** lithium-ion battery. Here are some specs:

- SIMO can operate for approximately 1 hour on a single battery.
- About 3 hours are required to completely recharge ASIMO’s battery.
- ASIMO’s battery weighs about 13 pounds (6 kg), and is located in its backpack.
- The battery can be recharged onboard ASIMO through a power connection, or the battery can be removed and charged externally.
- A new battery charging station was developed for ASIMO’s autonomous recharging. When the remaining battery level falls below a certain level, ASIMO will automatically identify and walk to the closest available battery charging station and re-charge while standing. See figure below. [^4]

![New autonomous battery charging function](https://github.com/iqfareez/MCTE-4362-Robotic-Hardware/assets/60868965/68dd3092-9ddd-472e-8d73-bfc7f60c2b37)

<sup>Idk but he looks uncomfortable</sup>

**[⬆ Back to top](#humanoid-robots)**

[^2]: https://asimo.honda.com/asimo-specs/
[^3]: https://www.wevolver.com/specs/sophia-a-realistic-humanoid-robot
[^4]: https://global.honda/newsroom/news/2007/c071211-eng.html
