---
title: "Generative Design Skateboard Truck"
excerpt: "Lightweight electric skateboard truck modeled using Fusion 360 Generative Design and prototyped using pSLS technology "
header:
  image: /assets/img/SyringePumpRender.png
  teaser: /assets/img/SyringePump.png

gallery:
  - url: /assets/img/SyringePump1.JPG
    image_path: /assets/img/SyringePump1.JPG
    alt: "Interior Wiring of Syringe Pump"
  - url: /assets/img/SyringePump2.JPG
    image_path: /assets/img/SyringePump2.JPG
    alt: "Side Profile Syringe Pump"
  - url: /assets/img/SyringePump3.JPG
    image_path: /assets/img/SyringePump3.JPG
    alt: "Breadboard wiring along with the stepper motor driver"
---

## Powder Bed Selective Laser Sintering and Generative Design

Powder Bed Selective Laser Sintering (pSLS) is an additive manufacturing process that uses a laser to selectively melt and sinter plastic powder in a layer-by-layer manner to form a solid component. One key advantage of pSLS is that it does not require support structures, as the surrounding unsintered powder naturally provides support during the build process. Generative design is a modeling approach in which, rather than manually designing a component, the user defines performance goals, constraints, preserved regions, and loading conditions. The software then uses algorithms to automatically generate optimized design solutions. These resulting designs often feature organic, complex geometries that minimize weight while maintaining structural integrity.

These two technologies pair well together, as pSLS is capable of manufacturing the intricate, support-free geometries produced by generative design without concern for orientation or additional support material. This combination is especially valuable in industries such as automotive and aerospace, where reducing weight while maintaining strength is critical for improving efficiency and performance. 

A prime example is the Airbus Bionic Partition. This cabin partition was originally composed of multiple components, including brackets, fasteners, and structural elements. Through generative design, it was redesigned as a more integrated, lightweight structure, reducing assembly complexity and contributing to improved fuel efficiency.  More about the Airbus Bionic Partition can be found [here](https://www.airbus.com/en/newsroom/news/2016-03-pioneering-bionic-3d-printing).

## Generative Design Skateboard Truck

In this project, a skateboard truck for an electric skateboard will be designed using a generative design approach, integrating the truck and motor mount into a single component. The study will consider two materials, AlSi10Mg and 17-4 PH stainless steel, which are commonly used in metal powder bed fusion processes. The primary objective is to minimize mass while maintaining structural integrity, with a target safety factor of 2. Additionally, an “unrestricted” manufacturing method will be specified to allow the generative design algorithm maximum freedom in exploring a wide range of geometries.

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH90d2dQT28d5b602811de77901161bca7c6?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

## Materials

The two generative design studies conducted for the selected materials produced similar overall geometries for the final skateboard truck. The primary difference lies in the structural features: the AlSi10Mg (aluminum) design exhibits thicker and bulkier features and supports compared to the 17-4 PH stainless steel design. This is expected, as aluminum has a lower tensile strength than stainless steel, requiring additional material to maintain the same safety factor. As loads and forces increase, the aluminum design would continue to become significantly bulkier relative to the steel design in order to satisfy structural constraints. The final CAD models for both AlSi10Mg and 17-4 PH stainless steel respectively are shown below.

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH90d2dQT28d5b6028112a55368953c22d59?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH90d2dQT28d5b602811d93e9d50390c8130?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>
 
## Obstacle and Preserved Geometries

Defining appropriate obstacle and preserved geometries is critical to the success of a generative design study. The design must ensure sufficient clearance around the pivot point to allow proper truck rotation, adequate space for the motor system, and sufficient clearance must be provided for mounting bolts and the Allen key required for installation.

<p align="center">
  <img src=" /assets/img/PivotClearance.gif" alt="Pivot Cup Turning Motion" width="700">
</p>

<p align="center">
  <img src=" /assets/img/RotatingMotor.gif" alt="Motor Rotation" width="700">
</p>

To satisfy these clearance requirements, regions within the assembly must be designated as preserved geometries. These include the ends of the axle (which define the wheel bearing seat diameter and spacing), the pivot cup interface, the central cutout region, and the motor mounting plate. All surrounding components in the CAD assembly should be defined as obstacle geometries to prevent interference during the design generation process. Additionally, installation clearance regions must be specified as obstacles for components such as the TPU bushing, motor mounting screws, wheel nuts, and areas surrounding the axle.

By properly defining these preserved and obstacle geometries, the generative design algorithm can produce a structure that maintains the necessary clearances for all components while preserving the required degrees of freedom for motion.


## Key Features of the Design

## Off Shelf Parts

| Part | Quantity |
|------|----------|
| Heat Set Inserts (M3) | 11 |
| Alloy Steel Socket Head Screws (M3) | 8 |
| Latching Push Button | 1 |
| Non-latching Push Button | 2 |
| RGB LED (Common Anode/Cathode) | 1 |
| 400-point Solderless Breadboard | 1 |
| Jumper Wire Kit | 1 pack |
| Assorted Resistor Kit | 1 pack |
| Stepper Motor Driver  | 1 |
| Stainless Steel Thread-locking Socket Head Screws | 8 |
| Mean Well RD-65A Dual Output Power Supply | 1 |
| Zinc-Plated Steel Hex Nut | 1 |
| Arduino Uno | 1 |
| V-Slot 20×40 Aluminum Extrusion (350 mm) | 1 |
| NEMA-17 Stepper Motor | 1 |
| M3 × 10 mm Bolts | 4 |
| M5 T-Slot (Tree) Nuts | 8 |
| M5 × 8 mm Bolts | 8 |
| F688ZZ Flanged Ball Bearing (8 mm ID) | 1 |
| M3 × 8 mm Thread-forming Screws | 4 |
| TR8×8 Brass Lead-Screw Nut | 1 |
| LM8UU Linear Bearing | 1 |
| 20 mL Syringe | 1 |
| TR8×8 Lead Screw (250 mm) | 1 |
| 8 mm Linear Rod (200 mm) | 1 |
| ¼” to 8 mm Flexible Shaft Coupler | 1 |

{% include gallery caption="Generative Design Skateboard Truck" %}
