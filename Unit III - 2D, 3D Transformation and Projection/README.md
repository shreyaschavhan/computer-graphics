# Unit III : 2D, 3D Tranformation and Projection.

## 2D Tranformation:

* 2D Tranformation:
> * Repositioning and Resizing of an object is called as tranformation
> * Types of Tranformation:
> 	* Translation
> 	* Rotation
> 	* Scaling
> * Homogenious Co-odinates
> * Other Tranformation:
> 	* shearing
> 	* Reflection


---

* Translation:
> * Translation is repositioning of an object in a straight line.
> * Derivation:
>	* ![image](https://user-images.githubusercontent.com/68887544/115364013-96390e80-a1e0-11eb-90e5-9b5ee3e5c0d8.png)
> * Example Numberical:
> 	*  ![image](https://user-images.githubusercontent.com/68887544/115364625-342cd900-a1e1-11eb-868c-122712a80682.png)

---

* Rotation:
> * Repositioning of an object in a circular path is called as Rotation.
> * Derivation:
> 	*  ![image](https://user-images.githubusercontent.com/68887544/115368302-93d8b380-a1e4-11eb-9e3c-7d4712651f27.png)
> 	* Matrix Representation:
> 	* ![image](https://user-images.githubusercontent.com/68887544/115368805-13668280-a1e5-11eb-8a6c-380a146466e1.png)
> * If Anticlockwise, Rotation angle +ve
> * If Clockwise, Rotation angle -ve

---

* Scaling:
> * Zoom-In or Zoom-out of object is called as scaling
> * Scaling Factor:
> 	* scaling in x-direction : S<sub>x</sub>
> 	* scaling in y-direction : S<sub>y</sub>
> * Equation:
> 	* ![image](https://user-images.githubusercontent.com/68887544/115370628-def3c600-a1e6-11eb-829c-f4835123a132.png)
> * Conditions:
> 	* ![image](https://user-images.githubusercontent.com/68887544/115371255-6fcaa180-a1e7-11eb-8881-ae8a6616efa2.png)

---

* Homogenious Co-ordinates:
> * It derives the general matrix equation that covers all the equations by translation, rotation and scaling.
> * General Equation:
> 	*  ![image](https://user-images.githubusercontent.com/68887544/115372643-bec50680-a1e8-11eb-87e2-28cc673c199f.png)
> * HOmogeneous Co-ordinates (Row Major):
> 	* ![image](https://user-images.githubusercontent.com/68887544/115381574-52023a00-a1f1-11eb-9f36-d157b2233a06.png)

---

* Rotation About Arbitrary point:
> * Translate arbitrary point to origin.
> * Rotate at θ angle
> * Translate back at same arbitrary position.
> * ![image](https://user-images.githubusercontent.com/68887544/115510442-5d12a400-a29d-11eb-807f-229d74f76ccb.png)
> * Final Equation:
> 	* ![image](https://user-images.githubusercontent.com/68887544/115510920-e9bd6200-a29d-11eb-83f8-3a5541ef5062.png)
>

---

* Shear:
> * Slanting or tilting something is called as shear
> * types:
> 	* X - shear : Only X co-ordinate change, y is preserved
> 	* Y - shear : Only y co-ordinate change, X is preserved
> * X - Shear Equation:
> 	* ![image](https://user-images.githubusercontent.com/68887544/115518819-3c028100-a2a6-11eb-9e16-b942724ef801.png)
> * Y - Shear Equation:
> 	* ![image](https://user-images.githubusercontent.com/68887544/115518988-68b69880-a2a6-11eb-81d6-248f03e180d9.png)
>
> * Shearing relative to other reference line:
> 	* ![image](https://user-images.githubusercontent.com/68887544/115536208-2ea1c280-a2b7-11eb-857f-b2f1c297cc06.png)


---

## 3D Tranformation:

* 3D
> * Dimension: defining a object in a physical spatial with minimum no. of co-ordinate is called as Dimension.
> * The number of ways in which we can move in a dimension is defined as no. of dimension.
> 	* 0D : We cannot move at all
>	* 1D : We can move in only one direction
> 	* 2D : We can move in two directions
> 	* 3D : We can move in all directions (3)

----

* 3D Translation:
> * Equation:
>   * ![image](https://user-images.githubusercontent.com/68887544/115537577-94db1500-a2b8-11eb-8724-08c32fab63de.png)
>

----

* 3D Scaling:
> * Equation:
> 	*   ![image](https://user-images.githubusercontent.com/68887544/115538761-d7512180-a2b9-11eb-8e0d-bf8850a9b857.png)

---

* 3D Rotation parallel to co-ordinate axis:
> * Equation z-axis:
>   * ![image](https://user-images.githubusercontent.com/68887544/115539641-d40a6580-a2ba-11eb-9988-8686663aa266.png)
> * Equation all axis:
>   * ![image](https://user-images.githubusercontent.com/68887544/115540213-7cb8c500-a2bb-11eb-9c51-dc6a7310a927.png)

---

## Projections:

* Projections:
> * Projection is the process of tranforming an object representation from n-dimensional space to less than n-dimensional space.
> * projection is the process of creating image on 2D plane.
> * View Plane or Projectin Plane: Plane where object is projected.
> * Types:
> 	* Parallel Projection
> 	* Perspective Projection
> 	*  ![image](https://user-images.githubusercontent.com/68887544/115541681-0ddc6b80-a2bd-11eb-817a-bf3a25c5b8a3.png)
> * Taxonomy of Projection:
>   * ![image](https://user-images.githubusercontent.com/68887544/115541885-44b28180-a2bd-11eb-9c6b-39aaf0d47ecd.png)
>
> * Rays of line is called as projector.
> *
---

* Parallel Projection:
> * Parallel projection is achieved by passing parallel rays from the object vertices and projecting the object on view plane.
> * All projection vectors are parallel to each other.
> * It preserves true shape and size of the object on view plane.
> * It fails to capture depth information and hence cannot produce a realistic view.
> * Types:
> 	* Orthographic Parallel projection
> 	* Oblique parallel projection
> 	* ![image](https://user-images.githubusercontent.com/68887544/115542078-80e5e200-a2bd-11eb-97a9-856061a94f89.png)
>   * ![image](https://user-images.githubusercontent.com/68887544/115542821-4c265a80-a2be-11eb-8ef2-9b8e19b2c698.png)

---

* Orthographic Projection:
> * Ortho means at Right angle.
> * If projectors are perpendicular to view plane, then it is called as orthographic projection.
> * Types:
> 	* Multiview: Top view, side view, bottom view, i.e we can generate multiple type of view but they can be seen in 2Dimensional view.
> 	* Auxinomatrix: Here we can see in all 3 dimensions
> 		* Isometric = All angle equal - ![image](https://user-images.githubusercontent.com/68887544/115545473-7a596980-a2c1-11eb-98bd-aaf2a8e6c933.png)
> 		* Dimetric = Two angles are not equal - ![image](https://user-images.githubusercontent.com/68887544/115545762-cdcbb780-a2c1-11eb-8335-028713f54014.png)
> 		* Trimetric = Three angles are not equal. -![image](https://user-images.githubusercontent.com/68887544/115545858-eb008600-a2c1-11eb-9a1e-786287391782.png)


---
* Oblique parallel Projection:
> * Projectors are parallel to each other but not perpendicular to view plane.
> * Types:
> 	* Cavalier
> 		* Keep bigger face of object
> 		* Strike rays at any angle
> 		* The length of image with wide length will be same and other edge length will be proportional.
> 		 
> 	* Cabinet:
> 		* Cabinet says if the angle is 63.4<sup>0</sup> then the wide length will look 1/2.
>

---

* Perspective Projection:
> * Lines of projection i.e projectors will intersect and we can see the lines meeting at one point, this point i s called as center of projection/ projection reference point.
> * It will give us realistic views.
> * Vanishing point: Like railway track, the parallell line seems meeting at infinity, such point is called as vanishing point.
> * Vanishing point types:
> 	* 1 point : if 1 vanishing point is created then called as 1 point.
> 	* 2 point : if 2 vanishing point is created then called as 2 point.
> 	* 3 point : if 3 vanishing point is created then called as 3 point.

---

> P.S. Done Unit III - 2D, 3D Transformation and Projection.
