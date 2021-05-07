# Unit I: Graphics Primitives and Scan Conversion Algorithm

## Introduction to Computer Graphics

### What is CG?
  * CG is a way of processing, generating, manipulating, storing and displaying images.
  * Two types:
    1. Interactive CG
        * It provides user a way to interact with the system.
        * In this type of CG, user provides an input and accordingly the output is generated.
    2. Non interactive CG
        * Also known as passive CG.
        * User have no way to interact with the system.


  * Operations :
    * Geometry: how to draw and represent scene
    * Animation: how to make obects move or how to add dynamic content in the scene
    * Rendering: how to add realistic light in the scene
    * Imaging: Image acquisition and image editing

### Graphic Primitives

  * Line : collection of points along a straight path
  * Line Segment : It is a part of line. Curves are often represented using small line segments
  * Vector : A line represented using both direction and magnitude.

### Basic Terminologies

* Pixel :
  * The smallest addressable unit of an image/screen.
  * Also known as pel or picture element.

 * Resolution:
    * Maximum number of pixel that can be displayed without overlap  on monitor screen.
    * Higher the resolution better the quality.
    * Number of pixel defines the actual number of samples are used from real valued scene.

 * Aspect ratio:
    * the ratio of number of vertical pixels to the number of horizontal pixels required to draw a line of same length in both direction is called as aspect ratio.

* Frame Buffer:
  * Large continuous section of computer memory is called frame buffer.
  * There is one bit memory for each pixel
  * Ideally, the size of frame buffer is same as screen resolution.
  * Frame buffer is known as bitmap if it uses 1 memory bit per pixel
  * Frame buffer is known as pixmap if it uses more than 1 memory bit per pixel

### Display Devices:

* Output devices used to display information is called as Display devices.

* CRT:
    * ![image](https://user-images.githubusercontent.com/68887544/114137972-9278d280-992a-11eb-9f9b-be2b7e0fddb8.png)
    * Persistence Rate:
       * It defines how long a pixel emits light after the CRT beam is removed.
       * The time it takes the emitted light to decay to 1-10th of its original intensity is called as the persistance of phosphor

---

> P.S. Done
