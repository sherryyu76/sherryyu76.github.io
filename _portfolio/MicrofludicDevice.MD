---
title: "Pinch Flow Fractionation Microfludic Device"
excerpt: "High resolution microfludic leveraging pinch and laminar flow to enable precise size-based separation of particles with sub-micron to micrometer-scale differences."
header:
  image: /assets/img/uDeviceSketch.jpg
  teaser: /assets/img/DeviceRotated.jpg

gallery:
  - url: /assets/img/DeviceRotated.jpg
    image_path: /assets/img/DeviceRotated.jpg
    alt: "Casted PDMS Microfludic Device"
  - url: /assets/img/uDeviceSketch.jpg
    image_path: /assets/img/uDeviceSketch.jpg
    alt: "CAD Sketch of Device"
  - url: /assets/img/TestSetUp.jpg
    image_path: /assets/img/TestSetUp.jpg
    alt: "Test Set Up"
  - url: /assets/img/TestSolution.jpg
    image_path: /assets/img/TestSolution.jpg
    alt: "Test Solution That Included Various Partical Sizes Beads For Sorting"
  - url: /assets/img/ResinMold.jpg
    image_path: /assets/img/ResinMold.jpg
    alt: "High Resolution Mold Printed Using Resin Printing"
---

## Pinch Flow Fractionation
Pinch flow fractionation is a commonly used microfluidic particle sorting technique that separates particles based on size using fluid flow at the microscale. At this scale, fluids behave drastically differently than at the macroscale, most notably due to laminar flow, in which two adjacent fluid streams do not mix.

Pinch flow fractionation heavily relies on this concept. Two streams are introduced through separate inlets: a sample stream containing unsorted particles and a buffer stream consisting of a clear solution. These streams are then directed into a pinch region, where the buffer flow compresses the sample into a very thin layer near the channel wall. Due to this pinching effect, smaller particles remain closer to the wall, while larger particles extend farther into the flow. Because the particles begin at different distances from the wall, when they enter a wider section of the channel, the streamlines expand and separate, allowing particles of different sizes to be directed into different outlets.

One biomedical application of PFF that requires the sorting of small particles is cell sorting, particularly the separation of red and white blood cells. This process is important for medical diagnostics, ranging from detecting common infections to identifying diseases such as leukemia. A major reason PFF is preferred over traditional sorting techniques, such as filtration, is that it utilizes laminar flow, which is gentler on cells and helps preserve cell viability while still achieving high-resolution separation. Further details on cell sorting using pinch flow fractionation and its advantages over traditional techniques are discussed in: [High-resolution microfluidic particle sorting using pinch flow fractionation](https://www.sciencedirect.com/science/article/pii/S0255270124004252).

## Design Considerations
When designing the final device, several considerations were taken into account to ensure optimal performance. Two key factors included the placement of the outlet boundaries for each of the three outputs and the proper balancing of flow through each channel to prevent particles from being directed into incorrect streams.

In determining the placement of the outlet boundaries, two particle size ranges were tested: 125–150 μm and 425–500 μm. Using a linear relationship, the particle position with respect to the bottom-right corner of the device is given by:
$$
Y_0 = \left(w_p - \frac{D}{2}\right)\frac{w_b}{w_p}
$$
where \( w_p \) is the pinch width, \( w_b \) is the broadened section width, and \( D \) is the particle diameter.

Based on these calculated ranges, buffer regions were introduced before each outlet. The minimum and maximum values of both particle ranges were used to define the overall stream span, and additional buffer spacing was incorporated to ensure that particles would reliably enter their intended outlets. Additionally, the diameter of the outlet holes was fixed due to the barbed fittings used in the experimental setup, which imposed a maximum allowable outlet channel width. For the larger particle range, the calculated positional span exceeded this maximum channel width, further necessitating the inclusion of buffer regions to accommodate the spread and maintain accurate particle sorting.

<p align="center">
  <img src="/assets/img/annotated.jpeg" alt="Annotated Device Profile" width="700">
</p>

With regard to balancing the flow rate of each of the three output channels, an three channel asymmetric approach was used. This ensures that the buffer flow is less likely to shift into one of the particle outlets. Since resistance is directly proportional to the length of the channel, increasing the channel length provides a straightforward method for controlling resistance. By designing the buffer channel to have the shortest length (lowest resistance) and the small particle channel to have the longest length (highest resistance), the buffer flow is directed through its intended outlet, preventing it from entering the particle outlets and disrupting particle trajectories.

However, the total channel length is ultimately constrained by the dimensions of the glass slide used to create the device. To maximize the effective channel length within this limited space, a serpentine channel design was implemented for the two particle outlets. This allows for increased channel length, while efficiently utilizing the available area. In addition to adjusting the outlet channel lengths to achieve the desired resistance for each channel, three individual syringe pumps were utilized at each outlet. This allowed for precise control of the flow rate in each outlet channel, preventing uneven flow that could disrupt the trajectories of the particles.

## Testing

The experimental setup consisted of two syringe pumps for the inlet streams and three syringe pumps at the outlets to collect the sorted solutions. The inlet flow rates were set to 3.0 mL/min for the buffer and 0.6 mL/min for the particle solution to maximize pinch flow. Polyethylene (PE) beads of varying sizes were used for testing. Since PE beads are hydrophobic, a 3% Tween solution was used to properly suspend the particles. A microscope was then used to capture and analyze the results.

<p align="center">
  <img src="/assets/img/TestSetUp.jpg" alt="Testing Set-Up" width="700">
</p>

<p align="center">
  <img src="/assets/img/TestSolution.jpg" alt="Test Partical Solution" width="700">
</p>


## Results
<iframe width="560" height="315" src="https://www.youtube.com/embed/NUa7pG6YIWE" 
title="Pinch Flow Fractionation Demo" frameborder="0" allowfullscreen></iframe>



{% include gallery caption="Pinch Flow Fractionation Microfludic Device" %}
