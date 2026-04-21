---
title: "Top Down Modeling Bike Phone Mount"
excerpt: "Multi-material, print-in-place pair of pliers that functions immediately after printing with no assembly required, featuring a precise grip capable of picking up small components such as through-hole resistors. "

header:
  image: assets/img/Plier Iteration 2:3.jpg
  teaser: assets/img/plier-all.jpg

gallery:
  - url: assets/img/plier-all.jpg
    image_path: assets/img/plier-all.jpg
    alt: "All pliers"
  - url: assets/img/Plier Iteration 2:3.jpg
    image_path: assets/img/Plier Iteration 2:3.jpg
    alt: "Two of the best iterations"
  - url: assets/img/PlierGIF.gif
    image_path: assets/img/PlierGIF.gif
    alt: "Plier in motion"
---

## Top Down Modeling 

Top-down modeling is a CAD design approach in which components are created within the context of a single assembly, rather than being designed individually and later combined. One of the main advantages of top-down modeling is its effectiveness in complex assemblies with many interdependent parts. By designing components in relation to one another, it allows for easy parameterization, consistent alignment, and direct referencing between features, ensuring that parts fit and function together correctly.

In this project, a top-down modeling approach was used to design a bike phone mount that accommodates phones of varying sizes. When mounted, the holder allows the phone to rotate and securely snap into place between landscape and portrait orientations. The multiple components involved in the retractable and rotating mechanism benefit significantly from top-down modeling, as it enables direct access to critical dimensions and simplifies the creation of aligned features and joints, such as through the use of as-built joints.

## CAD Model

<iframe
  src="https://vanderbilt643.autodesk360.com/shares/public/SH90d2dQT28d5b6028119e2765fd49261ed5?mode=embed"
  width="640"
  height="480"
  frameborder="0"
  allowfullscreen>
</iframe>

## Key Features of the Design

The design of this phone mount consists of five major components: a back panel that securely supports the phone, retractable wings that grip the device against the back panel for added stability, a bike clamp that attaches the mount to a 22.2 mm diameter handlebar, and a detent mechanism that enables controlled rotation and locking between landscape and portrait orientations. Together, these components create a secure and adjustable mounting system that accommodates a range of phone sizes while maintaining stability during use.

### Detent Mechanism

A ball-spring detent mechanism is used to enable rotation between landscape and portrait orientations. The mechanism consists of a compression spring, an 8 mm ball bearing, a gear component, a guide/retaining component, and a housing lip. The spring and ball bearing are placed within a cavity in the guide/retaining component, which is positioned over the gear and secured with a lid to keep the detent assembly in place. As the assembly rotates, the spring applies force to the ball bearing, pressing it into the grooves of the gear. This interaction creates discrete positions and provides resistance, allowing the mount to hold its orientation securely.

Overall, the mechanism performed effectively; however, a key design consideration is the depth of the gear grooves. If the grooves are too deep, the detent force becomes too high, making rotation difficult. Conversely, if the grooves are too shallow, the holding force is insufficient, and the mount may not reliably maintain its orientation. This trade-off must be carefully balanced to achieve both smooth rotation and adequate positional stability.

<p align="center">
  <img src="/assets/img/Dovetail-Iterations.jpg" alt="Dovetail Iterations" width="700">
</p>

### Printing Method

<p align="center">
  <img src="/assets/img/plier-all.jpg" alt="Plier Iterations" width="700">
</p>

Traditional filament printing was used to manufacture the majority of the phone mount, as it offers rapid prototyping, minimal post-processing, and sufficient strength for this application. However, a trade-off of this method is reduced surface quality, particularly in features such as the gear grooves. The layer-based printing process introduces surface roughness, which can negatively affect the smooth rotation of the detent mechanism. To combat this, a shallower groove depth, approximately three-quarters of the ball bearing diameter, was selected to reduce resistance while still maintaining adequate detent engagement.

For the clamp component, pSLS was used. Since the clamp must withstand tensile stress from being secured onto the bike handlebar, it is critical to use a manufacturing method that can endure repeated deformation without failure. The nylon pSLS-printed part met these requirements by providing a combination of strength, flexibility, and high dimensional accuracy.

<p align="center">
  <img src="/assets/img/Plier-Iteration-2.PNG" alt="Second Iteration" width="700">
</p>

<p align="center">
  <img src="/assets/img/PlierGIF.gif" alt="Pliers Working Demonstration" width="700">
</p>


### Assembly

Heat-set inserts are first installed into the appropriate components, including the bottom portion of the bike clamp (M5), the back panel (M3), the bottom of the detent guide component (M3), and the gear panel (M3), using inserts of the correct diameter. Next, the retractable wings are assembled by partially threading screws into the rails using thread-forming screws, then inserting the male wing into the female track. An extension spring is attached between the two rails to enable retraction, and an M2 screw is installed along the side slot to prevent the wings from overextending. The gear panel is then secured to the back panel using four M3 × 15 mm screws.

Following this, the detent mechanism is assembled by placing the guide/retaining component over the gear, inserting the compression spring and 8 mm ball bearing into the cavity, and securing the assembly with a lid fastened by an M3 × 6 mm screw to retain the ball bearing inside the detent mechanism. The bottom portion of the detent assembly is then attached to the bike clamp using M3 × 10 mm screws. Finally, the fully assembled phone mount is secured onto the bike handlebar by fastening four M5 × 6 mm screws through the clamp using an Allen key, ensuring a tight and stable fit.

{% include gallery caption="Multimaterial Pliers" %}
