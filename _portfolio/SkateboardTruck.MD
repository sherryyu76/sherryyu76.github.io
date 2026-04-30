---
title: "Syringe Pump"
excerpt: "Custom printed, & assembled low-cost syringe pump that addressed high cost of commercial units, while enabling precise fluid delivery (±0.0001 mL)"
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

The automated syringe pump was designed to deliver or withdraw liquid from a syringe with high precision and repeatability for laboratory and medical-style applications. Unlike manual syringe operation, which is inconsistent and difficult to control, this system converts the rotational motion of a stepper motor into linear motion through a lead-screw-driven actuator. This allows the device to control fluid flow rates in milliliters per minute, making it suitable for experiments requiring accurate, programmable dosing.

The pump supports both 10 mL and 20 mL syringes without mechanical reconfiguration. Flow rate is set in software and converted into motor speed using the geometry of the syringe and lead screw, allowing consistent volumetric delivery across syringe sizes.

<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH90d2dQT28d5b6028110fb0092e04850470?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

## Key Features of the Design

- **Stepper-Driven Lead Screw** – A stepper motor drives an 8 mm lead screw that converts rotational motion into precise linear movement of the syringe plunger.  
- **Universal Syringe Mount** – Custom 3D-printed pusher and holder blocks allow both 10 mL and 20 mL syringes to fit securely without mechanical reconfiguration.  
- **Programmable Flow Control** – The syringe diameter and desired flow rate are entered in software and used to calculate the motor speed for accurate volumetric delivery.  
- **Manual & Automatic Operation** – A latch button controls automatic pumping, while forward and reverse buttons allow manual positioning of the actuator.  
- **Limit Switch Safety** – A normally-closed limit switch stops all motion when the syringe reaches its mechanical limit to prevent damage.  
- **Status Indication** – An RGB LED displays pump states including running, paused, manual motion, and limit reached.  
- **Protective Enclosure** – The electronics are housed inside a box that protects users from electrical components and shields them from fluid spills.  

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

## Custom 3D Printed Parts

| Part | Link |
|------|------|
| Electronic Component Enclosure | [View Model](https://a360.co/4qRrEPI) |
| Syringe Carriage | [View Model](https://a360.co/49hPJcu) |
| Motor Mounting Plate | [View Model](https://a360.co/4sz29nX) |
| In Support | [View Model](https://a360.co/3NIO0UY) |
| In Support with Syringe Wing | [View Model](https://a360.co/49hPRbY) |

## Operating the Syringe Pump

**1.** Set the syringe diameter size and desired flow rate in the Arduino IDE program using the functions `syringeDiameter_mm` and `flowRate_mL_min`.  
**2.** Plug the computer into the Arduino using the USB cable and select the proper USB port in the program.  
**3.** Upload the program to the Arduino.  
**4.** Remove the USB cable from the Arduino and plug in the power cord.  
**5.** Prepare the syringe by pulling the plunger until full with the desired amount of liquid.  
**6.** Use the forward and reverse buttons (red) to set the correct length of the actuator so that the syringe will fit in the inserts. Ensure the pump is not moving. If it is, press the black latch button to stop it and reset the length between the syringe holders.  
**7.** Insert the syringe into the holder. The plunger should go in the rectangle closer to the motor, and the base of the syringe should go on top of the rectangle closer to the LED.  
**8.** Press the black latch button to start the pump. The LED should turn green.  
**9.** Once the pump is complete, the LED will turn red and the actuator will stop moving.

🔗 **[View the Syringe Pump Arduino code on GitHub](https://github.com/sherryyu76/Syringe_Pump_Code/blob/main/ArduinoCode)**


{% include gallery caption="Automatic Stepper Motor Driven Syringe Pump. " %}
