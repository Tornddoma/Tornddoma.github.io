---
title: "Generative Design: Laptop Stand Part"
excerpt: "A part created using generative designed with the goal of reducing its mass while maintaining mechanical performance."
header:
  teaser: /assets/img/Generative Design Assets/Generative Design Render.PNG
gallery:
  - image_path: assets/img/Generative Design Assets/Stand.jpg
  - image_path: assets/img/Generative Design Assets/Original Stand.jpg
  - image_path: assets/img/Generative Design Assets/Generative Design Part Stand.jpg
  - image_path: assets/img/Generative Design Assets/Generative_Design_Outcome_2025-Apr-24_10-11-06AM-000_CustomizedView1850467492.png
  - image_path: assets/img/Generative Design Assets/Part.jpg
  - image_path: assets/img/Generative Design Assets/Explore Page Gen Design.png

---

![Generative Design Part Render](/assets/img/Generative Design Assets/Generative Design Render.PNG)


# Part and Application 

The part that was created using generative design for this project is a component of my laptop stand. Specifically, it is one of the two "legs" of the stand that support a larger platform at an angle, where the laptop rests. It is connected on one side by a pin, allowing it to rotate, while the other end fits into holes, enabling the stand's angle to be adjusted. I would have loved to recreate the entire stand; however, size constraints were too small and prevented me from doing so. (Images of the stand with the original part are provided in the gallery at the end of this page.)

The goal of creating this part was to reduce its mass while maintaining its mechanical performance. The original part was made of metal, but I believed the same performance could be achieved using plastic, considering the weight of the platform and laptop is not very heavy. This change would allow me to recreate the part with reduced size and mass while preserving its intended function. When I travel, I tend to carry my laptop and all the accessories I use with it, including this stand. The weights of the accessories added together can ger quite heavy, so I decided to recreate this part as a first step toward potentially remaking the entire stand to be both lighter and potentially more compact.


# Preserve and Obstacle Geometry

* **Preserve Geometry** There were four different preserve geometries within my model. All four of these geometries could be considered critical preserve regions. One of the preserve geometries was the pin hole. This was preserved to ensure that there would be a pin hole in the location that required it (top right of image). The next two preserve geometries were rectangular prisms, which acted as a marker as well as a barrier for the generative design. These were placed so that the study would generate material to connect the four parts together the way I wanted, as well as act as a stopping point of rotation for the laptop stand if the leg was moved too far. The last preserve geometry was a simple cylinder, since I needed some type of geometry there that was smaller than the other areas of the part to fit within the holes used to lock the stand in place (bottom left of image).
![Preserve Geometries](/assets/img/Generative Design Assets/Preserve Geometries.png)

* **Obstacle Geometry** A total of seven obstacle geometries were made. These regions are the areas where material is not generated during the creation of the part. Four of the obstacle geometries, shown below as the top two and bottom two rectangular prisms, were placed to ensure that no material would be generated in the areas where the stand could be, preventing any problems with the rest of the stand. A smaller prism was placed in front of the small bottom extrusion to ensure that there would be no material sticking out at the bottom, since it needed to be flat to ensure the original angles were being created when the leg was in the holes. There is also a cylindrical obstacle geometry inside the pin hole to prevent any material from blocking the hole. Originally, this obstacle geometry was not added, and the generative study filled the pin hole. Lastly, an obstacle geometry was placed under the part to prevent material from being generated there, as the extra material generated in that area did not look good (using the preview feature) and would prevent the stand from being folded for storage.
![Obstacle Geometries](/assets/img/Generative Design Assets/Obstacle Geometries.png)


# Load Case Application and Structural Constraints

There were three types of forces that were applied to the generative study. These types of forces were bearing loads, forces, and moments. A bearing load was required in this generative study as the part was connected to the main stand using a cylindrical pin. This would cause a bearing load on the walls of the part surrounding the pin. Next, with the other end of the part touching both the ground and the side of one of the holes, they generate a reaction from the wall of the hole and the floor to the part. These reactive forces counter the forces from the bearing load and ensure that the part is in equilibrium (not moving). Lastly, a moment is generated by the restriction of rotation of the part about the pin. This moment is located where the pin connection is, and the restriction of motion is from the other end of the part being held in place by the holes of the stand.

