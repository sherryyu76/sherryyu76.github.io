---
title: "Generative Design Skateboard Truck"
excerpt: "Lightweight electric skateboard truck modeled using Fusion 360 Generative Design and prototyped using pSLS technology "
header:
  image: /assets/img/truckSkateboard.jpg
  teaser: /assets/img/truckFront.jpg

gallery:
  - url: /assets/img/truckFront.jpg
    image_path: /assets/img/truckFront.jpg
    alt: "Powder Printed Generative Design Skateboard Truck"
  - url: /assets/img/truckSide.jpg
    image_path: /assets/img/truckSide.jpg
    alt: "Side Profile Skateboard Truck"
  - url: /assets/img/truckSkateboard.jpg
    image_path: /assets/img/truckSkateboard.jpg
    alt: "Skateboard Truck Assembled Onto Skateboard"
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


## Load Cases

Load cases are a critical aspect of the generative design process. It is essential that the applied loads accurately represent the forces the skateboard truck will experience under real-world conditions to ensure optimal performance. Both the magnitude and location of these forces must be defined to reflect realistic use scenarios. The load cases used in this study, including their magnitudes, application points, and descriptions, are summarized below.

| Name of Force                          | Magnitude        | Location of Application                         | Rationale                                                                 |
|----------------------------------------|------------------|--------------------------------------------------|---------------------------------------------------------------------------|
| Rider Weight (Bearing Load)            | 300 N (each side)| Ends of preserved axle (perpendicular)          | Simulates rider weight distributed through wheels onto the truck         |
| Turning Shear Force                    | 180 N            | Along Y-axis of preserved axle                  | Represents lateral force during turning                                  |
| Motor Torque                           | 8 N·mm           | Face of motor mounting plate                    | Simulates torque applied by motor during acceleration                    |
| Counter Torque (Braking)               | -8 N·mm          | Face of motor mounting plate                    | Represents braking torque opposing motor rotation                        |
| Bump/Curb Force (Motor Side)           | 1000 N           | Side with motor mount                           | Simulates impact force when hitting a bump on motor side                 |
| Bump/Curb Force (Opposite Side)        | 1500 N           | Side without motor mount                        | Higher impact force on unloaded side during uneven terrain               |
| Motor Weight                           | 9 N              | Motor mounting plate                            | Accounts for static load of motor on mount                               |
| Motor Mount Impact Force               | 500 N            | Motor mount (opposite direction of gravity)     | Simulates impact when motor mount hits a bump or obstacle                |

Large language models, such as ChatGPT, were used as a supporting tool to help estimate reasonable load magnitudes and identify appropriate locations for force application. To further improve the performance and reliability of the generated design, additional load cases could be incorporated to better capture a wider range of real-world conditions. Expanding the set of forces would allow the generative design algorithm to more effectively determine where increased structural integrity is necessary.


## Conclusion

In conclusion, generative design and pSLS offer a unique and powerful approach to modeling and prototyping components, particularly for applications that require both lightweight structures and strong mechanical performance. In this project, the generative design process successfully produced a skateboard truck that met the intended functional requirements, enabling the necessary motion while minimizing mass and maintaining structural integrity.

Although many advantages hold, there are notable limitations. Components generated through generative design often include complex organic geometries that are difficult to manufacture using traditional methods, which can limit their feasibility for commercial production. However, in specialized fields such as automotive and aerospace, where weight optimization is critical, generative design continues to provide a significant competitive advantage.


{% include gallery caption="Generative Design Skateboard Truck" %}
