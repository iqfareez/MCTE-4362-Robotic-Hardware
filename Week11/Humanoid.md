# Humanoid Robots

[![Download as PDF](https://img.shields.io/badge/Download%20as%20PDF-EF3939?style=flat-square&logo=adobeacrobatreader&logoColor=white&color=black&labelColor=ec1c24)](https://mdtopdf.up.railway.app/convertPdf?url=https://github.com/iqfareez/MCTE-4362-Robotic-Hardware/blob/main/Week11/Humanoid.md)
![Assignment completion](https://img.shields.io/badge/Status-In%20progress-yellow?style=flat-square)

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

Humanoid robots are remarkable creations that **closely resemble the human form**, featuring an array of advanced technologies and capabilities. With their human-like appearance and ability to perform intricate tasks, humanoid robots have the potential to revolutionize various industries, from healthcare and entertainment to manufacturing and personal assistance. These robots possess articulated limbs, sophisticated sensors, and artificial intelligence algorithms, enabling them to navigate complex environments, interact with humans, and mimic human gestures and expressions.

![humanoid robots](https://github.com/iqfareez/MCTE-4362-Robotic-Hardware/assets/60868965/f60ae85a-0565-4407-b578-84e538f9d252)

## History [^1]

| Year & Robot Name                    | Description                                                                                                                                                                                                                                                                                                                                                       |                                                                                                 Image                                                                                                  |
| :----------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| **1495 - Leonardo’s Robot**          | An inventor Leonardo da Vinci designed a suit of armour that moved as if there was a real person inside. It was operated by a series of pulleys and cables, it could do various human-like movements. The goal was merely to amuse Milanese royalty, but modern recreations of the device have shown that it was fully functional.                                |                                       ![leonardo image](https://upload.wikimedia.org/wikipedia/commons/thumb/4/45/Leonardo-Robot3.jpg/440px-Leonardo-Robot3.jpg)                                       |
| **1774 - The Jacquet-Droz Automata** | Pierre Jacquet-Droz, his son Henri-Louis, and Jean-Frédéric Leschot created three automata that are still operational today. One is a female robot musician who plays an organ with her fingers, another is a child robot artist capable of drawing four different images, and the third is a child robot writer who can write up to 40 characters using a quill. |                          ![robot image](https://images.squarespace-cdn.com/content/v1/58bb0536893fc04255997b40/1534602058526-D1HXFNZSNJGU0IVWX0G5/Jaquet+Droz+History+4.jpg)                           |
| **1970 - WABOT-1**                   | The first digitally controlled anthropomorphic robot was built at Waseda University in Tokyo. It had a limb-control system with tactile sensors for walking and gripping, a vision system that could measure distances, and a conversation system that could communicate in Japanese.                                                                             |                                                ![image](https://bostonglobalforum.org/aiwsin/wp-content/uploads/sites/18/2021/01/c7d5b.179.large_.jpg)                                                 |
| **2000 - Asimo**                     | Honda designed and developed Asimo as a multi-functional mobile assistant that could help people with poor mobility.                                                                                                                                                                                                                                              | ![asimo robot](https://www.cnet.com/a/img/resize/eda639c60821807e9759bb305152838b58ff5c3e/hub/2014/04/17/94b3b33e-eda0-459d-a5e2-7a75c7b3e80a/485318345.jpg?auto=webp&fit=crop&height=1200&width=1200) |
| **2016 - Sophia**                    | A humanoid robot capable of expressing emotions and holding conversations. It was designed to look like Audrey Hepburn, and has been granted citizenship in Saudi Arabia and the United Arab Emirates.                                                                                                                                                            |                         ![sophia robot](https://upload.wikimedia.org/wikipedia/commons/1/1e/Sophia_at_the_AI_for_Good_Global_Summit_2018_%2827254369347%29_%28cropped%29.jpg)                          |

[^1]: https://www.howwegettonext.com/a-history-of-humanoids

## Main Components of the design

### Body design

A robot resembling the **human body** in shape.

Some examples:

![examples](https://media.springernature.com/lw685/springer-static/image/art%3A10.1007%2Fs43154-021-00050-9/MediaObjects/43154_2021_50_Fig1_HTML.png)

### Locomotion

Most humanoid robot that are designed to move use **legged type locomoation**. Legged locomotion is more versatile and can be used in many different environments. However, legged locomotion is **more complex** than wheeled locomotion, for example.

Example below shows a **3-DoF leg** composed of three links: thigh, shank and hoof, connected through the hip, knee and fetlock joints. The **damper** is also installed on the hip joint to absorb the impact force when the hoof hits the ground.

![image](https://github.com/iqfareez/MCTE-4362-Robotic-Hardware/assets/60868965/6610b7da-5e09-4baf-ac5d-77badf474eec)

#### Actuators that are commonly involved in legged locomotion

| Actuator        | Usage                      |
| --------------- | -------------------------- |
| Electric motor  | Generating leg movement    |
| Hydraulic       | Powering joint movements   |
| Pneumatic       | Controlling leg extension  |
| Servo motor     | Adjusting leg position     |
| Linear actuator | Enabling linear leg motion |
| Force sensor    | Detecting leg force        |

### Navigation

Imitating human ability to walk, jump and run is a challenging task for engineers to design it. The robot must be able to **sense its environment** and **adapt to it**. The robot must also be able to **plan its path** and **avoid obstacles**. Below are some aspects that are involved in navigation:

#### Sensing

The robot must be able to sense its environment. This can be done using **sensors** such as **cameras**, **radars**, **ultrasonic sensors**, **infrared sensors**, **laser sensors** and **GPS**.

#### Planning

The robot must be able to plan its path. This can be done using **algorithms** such as **A\***, **Dijkstra's algorithm**, and so on.

#### Inverse Kinematics

The robot must be able to calculate the **joint angles** required to move the robot to a specific position. The smooth and dynamic robot movement can uses inverse kinematics algorithm. Within robot motion pattern, positioning actuator angle of robot's legs will be determined by the amount of steps in X axis, Y axis, and Z axis robot.

#### Balance Model

Balance controller uses two types of sensors, **accelerometer** and **gyroscope**.

Both sensors are placed parallel to the transverse plane of robot on robot trunk. Gyroscope will _measures angular velocity of the movement of robot body_, and accelerometer will _measures the linear acceleration of robot_. Both sensors are filtered using [Moving Averaging Filter](https://www.analog.com/media/en/technical-documentation/dsp-book/dsp_book_ch15.pdf) to refine the sensor readings.

### Data collection

Humanoid robot are still in development stage. Therefore, data collection is important to improve the robot's performance.

#### Data collection sensors example

| Sensor type                     | Usage                                                                           |
| ------------------------------- | ------------------------------------------------------------------------------- |
| Camera                          | Collecting visual data                                                          |
| Microphone                      | Collecting audio data                                                           |
| Lidar                           | Capturing 3D depth information of the surroundings                              |
| Inertial Measurement Unit (IMU) | Collecting data on acceleration, orientation, and angular velocity of the robot |
| GPS                             | Providing global positioning data for outdoor navigation                        |
| Force/Torque Sensor             | Measuring contact forces and torques during interactions                        |
| Pressure Sensor                 | Detecting pressure changes or variations in the environment                     |
| Proximity Sensor                | Sensing the presence or proximity of objects or obstacles                       |
| Range Sensor                    | Measuring distances to objects or surfaces                                      |

### Power management

Power
