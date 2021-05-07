# Unit V - Curves and Fractals

## &#10023; Syllabus:
> * Curves:
>   * Introduction
>   * Interpolation and Approximation
>   * Blending Function
>   * B-Spline Curve
>   * Bezier Curve
> * Fractals:
>   * Introduction
>   * Classification
>   * Fractal Generation:
>       * Snowflake
>       * Triadic Curve
>       * Hilbert curve
>       * Applications

---

## &#10023; Curves:

* **Introduction:**
> * Whatever you draw continuously without lifting up pen is called as curve.
> * i.e set of points joined continuously is called as curve.
> * Representation:
>   * Explicit
>   * Implicit
>   * Parametric form

---

* **Interpolation and Approximation:**
> * Curve is specified by a set of control points.
> * **Interpolation:**
>   * If the curve passes through the control points, it is called interpolation.
>   * **Interpolation** curves are used in animation and specifying camera motion. It is also used in digitizing the coordinates
> * **Extrapolation/Approximation:**
>   *  If the curve does not pass through the control points and approximate the shape, it is called Approximation or Extrapolation.
>   * Such curvevs are used to estimate the shape of the object surface.
> * Example:
>  ![image](https://user-images.githubusercontent.com/68887544/115949419-aad41a00-a4f2-11eb-822f-8e6b037117b3.png)
> * Convex Hull:
>   * The curve is satisfying convex hull property if the  entire curve lies within the convex hull.
>   * ![image](https://user-images.githubusercontent.com/68887544/115949464-f2f33c80-a4f2-11eb-947f-ab7002aea989.png)
>   * Clipping the curve satisfying convex hull property is easy.
>   * Trivial acceptance and rejection conditions are easy to evaluate for them.
>   * If bounding box of the convex hull is inside Clipping region, no need to clip the curve. And if a bounding box is completely outside clipping window, clip the entire curve.
---

* **Blending Function:**
> ![image](https://user-images.githubusercontent.com/68887544/115949590-c855b380-a4f3-11eb-8876-265a00de3d60.png)
> ![image](https://user-images.githubusercontent.com/68887544/115949816-3058c980-a4f5-11eb-8745-8e890c6d9152.png)
> ![image](https://user-images.githubusercontent.com/68887544/115949611-e3c0be80-a4f3-11eb-9372-193f552af0bc.png)

---

* **Bezier Curve:**
> * This is an approximate spine curve.
> * With cubic polynomials, Bezier curve can approximate any number of control points.
> * In Bezier curve, the degree of polynomial depends on a number of control points used to generate curve segment.
> * In Bezier curve, the degree of the polynomial is always one less than a number of control points.
> ![image](https://user-images.githubusercontent.com/68887544/115950160-3ea7e500-a4f7-11eb-8b52-fdf365d0b18c.png)
> * With n + 1 control points,parametric equation of Bezier curve approximating points p<sub>0</sub> to p<sub>n</sub>,
>   * ![image](https://user-images.githubusercontent.com/68887544/115950224-a2caa900-a4f7-11eb-86d0-a194104ad58d.png)
> * ![image](https://user-images.githubusercontent.com/68887544/115950236-b6760f80-a4f7-11eb-9aa0-b7768129c962.png)
> * ![image](https://user-images.githubusercontent.com/68887544/115950251-c261d180-a4f7-11eb-9c4a-3931cf319ec4.png)
> * Properties of Bezier Curves:
>   * Degree of the curve is one less than a number of control points
>   * Always interpolates first and last control points and approximates remaining two.
>   * The slope of the derivative at the beginning is along the line joining the first two points and slope of the derivative at the end is along the line joining last two points.
>   * Bezier curve always satisfies the convex hull property.
>   * At any parameter value t, sum all four Bezier blending function is always 1, i.e,
>       *   ![image](https://user-images.githubusercontent.com/68887544/115950468-0e614600-a4f9-11eb-9eb3-ea0cecea9aac.png)
>   * Polynomial Smoothly follows the control points without much oscillation.
>   * Bezier curves do not have local control; repositioning one control point changes the entire curve.
>   * The curve is invariant under affine trnaformation.
>   * The basis functions are real.
>   * The curve exhibits variation diminishing property, i.e. any line intersects the Bezier curve at most as often as that line intersects the polygon interpolating control points.
>   * Bezier curve can fit any number of control points.
>   * Reversing the order of control points yield the same Bezier curve.
> * **Applications of Bezier Curve:**
>   * ![image](https://user-images.githubusercontent.com/68887544/115950588-c68eee80-a4f9-11eb-8ec5-9d0579a8f667.png)
> * Cubic Bezier Curves:
>   * Cubic Bezier curves are bridge between computation cost and smoothness.
>   * They are very flexible and estimate shape nicely.
>   * We should specify four control points to generate a cubic Bezier curve.
>   * Blending functions for cubic Bezier curve is derived by putting n = 3 in the equation of Bezier curve,
>       *  ![image](https://user-images.githubusercontent.com/68887544/115950716-8da34980-a4fa-11eb-8f4a-d9816fbd00c2.png)
>   * ![image](https://user-images.githubusercontent.com/68887544/115950761-ccd19a80-a4fa-11eb-8ebc-de0c53f9c98d.png)
>   * ![image](https://user-images.githubusercontent.com/68887544/115950772-d78c2f80-a4fa-11eb-983b-c5e10fb6fc0d.png)
>   * Matrix Representation:
>     * ![image](https://user-images.githubusercontent.com/68887544/115950811-17ebad80-a4fb-11eb-97a4-58b8fd4a9601.png)
>   * Limitation of Bezier curve:
>     * ![image](https://user-images.githubusercontent.com/68887544/115950897-91839b80-a4fb-11eb-8485-cd2bc2206daa.png)
>   * Subdivision Method:
>     * ![image](https://user-images.githubusercontent.com/68887544/115950939-ba0b9580-a4fb-11eb-8d76-2cd5ec6121eb.png)

---

* **B-Spline Curve:**
>  * ![image](https://user-images.githubusercontent.com/68887544/115951021-2a1a1b80-a4fc-11eb-86e5-a1e373e95142.png)
>  * ![image](https://user-images.githubusercontent.com/68887544/115951034-37cfa100-a4fc-11eb-9c60-9f2d4eed8425.png)
>  * ![image](https://user-images.githubusercontent.com/68887544/115951045-3ef6af00-a4fc-11eb-94fe-d7613a48b8ae.png)
> * ![image](https://user-images.githubusercontent.com/68887544/115951051-47e78080-a4fc-11eb-98e7-76e6c05dc6f2.png)
> * ![image](https://user-images.githubusercontent.com/68887544/115951053-4c139e00-a4fc-11eb-848e-d889e07e8dc9.png)
>

---

* **Bezier VS B-Spline Curve:**
> ![image](https://user-images.githubusercontent.com/68887544/115951531-d9f08880-a4fe-11eb-9f02-03d2e289d2be.png)

---

## &#10023; Fractals:

* **Fractals:**
> * Fractals are infinitely complex patterns that are self similar across different scales.
> * Properties:
>   * Infinite detail at every point.
>   * Self-similarity between object parts.
>   * Natural objects have infinite details; however, we should design a process which produces finite  detail because on the computer we cannot display infinite detail.
>   * After certain levels of zoom in, Euclidean shapes lead to smooth drawing. While in the fractal object, if we keep zoom in, we continue to see the same detail as it appears in the original object.
>   * ![image](https://user-images.githubusercontent.com/68887544/115954768-66577700-a510-11eb-99d2-4eea83132d5a.png)
>   * Zoom in effect on the monitor is achieved by selecting a smaller and smaller window with the same viewport. Less and less detail is mapped to the same size as the viewport.

---

* **Classification:**
> * Self-similar fractals:
>   * Such fractal exhibits the self-similarity in shape.
>   * We can construct the object by applying different scaling factors to all parts or by using the same scaling factor for all.
>   * If we use a random scaling factor to generate the subparts, a fractal is called statistically self-similar.
>   * statistically self similar fractals are used to construct shapes like tree, shrubs, plants etc.
> * Self-affine fractals:
>   * Such fractals use different scaling factors for all three directions. We can add random variation to get statistically self-affine fractals. This class of fractals is best suited to model terrain, water, clouds etc.
> * Invariant fractals:
>   * Nonlinear transformation is applied to construct such fractals. A self-squaring function in complex space produces self-squaring fractals like Mandelbro. Self-inverse fractals are generated using the inversion procedure.
> * ![image](https://user-images.githubusercontent.com/68887544/115955031-db777c00-a511-11eb-9b3a-a13e4157e9a5.png)

---

* **Fractal generation:**
> ![image](https://user-images.githubusercontent.com/68887544/115955080-31e4ba80-a512-11eb-9148-d8e24a995270.png)
> ![image](https://user-images.githubusercontent.com/68887544/115955086-36a96e80-a512-11eb-935e-cd92d61d69f7.png)
> ![image](https://user-images.githubusercontent.com/68887544/115955096-4032d680-a512-11eb-9de0-734e00975984.png)

---

* **Application:**
> * Fractals are used to model the natural shapes. Some of the prominent application areas of fractals are listed here:
>   * Modelling natural structures like Geographic terrain, mountain, plant structure, clouds, vegetables, etc.
>   * study of the chaotic phenomenon.
>   * Fractal art
>   * Space research
>   * Study of convergence of iterative processes
>   * Engineering and architecture.
>   * Medical science.
>   * Chemical processes.
>   * Medical diagnostic images.
>   * Fluid mechanics
>   * Image compression
>   * Telecommunication

---
> P.S. Done Unit V - Curves and Fractals.
