[![Download as PDF](https://img.shields.io/badge/Download%20as%20PDF-EF3939?style=flat-square&logo=adobeacrobatreader&logoColor=white&color=black&labelColor=ec1c24)](https://mdtopdf.up.railway.app/convertPdf?url=https://github.com/iqfareez/MCTE-4362-Robotic-Hardware/blob/main/Week6/AGV-AMR.md)
![Assignment completion](https://img.shields.io/badge/Status-WIP-yellow?style=flat-square)

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
| Control system and sensors | Simpler than AMR | More sophisticated than AGV |
| Cost | In some cases, less expensive | Can be more expensive than AGV |
| Navigation | Primarily follow fixed infrastructure | Freely navigate operational space |
| Payload capacity | Can carry extreme payloads | Payload capacity may be limited |
| Obstacle avoidance | Can become “stuck” if they come across an object | Actively navigate around obstacles |
| Localization | Follow fixed infrastructure | AMR manufacturers have a variety of methods to keep their machines “localized” |
| Best application | Work best in well defined conditions such as material handling | Work best in unstructured environments such as security, deliveries, and person to goods intralogistics |

![amr vs agv image](https://cssi.com/wp-content/uploads/AMR-vs-AGV-768x461.png)

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

## Main components of the robot

### Body design

**AGVs** come in several varietirs, depends on each use cases:

| Main types | Description                                                                                                                                                                                                                        | Example                                                                                                         |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| Carts      | The simplest AGV material handling machines. They’re low-profile carts with a storage structure mounted on top containing various materials or items. It moves around the facility and stops where the materials are needed.       | ![Cart AGV](https://www.conger.com/wp-content/uploads/2022/05/toyota-agv-cart-2.jpg)                            |
| Tugger     | Tugger AGVs are similar to carts, but they have a tow bar that can be used to pull other non-powered carts or containers.                                                                                                          | ![Tugger AGV](https://www.jbtc.com/automated-systems/wp-content/uploads/sites/6/2021/08/Industries-FoodBev.jpg) |
| Forklift   | Forklift AGVs are similar to tugger AGVs, but they have a forklift attachment that can be used to lift and move pallets. They’re used to automatically move and stack products like paper rolls, coils, and even vehicles.         | ![Forklift AGV](https://imgur.com/qwaz1jK.png)                                                                  |
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
    <img src="https://diequa.com/wp-content/uploads/2022/06/screenshot-differential-drive-main.png"/>
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

### Navigation

#### AGV Navigation

AGVs typically rely on pre-defined paths or routes that are physically marked on the ground or other infrastructure, such as magnetic tape, painted lines, QR code stickers or laser targets.

The AGV follows these paths and uses **optical sensors** to detect deviations from the path and make corrections. Some AGVs may use onboard sensors to detect obstacles and avoid collisions. AGVs are best suited for **well-defined environments** with fixed infrastructure, such as manufacturing facilities, warehouses, and airports.

Differences between painted line, Data Matrix line, and Data Matrix Grid:

1. For painted line, the AGV **simply follow** this line.
   ![AGV line](https://user-images.githubusercontent.com/60868965/231026410-b753c700-0001-4a36-987a-01fc687db749.gif)

2. For Data Matrix line, the AGV will follow the line and detect the code to know its **current precise positions**.
   ![AGV Data matrix](https://user-images.githubusercontent.com/60868965/231026754-1eb01605-f5c1-415a-993e-d12381e0ae80.gif)

3. For Data Matrix Grid, the AGV will go from one point to another point and detect the code to know its **current precise positions**. The sensor need to be accurate as possible to move the robot to the correct directions.
   ![AGV Grid matrix](https://user-images.githubusercontent.com/60868965/231027208-fbfd82fd-a547-49ac-b372-7b8da1820cbe.gif)

#### AMR Navigation

AMRs are designed to navigate through **dynamic environments** with changing infrastructure. It detects its enviroments and localization using natural landmarks. They are equipped with **sensors** such as cameras, lidar, and ultrasonic sensors to detect obstacles and avoid collisions.

Example of the robot 'read' its environment and localize itself using camera and lidar.

![AMR Lidar](https://user-images.githubusercontent.com/60868965/231027894-e2a1bbc4-5c57-4a65-adaa-753963179b40.gif)

### Data Collection
