---
title: "Multimaterial Pliers"
excerpt: "A pair of pliers printed using both TPU 95 and PLA, utilizing the flexibility of TPU 95 and the rigid structure of PLA to complete a task."
header:
  teaser: /assets/img/uFluidic Device Images/Device on Table - Copy.jpeg
gallery:
  - image_path: assets/img/uFluidic Device Images/Device in Hand.jpeg
  - image_path: assets/img/uFluidic Device Images/Mold Top-Side.jpeg
  - image_path: assets/img/uFluidic Device Images/Mold Top.jpeg
   
---

![Device Photo](/assets/img/uFluidic Device Images/Device on Table - Copy.jpeg)

# Project Description

The project's goal was to create a working pair of multimaterial pliers using a flexible spring component. The pliers would be used to pick up resistors to test their functionality. Due to the limitations of the multimaterial printer, assembling parts made from different materials was allowed. However, if the multi-part approach was taken, the parts had to be hand-pressed together without the use of tools or external assistance.

Print-in-place is a form of multimaterial 3D printing that enables more complex designs using multiple materials to be printed on a single print bed simultaneously, rather than printing each part separately using one material at a time on different beds. This method eliminates the need to print separate parts and assemble them afterward. Print-in-place can be achieved through printer designs such as tool changers or multimaterial single extruders. Other, more expensive methods of achieving multimaterial printing include using independent print cartridges.

One application of print-in-place technology is in soft robotics. This field of robotics utilizes softer and more flexible materials to enable interaction with delicate objects. A common example is soft grippers, which can be printed using the multimaterial print-in-place method. These grippers typically have a softer, more flexible exterior for safe handling of fragile items and a more rigid interior for structural integrity.

https://www.sciencedirect.com/science/article/pii/S2214785322063921

Many material combinations work well with print-in-place printing; however, the best combination depends on the specific application. For the multimaterial pliers, an ideal combination would include both a rigid and a flexible material—providing a firm structure for the user to hold and grip the resistors while incorporating flexibility to allow the pliers to return to their original shape after being released. For this project, PLA and TPU 95 were used to achieve this functionality.


# Design and Iterative Process

Seeing previous designs found in the lab, I used them as a reference to model my own design. I designed the flexible component utilizing thin pieces of flexible TPU while ensuring it was large enough to retain its shape both during use and after being released. The part features a square-like shape with extrusions on each side to attach connectors. The middle of the part contains nine open squares, spaced evenly apart with a 1 mm wall between each square to act as a spring. The handles and grippers were designed simply and printed using PLA, focusing on completing the task efficiently. To assemble these parts, I designed a series of triangular connectors, allowing each part to be slotted together appropriately.

After printing and assembling the first iteration, the completed pliers were notably larger than preferred, as the goal was to pick up resistors. The grippers also did not fully close when the handles were squeezed and required pushing the handles to the side to close them further. Lastly, the first iteration's triangle connectors did not fit correctly into one another, making it difficult or even impossible to fully press the parts together using only hands.

In the second iteration, the overall size of the model and the length of the handles were reduced. The size reduction cut down on the amount of filament used to print the pliers and made it easier to pick up resistors. The reduced handle length allowed the grippers to close completely before the handles came together. The last change in this iteration was the addition of clearance to the triangular connectors to ensure the parts would fit together. The first two changes yielded positive results; however, the added clearance made the connections too loose, causing the parts to fall apart.

In the third iteration, I kept the same rigid parts and reprinted the flexible part with less clearance to see if the parts would hold together. With the decreased clearance, the parts did hold together, but I was unable to fully press them together, as the reduced clearance was now too tight, preventing the triangles from fully fitting.

For the last iteration, I implemented a design change on the triangle connectors. For both the rigid and flexible parts, I removed all clearance and added fillets to the corners. The rest of the model remained unchanged, and the fillets were added to reduce the amount of material on the triangles so they would fit properly. This method proved to be effective, as the parts were able to slide together securely and held without any issues.


# Specifications

* **Relevant specifications of the pliers (jaw length, jaw capacity)**
Jaw Capacity: 14.142 mm
Jaw Length: 70.125 mm
Handle Length: 83.938 mm

# Print Settings

The print settings used to print the PLA handles and jaw were the default settings provided on the SuperSlicer application for PLA on the Voron printer using a 0.6mm nozzle. None of the settings for these parts were changed. The PLA was printed at 215°C for the first layer and then 210°C for all subsequent layers.

The print settings were altered when printing the flexible part using TPU 95. While retaining most of the print settings, the horizontal shell layers were completely removed, and the infill pattern was changed from gyroid to grid. These changes provided more flexibility in the part, making it easier for it to compress more easily without losing out on the spring-like features, allowing it to return to its original state after compression. While experimenting with iterations, some other print settings, such as reducing the infill amount and testing different patterns, were tested but were not used during the last iteration.


# CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a47e3fbe2806571966?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

<br>

# Plier GIF
[![Video Play Image](https://img.youtube.com/vi/dTI9CPz5Ph0/0.jpg)](https://www.youtube.com/watch?v=dTI9CPz5Ph0){:target="_blank" rel="noopener"}

{% include gallery caption="Multimaterial Plier Gallery" %}
