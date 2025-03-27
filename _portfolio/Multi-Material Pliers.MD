---
title: "MultiMaterial Pliers"
excerpt: "A pair of pliers printed using both TPU 95 and PLA."
header:
  teaser: /assets/img/uFluidic Device Images/Device on Table - Copy.jpeg
gallery:
  - image_path: assets/img/uFluidic Device Images/Device in Hand.jpeg
  - image_path: assets/img/uFluidic Device Images/Mold Top-Side.jpeg
  - image_path: assets/img/uFluidic Device Images/Mold Top.jpeg
   
---

![Device Photo](/assets/img/uFluidic Device Images/Device on Table - Copy.jpeg)

# Project Description

Description of the project with a blurb about print-in-place parts. Perform external
research to determine other applications print-in-place has been used. What
combination of materials work well for print-in-place?

# Fabrication Instructions

1. **CAD Model** The CAD model consists only of the mold required to cast the microfluidic device. The device specifications required the ability to sort particles up to 500 microns in diameter, with inlet and outlet channels positioned at least 11 mm apart (center to center). This separation accounts for the size of the barbs, which require extra space for proper insertion into the device. Since the device was designed as an AsPFF system, where outlet flow rates are highly significant, the outlets were modeled through the side of the device to prevent any flow rate restrictions. The model includes two inlet channels, a pinched section, a small expansion area, a drain channel, and two sorting channels.
2. **Print and cure mold** Once the model of the mold was completed, it was printed using a Formlabs Form 4 SLA printer with clear V5 resin and a 0.05 mm layer height. The selection of resin did not affect the outcome of the device and was chosen because it was readily available. Once the print was complete, it was washed for 5 minutes in a Formlabs Formwash with isopropyl alcohol (IPA) while still attached to the printing bed, followed by another 5 minutes off the bed. After washing, the device was dried for 30 minutes to remove all the IPA before being cured with UV light for 60 seconds at room temperature. After curing, the printing supports were removed, and the mold was complete.
3. **Parylene device** The cured mold was coated with parylene using a parylene deposition device. Parylene can be applied as a nanometer-thick coating, making it ideal for casting small devices such as those used in microfluidics. The parylene coating renders the SLA-printed mold cytocompatible and allows it to be compatible with PDMS casting. Cytocompatible means that a material is biocompatible or cell-safe, which is one of the essential requirements for microfluidic devices.
4. **Cast PDMS** Once the print was coated with a parylene film, it was cast with PDMS and other agents to speed up the curing process. The PDMS device was then cured within the mold at high temperatures for a few hours before being removed.
5. **Plasma bond glass slide** Once the PDMS device was demolded, it was plasma-bonded to a glass coverslip, creating a complete working device.


# Discussion

* **Why are resin-printed molds coated with parylene prior to casting the PDMS? What are hypothetical applications of your microfluidic mixer or sorter?**
  * Resin-printed molds are coated with parylene prior to casting the PDMS because it is cytocompatible, creates a smooth, non-stick surface, and improves adhesion. The cytocompatibility makes it cell-safe. The smooth, non-stick surface makes it easy to remove the PDMS mold after casting and curing, and the smoothness prevents the PDMS from acquiring any surface texture that could affect the device. Lastly, the improved adhesion of the PDMS to the parylene film ensures that the cast device is fully in contact with the film without any air bubbles. Hypothetically, my microfluidic sorter could be used to sort or remove certain particles from a liquid stream. If scaled down, a potential application could be to sort and remove parasites or other unwanted entities from the bloodstream.

* **Why is your geometry conducive to sorting? Discuss specific dimensions (pinch width, outlet width, location of ports, etc.)** 
  * The device I created is very small, as there was no need for a large broad section within my design for AsPFF. Due to the flow rate restrictions of the outlet barbs, the design was created to enable the outlet streams to flow freely out of the device. This ensures the proper outlet flow rate ratio required for AsPFF, as calculated for the design. The pinch width was set to 0.85 mm to accommodate the large inlet widths of 2 mm each and particles up to 0.5 mm (500 microns). The inlet widths were not specifically determined for any particular reason but were made equal to ensure the inlet flow rate ratios were set correctly with the syringe pumps used to pump liquid in. Since the device was small, the design was positioned further toward one end of the mold to reduce the amount of liquid required during the sorting process. Lastly, the slightly larger open area after the pinched section was designed to enable the laminar flow of the streams into each channel, and the outlet flow rate ratio was achieved with a larger drain channel (1.5 mm width) and two smaller sorting channels (0.6 mm width).

* **What steps or design features did you use to ensure that each outlet received the same flow rate, preventing disruptions to the streamlines and maintaining proper separation?**
  * Since my device utilized the AsPFF method of sorting, I purposely designed asymmetric channels to restrict the flow rate within the sorting channels and create a much larger flow rate in the drain channel. The calculated flow rate ratio from a sorting channel to the drain channel is 1:4. To prevent disruptions to the streamlines, the channels were designed to avoid tight or sharp corners, maintaining laminar flow. For AsPFF, proper separation depends on both the inlet and outlet flow rate ratios. The hypothetical flow rate ratio for the inlets was determined to be 1:4.1; however, during testing, a ratio of 1:4.22 was required to maximize the sorting capabilities of the device.

* **Based on the results of testing, could you implement any future changes to improve sorting?**
  * Testing showed that the device sorts most of the particles; however, some of the smaller particles get caught in the wrong stream and are not sorted properly. One possible solution would be to rerun the partially sorted stream through the device to achieve complete sorting. The problems I believe are occurring include some smaller particles not reaching the top wall in time before leaving the pinched section, as well as the geometry of the area after the pinched section potentially obstructing some of the flow. Based on these results, there are a few future changes that may improve sorting.
    * Method 1: Reduce Inlet Channel Width of Particle Stream
      * By reducing the inlet channel width, the particles would enter the pinched section closer to the wall, ensuring that they reach it before leaving the section.
    * Method 2: Increase Pinched Section Length
      * The same principle applies to this solution: by increasing the length of the pinched section, the particles are given more time to travel toward the wall before leaving the section.
    * Method 3: Modify Geometry of Area After Pinched Section
      * Since I believe the flow is being obstructed by the geometry of the area, a geometrical change that could be viable to prevent flow obstruction would be a semi-circle.

* **Did you attempt the bonus opportunity? If so, describe your approach and success.** 
  * I did not attempt the bonus opportunity to create a mechanism or device to enable equal flow rates. I did not attempt it as it was imcompatible with the AsPFF microfluidic device that I created.


# Mold CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a47e3fbe2806571966?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

<br>

# Sorting Video
[![Video Play Image](https://img.youtube.com/vi/dTI9CPz5Ph0/0.jpg)](https://www.youtube.com/watch?v=dTI9CPz5Ph0){:target="_blank" rel="noopener"}

{% include gallery caption="μFludic Device Gallery" %}
