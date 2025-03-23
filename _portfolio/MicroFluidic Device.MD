---
title: "Microfludic Device"
excerpt: "An asymmetric pinched flow fractionation (AsPFF) microfluidic sorting device."
header:
  teaser: /assets/img/uFluidic Device Images/Device on Table - Copy.jpeg
gallery:
  - image_path: assets/img/uFluidic Device Images/Device in Hand.jpeg
  - image_path: assets/img/uFluidic Device Images/Mold Top-Side.jpeg
  - image_path: assets/img/uFluidic Device Images/Mold Top.jpeg
   
---

![Device Photo](/assets/img/uFluidic Device Images/Device on Table - Copy.jpeg)

# Introduction to Microfluidic Devices

* **What are Microfluidic Devices?** As the name implies, microfluidic devices are small devices that utilize fluid flow to perform a task. They can conduct tests by collecting samples, manipulating them, and analyzing the results. Some forms of manipulation include particle or liquid separation, mixing, and droplet generation. Microfluidic devices rely on capillary action to move liquids through their channels, allowing the liquid to flow without external forces. The device created for this project focused solely on sorting particles of varying sizes.

* **What is Pinch Flow Fractionation (PFF)?** Pinch flow fractionation is a method of sorting particles in microfluidics through the use of a particle stream and a buffer stream. These two streams are sent through a narrow, pinched area where the buffer stream from one inlet pushes the particles from the other inlet against the wall. After exiting the pinched area, the combined (but unmixed) stream enters a broader area, where laminar flow causes the particles to move along a set path. The path of a particle depends on the width of the pinched and broad sections, as well as the diameter of the particle. Larger particles, whose centers are positioned farther from the wall when pushed against it, will flow further away from the wall of the broad section—but not beyond half of its width. Since the particles are spaced out, outlets can be placed to collect the sorted particles.

* **What is Asymmetric Pinched Flow Fraction (AsPFF)?** Asymmetric pinched flow fractionation (AsPFF) is a particle-sorting method similar to the PFF method. The key difference between the two is that AsPFF utilizes varying flow rates, whereas in PFF, the outlet flow rates must be equal. AsPFF achieves this by using asymmetric branch channels, where a single outlet is larger and usually shorter compared to the particle-collecting outlets. The larger outlet, called the drain channel, directs most of the liquid flow, creating an effect that amplifies the difference in particle positions against the sidewall during the pinch. This allows for the sorting of much smaller particles or cases where the  particles have minimal size differences.
  * Source: [Lab on a Chip: Continuous particle separation in a microchannel having asymmetrically arranged multiple branches](https://pubs.rsc.org/en/content/articlelanding/2005/lc/b501885d){:target="_blank" rel="noopener"}

* **Application Requiring the Sorting of Small Particles** One application that requires the sorting of small particles and can be achieved through microfluidic devices is cell and particle sorting. This type of sorting is essential in fields such as biology, biomedicine, and chemistry, where cell and particle isolation, separation, and focusing are key aspects of research and testing.
  * Source: [Microfluidic platforms for the manipulation of cells and particles](https://www.sciencedirect.com/science/article/pii/S266683192200011X){:target="_blank" rel="noopener"}

# Fabrication Instructions

1. **CAD Model** The CAD model consists only of the mold required to cast the microfluidic device. The device specifications required the ability to sort particles up to 500 microns in diameter, with inlet and outlet channels positioned at least 11 mm apart (center to center). This separation accounts for the size of the barbs, which require extra space for proper insertion into the device. Since the device was designed as an AsPFF system, where outlet flow rates are highly significant, the outlets were modeled through the side of the device to prevent any flow rate restrictions. The model includes two inlet channels, a pinched section, a small expansion area, a drain channel, and two sorting channels.
2. **Print and cure mold** Once the model of the mold was completed, it was printed using a Formlabs Form 4 SLA printer with clear V5 resin and a 0.05 mm layer height. The selection of resin did not affect the outcome of the device and was chosen because it was readily available. Once the print was complete, it was washed for 5 minutes in a Formlabs Formwash with isopropyl alcohol (IPA) while still attached to the printing bed, followed by another 5 minutes off the bed. After washing, the device was dried for 30 minutes to remove all the IPA before being cured with UV light for 60 seconds at room temperature. After curing, the printing supports were removed, and the mold was complete.
3. **Parylene device** The cured mold was coated with parylene using a parylene deposition device. Parylene can be applied as a nanometer-thick coating, making it ideal for casting small devices such as those used in microfluidics. The parylene coating renders the SLA-printed mold cytocompatible and allows it to be compatible with PDMS casting.
4. **Cast PDMS** Once the print was coated with a parylene film, it was cast with PDMS and other agents to speed up the curing process. The PDMS device was then cured within the mold at high temperatures for a few hours before being removed.
5. **Plasma bond glass slide** Once the PDMS device was demolded, it was plasma-bonded to a glass coverslip, creating a complete working device.

# Discussion

Why are resin-printed molds coated with parylene prior to casting the PDMS? What are hypothetical applications of your microfluidic mixer or sorter?
* a

Why is your geometry conducive to sorting? Discuss specific dimensions (pinch width, outlet width, location of ports, etc.)
* a

What steps or design features did you use to ensure that each outlet received the same flow rate, preventing disruptions to the streamlines and maintaining proper separation?
* a

Based on the results of testing, could you implement any future changes to improve sorting?
* Testing showed that the device sorts most of the particles; however, some of the smaller particles get caught in the wrong stream and are not sorted properly. One possible solution would be to rerun the partially sorted stream through the device to achieve complete sorting. The problems I believe are occurring include some smaller particles not reaching the top wall in time before leaving the pinched section, as well as the geometry of the area after the pinched section potentially obstructing some of the flow. Based on these results, there are a few future changes that may improve sorting.
  * Method 1: Reduce Inlet Channel Width of Particle Stream
    * By reducing the inlet channel width, the particles would enter the pinched section closer to the wall, ensuring that they reach it before leaving the section.
  * Method 2: Increase Pinched Section Length
    * The same principle applies to this solution: by increasing the length of the pinched section, the particles are given more time to travel toward the wall before leaving the section.
 * Method 3: Modify Geometry of Area After Pinched Section
  * Since I believe the flow is being obstructed by the geometry of the area, a geometrical change that could be viable to prevent flow obstruction would be a semi-circle.

Did you attempt the bonus opportunity? If so, describe your approach and success.
* I did not attempt the bonus opportunity to create a mechanism or device to enable equal flow rates. I did not attempt it as it was imcompatible with the AsPFF microfluidic device that I created.


# Mold CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a4a6dad7d02316b283?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

<br>

# Sorting Video
[![Video Play Image](https://img.youtube.com/vi/dTI9CPz5Ph0/0.jpg)](https://www.youtube.com/watch?v=dTI9CPz5Ph0){:target="_blank" rel="noopener"}

{% include gallery caption="μFludic Device Gallery" %}
