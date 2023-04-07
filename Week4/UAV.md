[![Download as PDF Button](https://img.shields.io/badge/Download%20as%20PDF-EF3939?style=flat-square&logo=adobeacrobatreader&logoColor=white&color=black&labelColor=ec1c24)](https://mdtopdf.up.railway.app/convertPdf?url=https://github.com/iqfareez/MCTE-4362-Robotic-Hardware/blob/main/Week4/UAV.md)
![Assignment completion](https://img.shields.io/badge/Status-Completed-green?style=flat-square)

# Unmanned Aerial Vehicle (UAV)

## Table of Contents

- [History of UAV](#history-of-uav)
- [Applications of UAV](#applications-of-uav)
- [Main components of the vehicle](#main-components-of-the-vehicle)
  - [Airframe design](#airframe-design)
  - [Propulsion](#propulsion)
  - [Navigation](#navigation)
  - [Data collection](#data-collection)
  - [Data transmission](#data-transmission)
  - [Power management](#power-management)
- [Internship experiences](#internship-experiences)

## History of UAV

- Early 1900s: First attempts to create unmanned aircraft
- 1960s-1970s: US military begins using UAVs for reconnaissance missions in Vietnam War
- 1980s: Advances in microelectronics and computer technology lead to development of smaller and more sophisticated UAVs
- 1990s-2000s: UAVs used for military operations in Iraq and Afghanistan, leading to increased interest from various industries
- Recent years: Development of commercial drones for personal and professional use, including photography, surveying, search and rescue, and delivery services. Ongoing advancements in technology continue to improve UAV capabilities and potential uses as discussed below.

## Applications of UAV

<table>
  <tr>
    <th>Application</th>
    <th>Description</th>
    <th>Example</th>
  </tr>
  <tr>
    <td>Agriculture</td>
    <td>
      <ul>
        <li>Crop monitoring and analysis</li>
        <li>Precision agriculture and mapping</li>
        <li>Pest and disease detection</li>
      </ul>
    </td>
    <td>
    Drones are used to spray, seed, and fertilise a paddy crops in Perlis.<br/>
    <img src="https://cilisos.my/wp-content/uploads/2022/09/index-768x1024.jpg" width="300"><br/>
    <a href="https://cilisos.my/meet-nasrun-the-perlis-guy-modernising-paddy-farming-using-drones/">[Source]</a>
    </td>
  </tr>
  <tr>
    <td>Delivery and logistics</td>
    <td>
      <ul>
        <li>Package and parcel delivery</li>
        <li>Inventory management and tracking</li>
      </ul>
    </td>
    <td>Amazon's Prime Air drones are capable of delivering packages weighing up to 5 pounds.
    <a href="https://www.cnet.com/tech/services-and-software/amazon-drone-delivery-happening-in-california-and-texas/">[Source]</a>
    </td>
  </tr>
  <tr>
    <td>Construction and engineering</td>
    <td>
      <ul>
        <li>Site surveying and inspection</li>
        <li>Progress monitoring and reporting</li>
        <li>Infrastructure maintenance and repair</li>
      </ul>
    </td>
    <td>Surveying and inspecting construction sites, monitoring progress and reporting on projects, and conducting infrastructure maintenance and repairs.</td>
  </tr>
 <tr>
    <td>Law enforcement</td>
    <td>
      <ul>
        <li>Surveillance and monitoring</li>
        <li>Traffic management and control</li>
        <li>Investigating crimes and accidents</li>
      </ul>
    </td>
    <td>PDRM using drones to catch highway emergency lane offenders in Ops Selamat 18, roadblocks on PLUS
    <img src="https://user-images.githubusercontent.com/60868965/230009659-a9299273-7237-48f4-b7c6-05dfdf1e86d1.png" />
    <a href="https://paultan.org/2022/05/05/pdrm-using-drones-to-catch-highway-emergency-lane-offenders-in-ops-selamat-18-roadblocks-on-plus">[Source]</a>
        </td>
  </tr>
  <tr>
    <td>Media and entertainment</td>
    <td>
      <ul>
        <li>Cinematography and videography</li>
        <li>Live event coverage and broadcasting</li>
      </ul>
    </td>
    <td>Producing aerial footage for films and television shows, covering live events such as sports and concerts, and broadcasting real-time footage to audiences around the world.</td>
  </tr>
</table>

## Main components of the vehicle

### Airframe design

The UAV can take different forms and shapes. They can ge categorized into several main types:

#### Fixed-wing

![Fixed wing SCS Nyamok Aludra](https://user-images.githubusercontent.com/60868965/229689440-71110f79-977a-40b0-964d-cc81e17c8301.png)

~ are designed to fly in the air like a plane. They are usually used for surveillance, photography, and mapping. They are also used for
military purposes.

<table>
  <tr>
    <th>Advantages</th>
    <th>Disadvantages</th>
  </tr>
  <tr>
    <td>Can cover long distances and stay in the air for extended periods of time</td>
    <td>Require a runway or catapult launch and a parachute or runway landing, making them less flexible for takeoff and landing locations</td>
  </tr>
  <tr>
    <td>Can fly at high speeds and altitudes, making them useful for surveillance and mapping applications</td>
    <td>Cannot hover in one place or fly at low speeds like rotary-wing UAVs, limiting their usefulness for certain applications</td>
  </tr>
  <tr>
    <td>Have a higher payload capacity than most other types of UAVs, making them suitable for carrying larger and heavier sensors and cameras</td>
    <td>Require more complex and expensive maintenance than some other types of UAVs</td>
  </tr>
  <tr>
    <td>Are more energy-efficient than rotary-wing UAVs, allowing them to cover greater distances on less fuel or battery power</td>
    <td>Require a larger operating area than some other types of UAVs, making them less suitable for use in confined spaces</td>
  </tr>
  <tr>
    <td>Are less affected by wind and other environmental factors than rotary-wing UAVs, making them more stable in flight</td>
    <td>Cannot perform vertical takeoff or landing, making them unsuitable for certain applications such as search and rescue or inspection of tall structures</td>
  </tr>
</table>

#### Rotary-wing

![Rotary wing UAV](https://user-images.githubusercontent.com/60868965/229689448-ba750e2b-f128-4528-89f2-2ad8d3b1f91e.png)

~ also known as a rotorcraft. They are designed to fly like a helicopter. Rotary-wing UAVs tend to be larger and more complex

<table>
  <tr>
    <th>Advantages</th>
    <th>Disadvantages</th>
  </tr>
  <tr>
    <td>Can take off and land vertically, making them highly flexible for takeoff and landing locations</td>
    <td>Have a shorter flight time than fixed-wing UAVs, limiting their range and endurance</td>
  </tr>
  <tr>
    <td>Can hover in one place or fly at low speeds, making them ideal for applications such as search and rescue, inspection of tall structures, and close-range surveillance</td>
    <td>Are more affected by wind and other environmental factors than fixed-wing UAVs, making them less stable in flight</td>
  </tr>
  <tr>
    <td>Are more maneuverable than fixed-wing UAVs, allowing them to fly in confined spaces and perform precise movements</td>
    <td>Have a lower payload capacity than fixed-wing UAVs, limiting their ability to carry heavy sensors and equipment</td>
  </tr>
  <tr>
    <td>Do not require a runway or catapult launch, making them highly flexible for takeoff and landing locations</td>
    <td>Are less energy-efficient than fixed-wing UAVs, requiring more frequent battery or fuel replacements during missions</td>
  </tr>
  <tr>
    <td>Can perform vertical takeoff and landing, making them suitable for certain applications such as search and rescue and inspection of tall structures</td>
    <td>Are often more expensive to purchase and maintain than fixed-wing UAVs</td>
  </tr>
</table>

#### Multirotor

![Multirotor skyfront dji](https://user-images.githubusercontent.com/60868965/229689445-9f3b24be-3503-4c10-83b1-9061a3008611.png)

~ uses multiple rotors to generate lift and propulsion. They can have different configurations, with three, four, six, or eight rotors being the most common.

<table>
  <tr>
    <th>Advantages</th>
    <th>Disadvantages</th>
  </tr>
  <tr>
    <td>Can fly in place or at low speeds, making them useful for precise positioning and maneuvering</td>
    <td>Shorter flight time than other types of UAVs</td>
  </tr>
  <tr>
    <td>Simple to operate and maintain</td>
    <td>Cannot fly as far or as fast as fixed-wing UAVs</td>
  </tr>
  <tr>
    <td>Can take off and land vertically, allowing them to be used in a variety of locations</td>
    <td>Limited payload capacity, making them less suitable for carrying heavy sensors or equipment</td>
  </tr>
  <tr>
    <td>Can be equipped with cameras and other sensors to capture high-quality images and data</td>
    <td>Affected by wind and other environmental factors, which can make them less stable in flight</td>
  </tr>
  <tr>
    <td>Relatively inexpensive compared to other types of UAVs</td>
    <td>Noisy compared to other types of UAVs, which can be disruptive in certain environments</td>
  </tr>
</table>

#### Hybrid

![SCS Nyamok VTOL Hybrid](https://user-images.githubusercontent.com/60868965/229689451-0c34f649-1cca-4add-b742-b57824ce5430.png)

~ UAV combines the features and capabilities of both fixed-wing and rotary-wing UAVs.

Hybrid UAVs can be configured in different ways, but most designs feature a tilt-rotor or tilt-wing mechanism that allows the UAV to transition between hovering and forward flight modes. Some hybrid UAVs also use a combination of electric and combustion engines to power their rotors and fixed wings.

<table>
  <tr>
    <th>Advantages</th>
    <th>Disadvantages</th>
  </tr>
  <tr>
    <td>Can take off and land vertically, allowing them to operate in tight spaces</td>
    <td>More complex and expensive than other types of UAVs</td>
  </tr>
  <tr>
    <td>Can transition to fixed-wing flight for longer endurance and greater range</td>
    <td>Requires specialized training and maintenance</td>
  </tr>
  <tr>
    <td>Can combine the benefits of both fixed-wing and rotary-wing UAVs</td>
    <td>Added weight and complexity of the tilt-rotor or tilt-wing mechanism can reduce payload capacity</td>
  </tr>
</table>

### Propulsion

<table>
  <tr>
    <th>Propulsion Type</th>
    <th>Pros</th>
    <th>Cons</th>
    <th>Example UAV</th>
  </tr>
  <tr>
    <td>Electric</td>
    <td>Quiet, efficient, low emissions</td>
    <td>Shorter flight times, limited payload capacity</td>
    <td>
    <img src="https://dji-official-fe.djicdn.com/dps/fa9086cc12f8187ba6462bb0df2dc881@origin.jpg" /><br/>
    <a href="https://www.dji.com/mavic-3">DJI Mavic 3</a>
    </td>
  </tr>
  <tr>
    <td>Gasoline</td>
    <td>More power, longer flight times</td>
    <td>Louder, more emissions</td>
    <td>
      <img src="https://www.insitu.com/wp-content/uploads/2020/11/SE_Gallery_04.jpg"/><br/>
      <a href="https://www.insitu.com/products/scaneagle">Insitu ScanEagle</a>
      </td>
  </tr>
  <tr>
    <td>Jet</td>
    <td>High speeds, high altitude capabilities</td>
    <td>Louder, more expensive to operate</td>
    <td>
    <img src="https://i.guim.co.uk/img/media/94122807825fb1ee6eabb011645551731a32341a/224_101_6409_3848/master/6409.jpg?width=1200&height=900&quality=85&auto=format&fit=crop&s=65f66cc0768f61b17adfda2a53067270"/><br/>
    <a href="https://www.ga-asi.com/remotely-piloted-aircraft/mq-9a">General Atomics MQ-9 Reaper</a>
    </td>
  </tr>
  <tr>
    <td>Hybrid</td>
    <td>Flexible, efficient</td>
    <td>More complex, higher cost</td>
    <td>
    <img src="https://www.aerocontact.com/public/img/aviaexpo/produits/images/471/detail_Phantom-Eye-1.jpg"/><br/>
    <a href="https://www.boeing.com/defense/phantom-eye/">Boeing Phantom Eye</a>
    </td>
  </tr>
  <tr>
    <td>Solar</td>
    <td>Unlimited flight times, environmentally friendly</td>
    <td>Slower, limited payload capacity</td>
    <td>
    <img src="https://www.airforce-technology.com/wp-content/uploads/sites/6/2017/09/5-zephyr.jpg" /><br/>
    <a href="https://www.airbus.com/en/products-services/defence/uas/uas-solutions/zephyr">QinetiQ Zephyr</a>
    </td>
  </tr>
</table>

#### Notes

- **Hybrid** propulsion systems combine two or more types of propulsion, such as electric and gasoline or electric and solar, to provide greater flexibility and efficiency. Hybrid UAVs **can switch between different propulsion systems** depending on the mission requirements, allowing them to optimize performance and range.
- **Gasoline** propulsion systems use gasoline as their primary fuel source, whereas **jet** propulsion systems typically use kerosene-based fuels, such as Jet A or Jet A-1.

### Navigation

Skyfront Perimeter 8 can be controlled manually, using **remote control**, or autonomously, using **SkyfrontGCS software**

Supported flight mode for Skyfront Perimeter 8 is shown as follows:

<table>
  <tr>
    <th>Manual through remote controller</th>
    <th>GPS-based waypoint autonomy</th>
  </tr>
  <tr>
    <td>Stabilize</td>
    <td>Survey</td>
  </tr>
  <tr>
    <td>Altitude (barometer- and GPS-based)</td>
    <td>Waypoint navigation and payload control</td>
  </tr>
  <tr>
    <td>Position (GPS-based)</td>
    <td>Automatic land and takeoff</td>
  </tr>
</table>

**Autopilot firmware** - Perimeter 8 equipped with Janus Autopilot (Proprietary) - [PX4](https://px4.io/) based.

> PX4 is an open-source flight control software stack designed for autonomous drones and other unmanned aerial vehicles (UAVs). It provides a complete set of software tools and algorithms for controlling the flight of drones, including stabilization, guidance, and navigation.

**Autopilot electronics** - Pixhawk

<img src="https://docs.px4.io/v1.9.0/assets/flight_controller/pixhawk4/pixhawk4_logo_view.jpg" width="500">

Below is the example of the **RC** used.

<img src="https://static.cytron.io/image/cache/catalog/products/FS-I6-M2/FS-I6-M2-800x800.jpg" width="350">

_p/s: it is not really FlySky brand, but it is similar!_

Alternatively, the flight path can be planned using **SkyfrontGCS** software. The software is able to plan the flight path, and send the flight path to the UAV. The UAV will then follow the flight path autonomously. The software is based on the Mission Control software I believe. The software also able to receive data from the UAV (temp, altitude etc.).

https://user-images.githubusercontent.com/60868965/229836388-35f5a503-1748-4116-b04f-bd242598d7d0.mp4

On the other hands, **DJI drones** can use [DJI Smart Controller](https://www.dji.com/rc?site=brandsite&from=eol_smart-controller). This controller is able to control the drones and also receive live broadcast from the drone's camera.

<img src="https://dji-official-fe.djicdn.com/dps/5919beda1853e73f3db4c2d3ea0f695c.jpg" width="500"/>

### Data Collection

Data that are collected by the UAV are varies to its use cases. However, below is the most common data that are collected by the UAV.

- Aerial imagery (RGB): Captured by high-resolution cameras such as the [Sony RX1R II](https://wingtra.com/mapping-drone-wingtraone/mapping-cameras/sony-rx1r-ii/).
- Thermal imagery (IR): Captured by thermal cameras such as the [DJI Zenmuse H20N](https://www.dji.com/zenmuse-h20n?site=brandsite&from=eol_zenmuse-xt2) (nightvision)
- LiDAR data: Captured by LiDAR sensors such as the [Velodyne Puck LITE](https://velodynelidar.com/products/puck-lite/)
- Atmospheric data: Captured by sensors such as the [Sensirion SHT31](https://sensirion.com/products/catalog/SEK-SHT31) or the Bosch BME280
- Video data: Captured by cameras similar to those used for aerial imagery, or specialized cameras such as the DJI Zenmuse Z30 or [GoPro](https://gopro.com/en/us/) for zooming capabilities.

### Data Transmission

Below is setup for Skyfront Perimeter 8 including the GCS and the antenna.

![GCS Skyfront antenna](https://skyfront.com/wp-content/uploads/2022/05/Edited-nobg-CP1A0582-1536x1189.png)

However, we used somewhat different antenna model

![Skyfront antenna](https://user-images.githubusercontent.com/60868965/230003919-0e024fd9-f19a-40fa-bd48-dfef584d588e.png)

The antenna is able to transmit data to and from the ground station. The data is then processed by the ground station and displayed on the screen. The connection between GCS and the antenna is by using **ethernet** RJ45 cable.

It is reported that the telemetry can reach 10 - 100 km.

For Perimeter 8, it is possible to add payload such as camera etc, however, the telecommunication system need to be added seperately from 3rd party providers. One popular choices is from [Microhard](https://www.microhardcorp.com/).

Example:

![n920X2](https://www.microhardcorp.com/images/products/detail_n920X2_OEM_top.jpg)

### Power Management

#### Battery

In Mavic 3, it uses LiPo Battery to power the UAV. The battery specifications are as follows:

- **Capacity**: 5000 mAh
- **Voltage**: 15.4 V
- **Charging Voltage Limit**: 17.6 V
- **Battery Type**: Li-ion 4S
- **Energy**: 77 Wh

<img src="https://user-images.githubusercontent.com/60868965/230261800-4d72ff90-07a2-41cf-b57e-c4cce9d07c02.png" width=" 400">

#### Engine/Hybrid

Skyfront perimeter 8 have some features regarding the power management.

- The Skyfront Perimeter 8 UAV is** powered by its engine** and equipped with a **backup battery** for emergency use.
- The battery is responsible for starting the engine and can sustain the UAV for only 3-5 minutes, which is enough time to land the vehicle and payload safely.
- Despite the engine powering the electronics, the battery is not involved in providing power.
- The UAV features a **fully redundant power system** that can operate on battery power in case of an engine failure.
- The Engine Wear Protection feature ensures that the engine operates continuously at less than 70% of its maximum power to prevent wear and tear.

Image below shows the fuel (red colour) that just been refilled into the tank prior the mission.

![Skyfront perimeter 8 fuel tank](https://user-images.githubusercontent.com/60868965/230523393-3b4cbfcf-50bd-4188-80a7-83717bbd5406.png)

- The fuel used is G2K proprietary hybrid gasoline-electric propulsion system. The engine is quite loud while operating (just like the lawn mower's engine)
- The battery is Lithium Polymer 3s (2x)
- With payload, the UAV can fly for 1-2.5 hours. But, without payload, the UAV can fly up to 6 hours!

On the other hands, [ScanEagle 3](https://www.insitu.com/wp-content/uploads/2020/12/ScanEagle3_ProductCard_DU120320.pdf) also equipped with electric hybrid engine for missions that equire increased available power and a low acoustic signature

The endurance can go up to 18 hours. Engine & fuel type: Heavy fuel (JP-5/JP-8)

## Internship experiences

<img src="https://user-images.githubusercontent.com/60868965/229862747-6af2d5a5-efc7-4e0a-8a2c-ee1d60618f76.png" width="100" />

In my 3 months of Internship at System Consultancy Services (SCS), I joined several mission related to UAV.

On August 2022, we had planned to conduct flight endurance test for the company's UAV - Skyfront Perimeter 8. The location of the mission is Pulau Indah, Perak. The site is clear and wide, made it suitable for a UAV pilots who want to test their drones.

![Skyfront cover](https://user-images.githubusercontent.com/60868965/229945849-43b5718e-25b5-4d69-a45c-7cc996ba4892.png)

I was assigned to monitor the telemetry of the UAV from the GCS. From the GCS, I can see the UAV if it is near. See video below:

https://user-images.githubusercontent.com/60868965/229838860-de1342af-529a-43ea-a793-1e37cc51e9b4.mp4

The mission was successful. The UAV was able to fly about 2 hours (iirc).

The pilot takeover the control and lands the UAV safely. [HD & Full video: https://youtu.be/RucIUQfPn2Q]

https://user-images.githubusercontent.com/60868965/229861251-c4ab1f15-a943-4a67-a615-2885a0f1b339.mp4
