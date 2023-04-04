[![Download as PDF Button](https://img.shields.io/badge/Download%20as%20PDF-EF3939?style=flat-square&logo=adobeacrobatreader&logoColor=white&color=black&labelColor=ec1c24)](https://mdtopdf.up.railway.app/convertPdf?url=https://github.com/iqfareez/MCTE-4362-Robotic-Hardware/blob/main/Week4/UAV.md)
![Assignment completion](https://img.shields.io/badge/Status-In%20Progress-yellow?style=flat-square)

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

## History of UAV

## Applications of UAV

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
    <td>DJI Mavic 3
    <img src="https://dji-official-fe.djicdn.com/dps/fa9086cc12f8187ba6462bb0df2dc881@origin.jpg" />
    </td>
  </tr>
  <tr>
    <td>Gasoline</td>
    <td>More power, longer flight times</td>
    <td>Louder, more emissions</td>
    <td>Insitu ScanEagle
      <img src="https://www.insitu.com/wp-content/uploads/2020/11/SE_Gallery_04.jpg"/></td>
  </tr>
  <tr>
    <td>Jet</td>
    <td>High speeds, high altitude capabilities</td>
    <td>Louder, more expensive to operate</td>
    <td>General Atomics MQ-9 Reaper
    <img src="https://i.guim.co.uk/img/media/94122807825fb1ee6eabb011645551731a32341a/224_101_6409_3848/master/6409.jpg?width=1200&height=900&quality=85&auto=format&fit=crop&s=65f66cc0768f61b17adfda2a53067270"/>
    </td>
  </tr>
  <tr>
    <td>Hybrid</td>
    <td>Flexible, efficient</td>
    <td>More complex, higher cost</td>
    <td>Boeing Phantom Eye
    <img src="https://www.aerocontact.com/public/img/aviaexpo/produits/images/471/detail_Phantom-Eye-1.jpg"/>
    </td>
  </tr>
  <tr>
    <td>Solar</td>
    <td>Unlimited flight times, environmentally friendly</td>
    <td>Slower, limited payload capacity</td>
    <td>QinetiQ Zephyr
    <img src="https://www.airforce-technology.com/wp-content/uploads/sites/6/2017/09/5-zephyr.jpg" />
    </td>
  </tr>
</table>

#### Notes

- **Hybrid** propulsion systems combine two or more types of propulsion, such as electric and gasoline or electric and solar, to provide greater flexibility and efficiency. Hybrid UAVs **can switch between different propulsion systems** depending on the mission requirements, allowing them to optimize performance and range.
- **Gasoline** propulsion systems use gasoline as their primary fuel source, whereas **jet** propulsion systems typically use kerosene-based fuels, such as Jet A or Jet A-1.

### Data Transmission

### Power Management
