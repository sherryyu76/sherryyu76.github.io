---
title: "Multimaterial Pliers"
excerpt: "Multi-material, print-in-place pair of pliers that functions immediately after printing with no assembly required, featuring a precise grip capable of picking up small components such as through-hole resistors. "

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

## Print in Place Parts 
Print-in-place printing is a design approach commonly used in FFF that incorporates mechanisms such as hinges, joints, and linkages directly into a single printed part to create movement without post-assembly. These designs require careful consideration of precision, tolerances, and material integrity in order to function properly. Small dimensional inaccuracies can prevent moving components from operating as intended.

In many cases, multi-material printing is used to enhance functionality. For example, flexible materials such as TPU can be combined with rigid materials such as ABS or PLA to create compliant mechanisms or integrated spring features. The contrast between elastic and structural materials allows controlled motion within a single printed assembly.Print-in-place parts have a wide range of applications. They can be used in simple articulated figurines, such as this [articulated dragon](https://www.printables.com/model/413203-articulated-night-spirit-dragon) to functional everyday components, such as this [print-in-place ball bearings](https://www.printables.com/model/541192-print-in-place-bearings).

This project applies the print-in-place design approach to create a multi-material pair of pliers, integrating moving components directly into the print to eliminate the need for mechanical assembly.

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH90d2dQT28d5b6028119e2765fd49261ed5?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

## Key Features of the Design

This multi-material plier design consists of two essential components: a rigid body and a flexible spring element. The rigid component, which forms the handles and clamping jaws, is printed in PLA to provide the structural strength and stiffness necessary for gripping objects securely. The flexible component is printed in 95A TPU, allowing the pliers to compress and reliably spring back to their original position during clamping. The two regions are connected using dovetail joints, which mechanically lock the materials together. To ensure the components remained securely joined during repeated clamping while still being printable as a combined design, multiple iterations were conducted to determine the optimal tolerance for the dovetail interface.

### Rigid Region Print Settings

Because the rigid region is expected to withstand force during the squeezing motion, structural integrity is critical. This is reinforced by increasing perimeter shells and including sufficient top and bottom solid layers to strengthen both the horizontal and vertical directions. A moderate infill density is also used to balance strength and material efficiency.

| Setting                     | Value         |
|------------------------------|--------------|
| Material                     | PLA          |
| Vertical Perimeters (Shells) | 3            |
| Top Solid Layers             | 3            |
| Bottom Solid Layers          | 3            |
| Infill Pattern               | Rectilinear  |
| Infill Density               | 30%          |


### Flexible Region Print Settings

To allow the flexible region to deform easily while still maintaining the ability to spring back and retain the overall model shape, solid top and bottom layers are removed. This increases compliance and allows the internal structure to control the elastic behavior. A grid infill pattern is used with a 90° infill angle so that the internal strands align parallel to the perimeter walls, enabling the component to flex in the intended orientation defined by the CAD model.

| Setting                     | Value        |
|------------------------------|-------------|
| Material                     | 95A TPU     |
| Vertical Perimeters (Shells) | 3           |
| Top Solid Layers             | 0           |
| Bottom Solid Layers          | 0           |
| Infill Pattern               | Grid        |
| Infill Density               | 20%         |
| Infill Angle                 | 90°         |


{% include gallery caption="Automatic Stepper Motor Driven Syringe Pump. " %}