The magnitude of the bearing load was determined by converting the weight of the laptop plus the weight of the stand platform from lbs to newtons, then dividing it by two. The reason it was divided by two is that the weight is split evenly between two legs on the stand. The angle/direction of the bearing load would depend on the angle at which the stand is placed. For the generative design study, two load cases were used, each having different angles (45 degrees and 30 degrees from the horizontal). The bearing load was placed at the pinhole, as that was where all the forces would be acting on the part from the laptop and platform above it. Next, the two reactive forces were determined based on the reactions generated by the ground and the side of the hole. These forces would equal the force components of the bearing load to ensure that the part was in equilibrium because, at this point, the stand would be stationary. Their direction would be normal to their point of contact, and their location would be at the point of contact as well. Lastly, the magnitude of the moment was calculated using M = Fd where M is moment, F is force, and d is distance. Here, d would be the perpendicular distance of the forces from the point of rotation, that being the pinhole. The direction of the moment would be opposite of the direction that the part is naturally spinning, therefore it would be counter-clockwise.

A structural constraint was added to the bottom end of the part. A fixed constraint was added to it because it would not be moving once the stand was set up. The result of the fixed constraint was that there was more material generated near that area compared to the other end of the part. This could be due to the high stresses and forces that fixed parts usually experience.

The real-world prototype could be tested by placing it into the laptop stand and determining what differences occur when using the original part and the prototype. This could also help determine any missed loads or load distributions to the part/stand overall to further refine the loads. Some other testing where the part is exposed to higher loads could determine how strong the part really is and could be further improved by considering other devices as well.


## Table of Forces Applied
### Load Case 1 (45 Degree Angle)

| Force | Magnitude | Location | Rational |
| ------- | ------- | ------- | ------- |
| Bearing | 7.8 N | Pin Hole   | Total force divided by 2 because 2 legs. |
| Force | 5.515 N | Bottom Small Extrusion | Horizon reactive force from the part pushing against hole to stay in place. |
| Force | 5.4 N | Bottom Wider Extrusion  | Veritcal reactive force from the hole pushing upward on the part |
| Moment| 1.35 Nm | Pin Hole | Moment created from forces restricting rotation |

### Load Case 2 (30 Degree Angle)

| Force | Magnitude | Location | Rational |
| ------- | ------- | ------- | ------- |
| Bearing | 7.8 N | Pin Hole   | Total force divided by 2 because 2 legs. |
| Force | 6.755 N | Bottom Small Extrusion | Horizon reactive force from the part pushing against hole to stay in place. |
| Force | 3.90 N | Bottom Wider Extrusion  | Veritcal reactive force from the hole pushing upward on the part |
| Moment| 1.35 Nm | Pin Hole | Moment created from forces restricting rotation |


# Critique of Generative Design

In my experience, generative design is very useful for prototyping. It enables AI to create multiple iterations of potential prototypes. By specifying where to build, where not to build, and what forces will act on the model, AI can solve these challenges independently, saving both time and potentially money. Since the designs are generated by AI and tend to be rough in appearance, I believe generative design is especially well-suited for the prototyping phase. These prototypes can then be further refined into more practical and finalized designs.

I did not encounter any limitations while using generative design, as my project was relatively straightforward. However, one limitation I believe exists is in the post-processing capabilities of generative design. Fusion provides many tools for refining the generated model, but I feel they are still somewhat lacking. Despite spending time adjusting my part, I was never able to get it to look exactly the way I wanted.

I believe generative design would be most useful in industries such as automotive, medical, robotics, and construction. These fields often require the design of components, ranging from small structural elements to larger assemblies, making generative design a valuable tool for initial prototyping and model generation. From there, the generated models can be refined or redesigned to suit specific needs.

On the other hand, I think generative design may fall short in applications that don’t involve structural or mechanical requirements. Simpler items can often be designed and built more quickly and easily using traditional methods like manual modeling. Additionally, generative design may not be ideal in cases where aesthetics or development speed are more important than performance, such as with toys or artistic creations.


# CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a438c1f7d61e1e6186?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

<br>

{% include gallery caption="Generative Design Part Gallery, Note: Explore page has one result because only unrestricted was used." %}

