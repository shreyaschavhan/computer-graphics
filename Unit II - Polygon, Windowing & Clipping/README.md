# Unit II - Polygon, Windowing &  Clipping

## Polygon:
* Polygon:
> * Defination: A figure or diagram drawing by joining more than two lines is called as polygon.
> * Types of polygons:
> * The classification of polygon is based on whre the line segment joining any two points within the polygon is going to lie.
> 	- Convex Polygon: Line segment joining two points inside the polygon. (Line angle is less than 180^0)
> 	- Concave polygon: Line segment joining two points outside the polygon. (at least one angle is more than 180^0 )
> 	- Complex polygon: Polygon with intersecting edges in called as complex polygon.


---

* Inside Test:
> * We do inside test to check if the given pixel is  inside the polygon or not.
> * Even - Odd Method:
> 	* Construct a line segment between the point in question & a known to be outside polygon.
> 	* Count t he intersection of line with polygon boundaries.
> 		* Inside : Odd no. of intersection
> 		* Outside: even no. of intersection
> 	* If intersection point in vertex: Then look at other end points of line segment.
> 		* If points are on same side of constructed line then "even no. of intersection" for only that intersection
> 		* If points are on different side of constructed  line " then odd no. of intersection" for only that intersection.
>
> * Winding number Rule:
> 	* Initialize winding no = 0
> 	* If line crosses an edge directed bottom
> 		* to top then add 1 to winding no.
> 		* to top-botoom add -1 to winding number
> 		* left to right right to left : no value
>	* Point outside if w.no = 0
> 	* otherwise Inside

---
## Polygon Filling:

* Polygon Filling:
> * We have two methods to fill polygon,
> 	* 1. seed fill and
> 	* 2. scan line algorithm
>

---

* Seed Fill:
> 	* We have two approaches:
>		* Flood fill algorithm
> 		* Boundary fill algorithm

---

