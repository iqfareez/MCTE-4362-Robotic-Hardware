[![Download as PDF](https://img.shields.io/badge/Download%20as%20PDF-EF3939?style=flat-square&logo=adobeacrobatreader&logoColor=white&color=black&labelColor=ec1c24)](https://mdtopdf.up.railway.app/convertPdf?url=https://github.com/iqfareez/MCTE-4362-Robotic-Hardware/blob/main/Week6/AGV-AMR.md)
![Assignment completion](https://img.shields.io/badge/Status-Completed-green?style=flat-square)

# Automated Guided Vehicle (AGV) & Autonomous Mobile Robot (AMR)

## Table of Contents

- [Introduction - AGV vs AMR](#introduction---agv-vs-amr)
- [History of AGV/AMR](#history-of-agvamr)
- [Applications of AGV/AMR](#applications-of-agvamr)
- [Main components of the robot](#main-components-of-the-vehicle)
  - [Body design](#body-design)
  - [Locomotion](#Locomotion)
  - [Navigation](#navigation)
  - [Data collection](#data-collection)
  - [Data transmission](#data-transmission)
  - [Power management](#power-management)

## Introduction - AGV vs AMR

**Automated Guided Vehicle (AGV)** follow a fixed path and can handle heavy loads, while **Autonomous Mobile Robot (AMR)** are more flexible, can navigate autonomously, and adapt to changing environments. AMRs are smaller, more agile, and can handle both large and small loads. It moves/navigates through maps built by its software or pre-loaded drawings. Both designs are featured with obstacle detection and avoidance capability.

Some key differences of AGV & AMR:
| Features | AGV | AMR |
| --- | --- | --- |
| :control_knobs: Control system and sensors | Simpler than AMR | More sophisticated than AGV |
| :money_with_wings: Cost | In some cases, less expensive | Can be more expensive than AGV |
| :compass: Navigation | Primarily follow fixed infrastructure | Freely navigate operational space |
| :package: Payload capacity | Can carry extreme payloads | Payload capacity may be limited |
| :round_pushpin: Localization | Follow fixed infrastructure | AMR manufacturers have a variety of methods to keep their machines “localized” |
| :1st_place_medal: Best application | Work best in well defined conditions such as material handling | Work best in unstructured environments such as security, deliveries, and person to goods intralogistics |

![amr vs agv image](https://cssi.com/wp-content/uploads/AMR-vs-AGV-768x461.png)

**[⬆ Back to top](#automated-guided-vehicle-agv--autonomous-mobile-robot-amr)**

### History of AGV:

- The first AGVs were introduced to industry in the 1950s, by Barrett Electronics of Northbrook, Illinois.

  ![first agv](https://www.fredagv.com/hubfs/Imported_Blog_Media/asi-barrett-agv-1950s-300x300.jpg)

- Developed in mid-20th century for industrial manufacturing environments
- AGV is also called **laser guided vehicle (LGV)**
- First AGVs were automated carts that followed physical wire or magnetic tape on the floor
- Evolved to include more advanced navigation technologies, such as laser and vision-based guidance systems
- Used in a wide range of industries today, including automotive manufacturing, food and beverage production, and logistics

### History of AMR:

- First commercial models introduced in the 2000s
- Initially used in manufacturing and logistics, but now adopted in a range of other applications, such as healthcare, hospitality, and retail
- Advances in sensor technology and artificial intelligence have enabled AMRs to navigate complex and dynamic environments

The **first automotic lawnmower, Mowbot**, introduced in 1969.

![mowbot](https://s.yimg.com/uu/api/res/1.2/6fUhqjyz.49ODQqZ_dmsRQ--~B/aD04MDA7dz02MDE7YXBwaWQ9eXRhY2h5b24-/https://www.blogcdn.com/slideshows/images/slides/312/161/3/S3121613/slug/l/mowbot1969-800-1.jpg)

**[⬆ Back to top](#automated-guided-vehicle-agv--autonomous-mobile-robot-amr)**

## Applications of AGV/AMR

Some of the applications of AGV/AMR are listed below:

<table>
  <thead>
    <tr>
      <th>Application of AGV/AMR</th>
      <th>Description</th>
      <th>Examples</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Manufacturing processes automation</td>
      <td>Automating material handling and transportation in manufacturing processes to improve efficiency and reduce errors.</td>
      <td>Transporting raw materials and finished products in a factory, moving products between assembly stations.</td>
    </tr>
    <tr>
      <td>Warehousing and logistics</td>
      <td>Automating the movement of goods in warehouses and distribution centers to reduce labor costs and increase efficiency.</td>
      <td>
      <p>Inside Amazon's Smart Warehouse (Robot Kiva & Pegasus)</p>
      <a href="https://www.youtube.com/watch?v=IMPbKVb8y8s">
      <img src="https://markdown-videos.deta.dev/youtube/IMPbKVb8y8s" alt="Inside Amazon's Smart Warehouse [YouTube]">
      </a>
      </td>
    </tr>
    <tr>
      <td>Healthcare material transport</td>
      <td>Automating the delivery of medical supplies, equipment, and patient records in healthcare facilities to improve efficiency and reduce human error.</td>
      <td>
      <p>
      A team of Malaysian scientists from International Islamic University Malaysia has created <strong>Medibot</strong> to help medical frontliners care for COVID-19 patients
      </p>
      <img src="https://cute.iium.edu.my/images/2020/09/10/WhatsApp%20Image%202020-09-10%20at%2012.14.03%20PM.jpeg">
      </td>
    </tr>
    <tr>
      <td>Agriculture and farming</td>
      <td>Automating material handling and transportation in agriculture and farming operations to improve efficiency and reduce labor costs.</td>
      <td>
      <p>Meraque Unveils RACE, Malaysia’s First Plantation Autonomous Ground Vehicle (AGV)</p>
      <img src="https://i.newscdn.net/publisher-c1a3f893382d2b2f8a9aa22a654d9c97/2022/08/76a27725c3d061dd81215d3f5921dee8.png=s800"><br/>
      <a href="https://www.malaysiakini.com/announcement/631279">[Source]</a>
      </td>
    </tr>
  </tbody>
<table>

**[⬆ Back to top](#automated-guided-vehicle-agv--autonomous-mobile-robot-amr)**

## Main components of the robot

### Body design

**AGVs** come in several varietirs, depends on each use cases:

| Main types | Description                                                                                                                                                                                                                        | Example                                                                                                         |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| Carts      | Low-profile carts with a storage structure mounted on top containing various materials or items. It moves around the facility and stops where the materials are needed.                                                            | ![Cart AGV](https://www.conger.com/wp-content/uploads/2022/05/toyota-agv-cart-2.jpg)                            |
| Tugger     | Similar to carts, but they have a tow bar that can be used to pull other non-powered carts or containers.                                                                                                                          | ![Tugger AGV](https://www.jbtc.com/automated-systems/wp-content/uploads/sites/6/2021/08/Industries-FoodBev.jpg) |
| Forklift   | Similar to tugger AGVs, but they have a forklift attachment that can be used to lift and move pallets. They’re used to automatically move and stack products like paper rolls, coils, and even vehicles.                           | ![Forklift AGV](https://imgur.com/qwaz1jK.png)                                                                  |
| Unit-load  | An automated to transport single products. It have large surface area to load items such as a pallet or a bin containing products.                                                                                                 | ![Unit-load AGV](https://www.conger.com/wp-content/uploads/2022/05/agv-unit-load.jpg)                           |
| Heavy-haul | The most robust type, featuring sturdy bases, durable wheels, and large platforms, and built to handle up to 250,000 lbs. They are designed to transport heavy loads such as large machinery, vehicles, and other heavy equipment. | ![Heavy-haul AGV](https://www.conger.com/wp-content/uploads/2022/05/heavy-haul-agv.jpg)                         |

On the other hands, **AMRs** shared similar body design with AGVs, but with some differences:

- AMRs have a more compact and mobile design with a smaller footprint.
- AMRs are designed for flexibility and agility in navigating through changing environments.
- AMRs have a modular design, with the ability to add or remove components depending on the task at hand.
- AMRs have a more user-friendly interface such as touchscreens or mobile apps for easier programming and monitoring of performance.
- Below are some examples:

| Main types         | Description                                                                                                                                                                                                                                                                                       | Example                                                                                                                                                                            |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Box-shaped         | This is a simple and common body type for AMRs. It is typically used for indoor applications where the robot needs to carry payloads, such as goods, parts or tools. The box shape provides ample space to store the payload and also allows for easy integration of various sensors and cameras. | ![box amr](https://www.techzine.eu/wp-content/uploads/2022/12/shutterstock_1964618788-1-768x512.jpg)                                                                               |
| Cylindrical-shaped | This body type is used for AMRs that need to navigate through tight spaces or areas with many obstacles. The cylindrical shape allows the robot to easily move around and avoid obstacles without getting stuck. This type of AMR is commonly used in hospitals or restaurants.                   | ![cylindrical amr](https://setthetables.com/wp-content/uploads/2022/11/%E8%B4%9D%E6%8B%89-%E6%B3%B0%E5%9B%BD%E8%8F%9CJohnnys-%E9%A9%AC%E6%9D%A5%E8%A5%BF%E4%BA%9A-11-1-scaled.jpg) |

**[⬆ Back to top](#automated-guided-vehicle-agv--autonomous-mobile-robot-amr)**

### Locomotion

~ refers to their ability to move from one location to another. Below are the types of locomotion used in AGVs/AMRs. All of the robots moves using electrical motors.

<table>
  <tr>
    <th>Motor type</th>
    <th>Description</th>
    <th>Usage</th>
    <th>Example</th>
  </tr>
  <tr>
    <td>Omni-directional</td>
    <td>Multiple small wheels or rollers arranged at an angle to the main axis of the robot, allowing movement in any direction</td>
    <td>Indoor environments with crowded spaces</td>
    <td>
    <p>Wheels Omni Wheel Robot 152mm 30kg</p>
    <img src="https://s.alicdn.com/@sc04/kf/Hb2278b5495574760a7197f171a14a16e9.jpg_960x960.jpg"/>
    </td>
  </tr>
    <tr>
    <td>Mecanum wheels</td>
    <td>Multiple small rollers mounted on the rim of the wheel at a diagonal angle, allowing movement in any direction</td>
    <td>Indoor environments with crowded spaces</td>
    <td>
    <p>RoboCT AGV</p>
    <img src="https://m.media-amazon.com/images/I/51aFnx5DQ6L._SX425_.jpg"/>
    </td>
  </tr>
  <tr>
    <td>Differential drive</td>
    <td>Driven independently by two separate motors, allowing the robot to turn by driving one wheel faster than the other</td>
    <td>Outdoor environments or rough terrain</td>
    <td>
    <p>DieQua’s Compact Drive and Steering Solutions</p>
    <img src="https://user-images.githubusercontent.com/60868965/231372606-9234b09d-baad-4f75-ac80-1e44cb80c118.png"/>
    </td>
  </tr>
  <tr>
    <td>Swerve drive</td>
    <td>Each wheel is mounted on a separate swiveling mechanism, allowing the robot to turn by changing the direction of wheels</td>
    <td>High-speed and precise maneuverability required</td>
    <td>
    <p>SDS MK4 Swerve Modules</p>
    <img src="https://cdn.andymark.com/product_images/mk4-swerve-modules/63a09d50e4dd4f0142b035e0/detail.jpg?c=1671470416"/>
    </td>
  </tr>
</table>

**[⬆ Back to top](#automated-guided-vehicle-agv--autonomous-mobile-robot-amr)**

### Navigation

AGVs typically rely on pre-defined paths or routes that are physically marked on the ground or other infrastructure, such as magnetic tape, painted lines, QR code stickers or laser targets.

The AGV follows these paths and uses **optical sensors** to detect deviations from the path and make corrections. Some AGVs may use onboard sensors to detect obstacles and avoid collisions. AGVs are best suited for **well-defined environments** with fixed infrastructure, such as manufacturing facilities, warehouses, and airports.

#### AGV - Line Navigation

Differences between painted line, Data Matrix line, and Data Matrix Grid:

1. For painted/magnetic line, the AGV **simply follow** this line.

   ![AGV line](https://user-images.githubusercontent.com/60868965/231026410-b753c700-0001-4a36-987a-01fc687db749.gif)

   The magnetic sensor is installed on the bottom of the AGV.

   ![Magentic sensor AGV](https://www.agvnetwork.com/images/technology/Sensors/agv_with_magnetic_sensor_for_navigation.jpg)

2. For Data Matrix line, the AGV will follow the line and detect the code to know its **current precise positions**.

   ![AGV Data matrix](https://user-images.githubusercontent.com/60868965/231026754-1eb01605-f5c1-415a-993e-d12381e0ae80.gif)

3. For Data Matrix Grid, the AGV will go from one point to another point and detect the code to know its **current precise positions**. The sensor need to be accurate as possible to move the robot to the correct directions.

   ![AGV Grid matrix](https://user-images.githubusercontent.com/60868965/231027208-fbfd82fd-a547-49ac-b372-7b8da1820cbe.gif)

#### AGV - Laser Navigation (LGV)

This robot used 360° horizontal 2D LiDAR scanner to detect reflector marks within its environment. The onboard computer performs necessary calculations to determine the robot’s position and orientation. The robot then uses this information to navigate through the environment.

![LGV Laser](https://www.agvnetwork.com/images/technology/Sensors/2d_lidar_for_navigation.jpg)

To learn more about LGV, visit [here](https://www.agvnetwork.com/what-is-a-laser-guided-vehicle-lgv).

#### AGV - Natural Navigation

This robot uses **natural landmarks** such as walls, pillars, and other objects to detect its environment and localize itself. It uses **sensors** such as cameras, lidar, and ultrasonic sensors to detect obstacles and avoid collisions.

![natural navigation](https://www.agvnetwork.com/images/technology/Sensors/2d_lidar_for_natural_navigation.jpg)

**[⬆ Back to top](#automated-guided-vehicle-agv--autonomous-mobile-robot-amr)**

#### AMR Navigation

AMRs are designed to navigate through **dynamic environments** with changing infrastructure. It detects its enviroments and localization using natural landmarks. They are equipped with **sensors** such as cameras, lidar, and ultrasonic sensors to detect obstacles and avoid collisions.

AMRs often use **[SLAM](https://www.mathworks.com/discovery/slam.html) (Simultaneous Localization and Mapping)** techniques in their navigation system. The robot collects sensor data from its surroundings and uses that data to build a map of the environment. At the same time, it uses that data to estimate its own position within the map.

As the robot moves through the environment, it continuously updates the map and refines its position estimate.

Example of the robot 'read' its environment and localize itself using camera and lidar.

![AMR Lidar](https://user-images.githubusercontent.com/60868965/231027894-e2a1bbc4-5c57-4a65-adaa-753963179b40.gif)

Below are some **crucial sensors** that an AGV/AMR needs to have:

<table>
  <tr>
    <th>Sensor</th>
    <th>Description</th>
    <th>Example</th>
  </tr>
  <tr>
    <td>LiDAR</td>
    <td>Emit laser beams and use the reflection of those beams to create a 3D map of the robot's environment. They are often used for mapping, localization, and obstacle detection.</td>
    <td>
    <a href="https://my.cytron.io/p-rplidar-s1-portable-tof-laser-scanner-kit-40m">RPLiDAR S1 Portable ToF Laser Scanner Kit-40M</a>
    <img src="https://static.cytron.io/image/cache/catalog/products/SN-LIDAR-S1/SN-LIDAR-S1_a-512x512.jpg">
    </td>
  </tr>
  <tr>
    <td>Cameras</td>
    <td>They can be used to capture images of the environment that can be processed to create a map, and can also be used to track visual features to determine the robot's position.</td>
    <td>
    <a href="https://www.stereolabs.com/zed-2i/">ZED 2i</a>
    <img src="https://user-images.githubusercontent.com/60868965/231380462-2327795f-d036-46e9-9b28-4813c281c38d.png">
    </td>
  </tr>
  <tr>
    <td>Inertial Measurement Units (IMUs)</td>
    <td>Measure the robot's acceleration and rotation. They are often used in combination with other sensors, such as lidar and cameras, to improve localization accuracy.</td>
    <td>
    <a href="https://my.rs-online.com/web/p/motion-sensor-ics/2496721">STMicroelectronics ASM330LHHX IMU</a>
    <img src="https://encrypted-tbn0.gstatic.com/shopping?q=tbn:ANd9GcQyNIQoYjJkz4wSrK-NgdqmWTTEByaxLz3DdVhl0flZf2mkuqxEtXHti3JuUF0N7WkwHxs4xbnb&usqp=CAc">    
    </td>
  </tr>
  <tr>
    <td>Ultrasonic Sensors</td>
    <td>Use sound waves to detect obstacles in the robot's path. They are often used for close-range obstacle detection.</td>
    <td>
    <a href="https://my.rs-online.com/web/p/reflective-optical-sensors/6666577">GP2Y0A710K0F Sharp</a>
    <img src="https://user-images.githubusercontent.com/60868965/231381600-5dab5010-9f31-4526-82cc-627b6756e81d.png">
    </td>
  </tr>
  <tr>
    <td>Proximity Sensors</td>
    <td>Detect the presence of objects in the robot's immediate vicinity. They can be used for obstacle detection and to determine the distance between the robot and other objects.</td>
    <td>Omron E2E2-X5C1 Proximity Sensor
    <img src="https://assets.omron.com/m/4b4fc4a4021f0778/Landscape_M-IMG_Product_E2E_NEXT_group_380x214.jpg">
    </td>
  </tr>
  <tr>
    <td>Wheel Encoders</td>
    <td>Wheel encoders measure the rotation of the robot's wheels. They can be used to estimate the robot's position and calculate its speed and direction of travel.</td>
    <td>
    <a href="https://www.sparkfun.com/products/12629">Wheel Encoder Kit</a>
    <img src="https://cdn.sparkfun.com//assets/parts/9/3/1/1/12629-01.jpg">
    </td>
  </tr>
</table>

#### AGV Traffic Control

In brief, traffic control measures include zone control, collision avoidance or a mix of both:

| Traffic Control         | Description                                                                                                                                                                                                                             |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Zone Control**        | The AGV is assigned a **specific zone to operate in**. The AGV will not leave the zone unless it is instructed to do so. A wireless transmitter transmits signals in defined areas to determine whether a given area is 'clear' or not. |
| **Collision Avoidance** | The AGV will avoid collisions with other AGVs and obstacles. The AGV contains sensors that transmit a signal and wait for a reply to determine if an object is in front of it.                                                          |
| **Combination Control** | The AGV will operate in a specific zone and avoid collisions with other AGVs and obstacles. This is the most robust system                                                                                                              |

Read more about traffic control [here](https://6river.com/what-are-automated-guided-vehicles/#:~:text=in%20any%20direction.-,AGV%20traffic%20control,-Traffic%20control%20measures).

**[⬆ Back to top](#automated-guided-vehicle-agv--autonomous-mobile-robot-amr)**

### Data Collection

The data that the robot collects depends on its applications. Below are some examples:

- **Environment data:** Camera, Lidar etc are used to do mapping, location of items etc. This data is used to improve the robot accuracy in navigation.
- **Battery levels:** To keep track of the battery levels and to prevent the robot from running out of battery.
- **Number of stocks available:** To keep track of the number of stocks available in the warehouse.
- Motor drives, laser scanners, localization, traffic, and obstacle interference, etc.

By collecting this data, the trends and patterns can be identified and used to **improve the products** and develop the best possible configuration for any given AGV system. Furthermore, Machine Learning (ML) can come into play to **predicts downtime**, maintenance, and other issues.

**[⬆ Back to top](#automated-guided-vehicle-agv--autonomous-mobile-robot-amr)**

### Data Transmission

The robots constantly sending/receiving data for control, data collection etc. They are are several ways the robot can communicate.

#### Wired Communication

Wired communication is the most common way of communication. It is the most reliable and secure way of communication. It is also the fastest way of communication. However, it is not the most flexible way of communication.

#### Wireless Communication

Wireless communication is the most flexible and convenient way of communication. This can include Wi-Fi, Bluetooth, ZigBee, or other wireless protocols.

![agv communication example](https://user-images.githubusercontent.com/60868965/231385685-ca41357b-4a69-4395-818b-8cd36b83f735.png)

#### RTLS

[Real-Time Location Systems (RTLS)](https://www.atlasrfidstore.com/what-is-rtls-an-introduction-to-real-time-location-systems/) are a type of technology used to track the real-time location of objects or people within a specific environment. The technology is used to track the robot's position within the facility, warehouse or factory in real-time.

All RTLS applications will consist of a few basic components: a transponder, a receiver, and software to interpret the data from each.

<table>
  <thead>
    <tr>
      <th>Transponders</th>
      <th>Receivers</th>
      <th>Software</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <ul>
          <li>Radio-Frequency Identification (RFID) Tags</li>
          <li>Bluetooth Beacons</li>
          <li>Smart Devices</li>
          <li>Wi-Fi Tags</li>
          <li>Global Navigation Satellite System (GNSS)/Global Positioning System (GPS) Tags</li>
          <li>Ultrasound Tags</li>
          <li>Infrared Tags</li>
          <li>Smart Devices (Depending on the Mode)</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Readers</li>
          <li>Location Sensors</li>
          <li>Access Points</li>
          <li>Receivers</li>
          <li>Beacons (Depending on the Mode)</li>
          <li>Smart Devices (Depending on the Mode)</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Firmware - software that resides on the hardware</li>
          <li>Software or application software - software that resides on the back-end computer or server</li>
          <li>Middleware - used to connect firmware and application software</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

**[⬆ Back to top](#automated-guided-vehicle-agv--autonomous-mobile-robot-amr)**

### Power Management

#### Batteries

AGVs are powered by rechargeable batteries. The choice of battery technology depends on factors such as power requirements, operating environment, and lifespan.

Most common battery technology among AGV is Lithium-ion batteries. Lithium Iron Phosphate (LiFePO4) batteries are also gaining popularities in robotics. Below is the example comparison.

<table>
  <thead>
    <tr>
      <th>Lithium-ion</th>
      <th>Lithium Iron Phosphate (LiFePO4)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <ul>
          <li>High energy density</li>
          <li>Fast charging times</li>
          <li>Low self-discharge rate</li>
          <li>High power density</li>
          <li>High operating temperature range</li>
          <li>Low cost</li>
          <li>Example: <a href="https://www.motorsportgoetz.com/Battery-Lithium-YB16AL-A2-YB14L-A2-YB12AL-A2-YV10L-B-12N14-3AYTX14">Battery Lithium YB16AL-A2</a> </li>
          <img src="https://www.motorsportgoetz.com/media/image/product/169322/lg/batterie-lithium-ionen-yt12b-bs-yt14b-bs-yb16al-a2-lit2b-quad-motorrad-roller-mit-led-anzeige_3.jpg">
        </ul>
      </td>
      <td>
        <ul>
          <li>High energy density</li>
          <li>High power density</li>
          <li>High operating temperature range</li>
          <li>Low cost</li>
          <li>Long cycle life</li>
          <li>Low self-discharge rate</li>
          <li>Low maintenance</li>
           <li>Example: <a href="https://discoverbattery.com/products/search/14-24-2800">AES LiFePO4 Industrial Mobile Battery</a> </li>
          <img src="https://img.discoverbattery.com/images/products/03_aes/870_artwork_images/aes-14-24-2800.png">
        </ul>
      </td>
    </tr>
  </tbody>
</table>

A **must have components** for battery-powered AGVs are Battery Management System and onboard charger controller.

#### Charging Infrastructure

AGVs must be able to recharge their batteries in a timely and efficient manner. Below are some examples of charging infrastructure used in industries.

<table>
  <thead>
    <tr>
      <th>Charging Infrastructure</th>
      <th>Example</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
       <strong>Charging Contact</strong>
      </td>
      <td>
      <img src="https://www.agvnetwork.com/images/technology/wireless/AGV_with_opportunity_contact_charging_6.jpg"/>
       <img src="https://user-images.githubusercontent.com/60868965/232446475-e77f3e4c-e579-487b-99b3-8b2afb4f9f6c.png"/>
      </td>
    </tr>
     <tr>
      <td>
       <strong>Wireless Charging</strong> - Usually slower compared to contact charging
      </td>
      <td>
      <img src="https://www.therobotreport.com/wp-content/uploads/2018/01/Delta-Products-in-the-form-of-a-new-93-percent-efficient-wireless-charging-system-for-AGV-Wireless-Power-Solutions.jpg"/>
       <img src="https://roboticsandautomationnews.com/wp-content/uploads/2021/02/versabox-wireless-charging-agv_induktives-laden-fts.jpg"/>
      </td>
    </tr>
  </tbody>
  </table>

**[⬆ Back to top](#automated-guided-vehicle-agv--autonomous-mobile-robot-amr)**
