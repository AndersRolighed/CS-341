Task RT2.1: Implement Lighting Models
This exercise was completed by following the lecture slides and writing the equations for the diffusion and specular components out into code.
These components were then used, while taking into account if no illumination was present, to formulate the expressions for the Phong and Blinn Phong models.
Also remembering to take account for the ambient light.


Task RT2.2: Implement shadows
This exercise is founded in the idea that a ray as observed by the camera, will be in the shadow of an object, if that ray is obstructed from its direct path to the light source by an object. For any ray, this was checked, if it happened to be obstructed, the light intensity was set to 0.


Task RT2.3.1: Derive iterative formula
The derivation worked by expanding the formular for the color of a given pixel c_b, and seeing that it will keep resulting in the reflections to come. By paying attention to this property, this iterative process can be summarized by the iterative formula as also described in the theory exercise pdf.

We believe that the simplification of the formula, when we are at most considering N reflections, is just a matter of setting the max number of iterations to N.



Task RT2.3.2: Implement reflections
Here we do as the exercise tells us, by creating an outer loop to loop over the amount of reflections we wish to iterate. The lighting is computed using the lighting function, where it is checked which object is obstructing the ray (if that is the case). The iterative formula is implemented and used to calculate the light intensity, and the new ray direction and origin is found. When doing this, there might be instances of a floating point being inside the object, which would case the ray from this new origin point, to get reflected back immediately. To account for this, the ray origin is moved a bit in the direction of the ray, so it now exists outside the object.


The total work done for this exercise was divided evenly amongst the group participants:
Anders Larsen (366794): 1/3
Clement Charmillot (307877): 1/3
Enrico Benedittini (367181): 1/3

Group 32.