* Boundary Fill Algorithm:
> * We can use boundary fill, where boundary of polygon is of same colour.
> 	* Two methods:
> 		* 4 Connected
> 		* 8 Connected
>	* 4 connected:
>		* Step I: It checks if pixel is already in the colour that we need as output.
>		* Step II: It checks if has same colour as boundary.
>		* If not you can fill
>		* Step III: Fill
>		* Ab boundary fill yeh kehta hai ki yeh khud toh dub gaya lekin apne passwale 4 ko leke bhi dubega.
> 		* 4 connected means, the 4 pixels around the selected pixel will be filled
> 		* (x,y) ---> (x+1, y), (x-1,y), (x, y+1), (x,y-1)
>                      *  ![image](https://user-images.githubusercontent.com/68887544/115138828-1da14900-a04c-11eb-9f01-fc69297bad79.png)
>	* 8 Connected:
>		* Same as 4-connected but also diagonal elements are considered.
> 		* ![image](https://user-images.githubusercontent.com/68887544/115139146-fe0b2000-a04d-11eb-8c7d-38eb453ccbdf.png)
>	* Algorithm:
>	* 4 Connected:
>		* ```
>			boundary_fill(x,y,fill_colour, boundary_colour){
>				if(getPixel(x,y)!=boundary_colour && getPixel(x,y)!=fill_colour){
>					putPixel(x,y, fill_colour){
>						boundary_fill(x+1, y,fill_colour, boundary_colour);
>						boundary_fill(x-1, y,fill_colour, boundary_colour);
>						boundary_fill(x, y+1,fill_colour, boundary_colour);
>						boundary_fill(x, y-1,fill_colour, boundary_colour);
>					}
>				}			
>			}
>
>
>	* 8 Connected:
>		* ```
>			boundary_fill(x,y,fill_colour, boundary_colour){
>				if(getPixel(x,y)!=boundary_colour && getPixel(x,y)!=fill_colour){
>					putPixel(x,y, fill_colour){
>						boundary_fill(x+1, y,fill_colour, boundary_colour);
>						boundary_fill(x-1, y,fill_colour, boundary_colour);
>						boundary_fill(x, y+1,fill_colour, boundary_colour);
>						boundary_fill(x, y-1,fill_colour, boundary_colour);
>						boundary_fill(x+1, y+1,fill_colour, boundary_colour);
>						boundary_fill(x+1, y-1,fill_colour, boundary_colour);
>						boundary_fill(x-1, y+1,fill_colour, boundary_colour);
>						boundary_fill(x-1, y-1,fill_colour, boundary_colour);
>					}
>				}			
>			}
>		
>		
---
* Flood Fill Algorithm:
> * If boundary colour is different then we use  flood fill.
> * Same as boundary fill, 4 connected 8 connected
> * Algorithm:
>	* ```
> 		flood_fill(x,y, old_colour, new_colour){
>			if(getpixel(x,y)==old_colour){
>				putpixel(x,y,new_colour){
>					flood_fill(x+1, y, old_colour, new_colour);
>					flood_fill(x-1, y, old_colour, new_colour);
>					flood_fill(x, y+1, old_colour, new_colour);
>					flood_fill(x, y-1, old_colour, new_colour);
>
>				}
>			}
>		} ```
> * same for 8 connected

---

* Scan Line Fill Algorithm:
> * Disadvantages of Seed fill over scan line fill:
> 	* Seed fill uses 4 to 8 connected approach
> 	* We used to  use stack there in seed fill, it can cause stack overflow.
>
> * What does scan line fill algorithm does:
> 	* Scan line algorithm directly fills pixels in between the right most and left most  point on the polygon.
> * Steps:
> 	* Locate the intersection points of the scan line with the polygon.
> 	* Pairing intersection points
> 	* move down side as per scan line & sort all pairs.
> 	* All pairs are sorted from y<sub>max</sub> to y<sub>min</sub>
> 	* Side get sorted on intersection point bases.
> 	* Area filling starts now.
> * Diagram:
> 	* ![image](https://user-images.githubusercontent.com/68887544/115190134-33bf1000-a105-11eb-8cd3-35a0c1e1ce7e.png)
>
> * Coherence Property:
> 	* Relating property of one scene to another part of scene.
> 	* Slope of line is 'm'
> 		* m = ![img](http://www.sciweavers.org/upload/Tex2Img_1618813922/render.png)
>		* ![image](https://user-images.githubusercontent.com/68887544/115191904-b5b03880-a107-11eb-97f5-4cc6a31762ea.png)

---

## Windowing and Clipping:

* View Transformation:
> * Windows to viewport:
> 	* ![image](https://user-images.githubusercontent.com/68887544/115193508-e5604000-a109-11eb-8200-3ee9538494f0.png)
> 	* Normalization Transformation:
> 		* ![image](https://user-images.githubusercontent.com/68887544/115194435-18570380-a10b-11eb-98b9-9a3fa27671ee.png)
>	* Workstation Transformation:
>		* ![image](https://user-images.githubusercontent.com/68887544/115194740-7d125e00-a10b-11eb-9fa6-4bdd2109532c.png)
>

---

* 2D Clipping:
> * Types of Clipping:
> 	* Point Clipping
> 	* Line Clipping
>		* Cohen-Sutherland line clipping algorithm
> 	* Polygon Clipping
> 		* Sutherland-hodgeman polygon clipping algo
> 	* Curve Clipping
> 	* Text Clipping
>
> * What is clipping:
> 	* Cropping image is indirectly called as Clipping
> 	* Clipping is a procedure by which we can select or reject a particular portion of an image in a specified region of a space.
> * Clipping window: Region in which we have to  show our image.
>  
---

* Cohen - Sutherland Line Clipping Algorithm:
> * He divided window in 9 parts of 4-bit region code.
> * Top Bit, Bottom bit, right bit, left bit.
> 	* Ex.
> 	*  ![image](https://user-images.githubusercontent.com/68887544/115196669-cf547e80-a10d-11eb-9ae3-5cc910b76748.png)
> * Rules:
> 	* If end points of a line have region code 0000, then the line is completely inside the clipping window.
> 	* If region code of a line's end points have same 1 bit position then line is completely  outside.
> 	* If region code of both end points are not 0000 or mixup region code then perform logical AnD operation of end points, if AND is not equal to 0000, reject otherwise partially clipped.
> 	
> * Slope intercept method:
> * m = (y2-y1)/(x2-x1)  
> * Fomulaes:
> 	* ![image](https://user-images.githubusercontent.com/68887544/115198479-b9e05400-a10f-11eb-9360-d238385abcc5.png)
> 	* Top:
> 		* ![image](https://user-images.githubusercontent.com/68887544/115199111-75a18380-a110-11eb-9d2b-d8f0433c09e4.png)
> 	* Cut Left:
> 		* ![image](https://user-images.githubusercontent.com/68887544/115199616-05473200-a111-11eb-9c74-59933b396755.png)
>	* Cuts bottom and Right:
>		* ![image](https://user-images.githubusercontent.com/68887544/115199930-548d6280-a111-11eb-9f52-f361d5013041.png)
> 	* Right:
> 		* ![image](https://user-images.githubusercontent.com/68887544/115200132-83a3d400-a111-11eb-8c26-37eb4e6431f6.png)

---

* Sutherland Hodgeman polygon-clipping Algorithm:
> * we will give computer a list of vertices(which are inside and intersect)
> * 4 rules:
>	* ![image](https://user-images.githubusercontent.com/68887544/115201238-bc907880-a112-11eb-8d3b-d0901041d01d.png)
> * Best result on Convex polygon.
> * For concave polyhon: Extraneuos lines, at least an angle > 180^0

---

* Weiler atherton polygon clipping algorithm:
>  * Polygon --> Subject polygon
> * Clipping window --> Clip Polygon
> * We will create two list here-
> * Subject polygon list will be used for inserting insertion points
> * Clip polygon list will be used for leaving intersection point.
> 	* ![image](https://user-images.githubusercontent.com/68887544/115215685-61b24d80-a121-11eb-9324-995d411a1139.png)
> * Weiler Atherton overcomes the disadvantages of sutherland hodgeman algorithm
>
---

> P.S. Done Unit II - Polygon, Windowing & Clipping
