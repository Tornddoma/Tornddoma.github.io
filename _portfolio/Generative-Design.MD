---
title: "Mass Reduction of Laptop Stand Part with Generative Design"
excerpt: "A part created using generative designed with the goal of reducing its mass while maintaining mechanical performance."
header:
  teaser: /assets/img/Generative Design Assets/Generative Design Render.PNG
gallery:
  - image_path: assets/img/Generative Design Assets/Generative_Design_Outcome_2025-Apr-24_10-11-06AM-000_CustomizedView1850467492.png
  - image_path: 
   
---

![Generative Design Part Render](/assets/img/Generative Design Assets/Generative Design Render.PNG)

# Generative Design

Generative design


# Part and Application

The part that was created using generative design for this project is a component of my laptop stand. Specifically, it is one of the two "legs" of the stand that support a larger platform at an angle, where the laptop rests. It is connected on one side by a pin, allowing it to rotate, while the other end fits into holes, enabling the stand's angle to be adjusted. I would have loved to recreate the entire stand; however, size constraints were too small and prevented me from doing so. (Images of the stand with the original part are provided in the gallery at the end of this page.)
The goal of creating this part was to reduce its mass while maintaining its mechanical performance. The original part was made of metal, but I believed the same performance could be achieved using plastic, considering the weight of the platform and laptop is not very heavy. This change would allow me to recreate the part with reduced size and mass while preserving its intended function. When I travel, I tend to carry my laptop and all the accessories I use with it, including this stand. The weights of the accessories added together can ger quite heavy, so I decided to recreate this part as a first step toward potentially remaking the entire stand to be both lighter and potentially more compact.

# Preserve and Obstacle Geometry

* **Preserve Geometry** There were 4 different preserve geometries within my model. All 4 of these geometries could be considered critial preserve regions in my model. 
![Preserve Geometries](/assets/img/Generative Design Assets/Preserve Geometries.png)

* **Obstacle Geometry** 
![Obstacle Geometries](/assets/img/Generative Design Assets/Obstacle Geometries.png)

▪ What were the critical preserve regions in your model (e.g., mounting
points, tool interfaces, constrained paths)?
▪ How did you define obstacle geometry (i.e., space the part must avoid)?


# Load Case Application and Structural Constraints

▪ Explain the types of forces you applied in the generative design study and
why each was necessary.
▪ How did you determine the magnitude, direction, and location of each
load?
▪ Where did you apply structural constraints, and how did this affect the
results?
▪ How can you test your real-world prototype to further refine the loads?

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

▪ In your experience, how useful is generative design for practical
engineering or prototyping?
▪ What limitations did you encounter?
▪ In what types of applications or industries would generative design be
most useful? Where might it fall short?


# CAD Model
<iframe src="https://vanderbilt643.autodesk360.com/shares/public/SH286ddQT78850c0d8a438c1f7d61e1e6186?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

<br>

{% include gallery caption="Generative Design Part Gallery" %}

