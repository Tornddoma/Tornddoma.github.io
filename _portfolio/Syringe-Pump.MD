---
title: "DIY Syringe Pump"
excerpt: "A syringe pump designed to output 1 to 10 mL/min of fluid at a constant speed."
header:
  teaser: /assets/img/Syringe Pump Render.png
gallery:
  - image_path: assets/img/Close Up Support.png
  - image_path: assets/img/Electrical Configuration.png
   
---

![Syringe Pump Render](/assets/img/IRL-Syringe-Pump Image.png)

# Purpose

The syringe pump was designed to deliver precise and accurate fluid amounts, making it suitable for applications such as testing or use in hospital settings for patients. It ensures sterile, continuous, and controlled fluid delivery, where precision is crucial. This DIY syringe pump was developed as part of the Rapid Prototyping course at Vanderbilt University, allowing us to practice and apply skills such as 3D modeling, part printing, and assembly. Additionally, this project required the use and programming of an Arduino for the pump to function.

# Features

* **Dispense Liquid at Set Rate** The syringe pump is designed to deliver fluids with precision and accuracy at rates ranging from 1 to 10 µL/min. This performance was verified during testing of the final model.
* **Moveable Carriage with Buttons** The pump features two buttons on the front panel, enabling the user to move the carriage forward or backward to load the desired syringe. This design eliminates the need for manually rotating the lead screw or disassembling any parts of the pump to load the syringe.
* **Works with Varying Syringe Sizes** The supports and carriage are designed to securely hold syringes of various sizes, up to 21 mm in diameter. This is achieved through the use of open slots and a band that firmly secures the syringe in place.
* **LED, Limit Switch, and Latching Button** The syringe pump features an RGB LED to indicate its current status to the user: green signals that the pump is running, yellow indicates it is paused, and red shows that the pump has run out of fluid and has stopped. Additionally, the pump includes a limit switch that halts the pump when pressed, typically when the syringe is empty. The latching switch allows the user to start or pause the pump as needed.

# Parts
## Off-The-Shelf-Parts

| Part | Quantity |
| ------- | ------- |
| V-Slot 20x40x350 | 1 |
| Nut-tr8x8-4 | 1 |
| NEMA-17-Motor | 1 |
| M5x8mm-Bolt| 12 |
| M5-Tee-Nut | 12 |
| M2.5 Thread forming screw | 2 |
| Limit Switch | 1 |
| M3x10mm-Bolt | 11 |
| M3x8-Thread-Forming-Screw | 4 |
| LM8UU-Linear-Bearing | 1 |
| Linear-Rod-8mmx200mm | 1 |
| Lead-Screw-TR8x8x250mm | 1 |
| Syringe | 1 |
| Syringe Plunger | 1 |
| Lock-Collar-Linear-Rod | 2 |
| Lock-Collar-Lead-Screw | 2 |
| Flanged-Ball-Bearing | 2 |
| meanwell_RD-65A | 1 |
| Breadboard | 1 |
| Arduino UNO | 1 |
| Coupler | 1 |
| 3M Hex Nut | 1 |

## Printed Parts

| Part | Quantity |
| ------- | ------- |
| End Support Holder w/ Switch Holes | 1 |
| End Support Holder w/o Switch Holes | 1 |
| Motor Mounting Plate | 1 |
| End Support | 1 |
| Syringe Band | 1 |
| Encolsure Box | 1 |
| Encolsure Cap | 1 |
| Enclosure Front Panel | 1 |
| Carriage | 1 |


# [Arduino Code](https://Tornddoma.github.io/_pages/Syringe-Pump-Arduino-Code)


# CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a4cb5f7ec64d6b820e?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>


# Operating Instructions

1. Plug in the power supply and fill syringe with fluid
2. Using the arrow buttons, move the carriage to the right spot for the syringe
3. Place and strap the syringe into the carriage using the TPU-printed strap
4. Input proper flow rate (in mL/min) and barrel diameter (in mm) into the arduino code (easily altered using the 2 variables at the of the code labeled “diameter” and “volFlowRate”)
5. Upload the code to the arduino
6. Press the "On/Off" latching button to start the syringe pump and press again to pause if needed
7. Green LED is ON/Going and Yellow LED is paused
8. When the syringe runs out of fluid, it will hit the limit switch causing the pump to stop and the LED to turn red.
9. The syringe pump can be reset by pausing it and moving the carriage back using the arrow buttons (Note: the arrow buttons only work when the pump is paused)


{% include gallery caption="Syringe Pump Gallery" %}
