---
title: "MicroFludic Device"
excerpt: "An asymmetric pinched flow fractionation (AsPFF) microfludic sorting device."
header:
  teaser: assets/img/uFluidic Device Images/Device on Table.jpeg
gallery:
  - image_path: assets/img/Close Up Support.png
  - image_path: assets/img/Electrical Configuration.png
   
---

![Syringe Pump Render](/assets/img/IRL-Syringe-Pump Image.png)

# Introduction to Microfluidic Devices

* **What are μFluidic Devices?** describe ufluidic devices (generally)
* **What is Pinch Flow Fractionation (PFF)?** what is it and how does it work
* **What is Asymmetric Pinched Flow Fraction (AsPFF)?**
* **Applications Requiring the Sorting of Small Particles** provide at least one specific application that requires sorting of small particles. Include
at least one citation from primary literature. 

# Instructions (Mold to Device)

* **Dispense Liquid at Set Rate** The syringe pump is designed to deliver fluids with precision and accuracy at rates ranging from 1 to 10 µL/min. This performance was verified during testing of the final model.
• How to go from the 3D printed mold to the final device (Lab on a Chip paper). Include
the following steps but with additional detail:
o CAD model
o Print and cure mold
o Parylene device
o Cast PDMS
o Plasma bond glass slide



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

# Sorting Video
[![Video Play Image](https://img.youtube.com/vi/dTI9CPz5Ph0/0.jpg)](https://www.youtube.com/watch?v=dTI9CPz5Ph0)

(^^ Click to Open in Browser ^^)


{% include gallery caption="Syringe Pump Gallery" %}
