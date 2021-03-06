CUDA Rasterizer
===============

[CLICK ME FOR INSTRUCTION OF THIS PROJECT](./INSTRUCTION.md)

**University of Pennsylvania, CIS 565: GPU Programming and Architecture, Project 4**

* Yan Wu
	* [LinkedIn](https://www.linkedin.com/in/yan-wu-a71270159/)
* Tested on: Windows 10, i7-8750H @ 2.20GHz 16GB, GTX 1060 6GB (Personal Laptop)

### Brief Introduction
In this project, I used CUDA to implement a simplified rasterized graphics pipeline, similar to the OpenGL pipeline. I implemented vertex shading, primitive assembly, rasterization, fragment shading, and a framebuffer for the basic pipeline. And there are also some extra features.

* [What is rasterization?](https://en.wikipedia.org/wiki/Rasterisation)
* Basic pipeline
  * Clear the fragment buffer with some default value.
  * Vertex shading
  * Primitive assembly
  * Rasterization
  * Fragments to depth buffer
  * Fragment shading
  * Fragment to framebuffer writing
* SSAA implemented
* UV texture mapping with bilinear texture filtering and perspective correct texture coordinates

### Results

* Results for basic Pipelines<br />
  <img src="/images/basic pipeline/triangle.gif" width="30%">
  <img src="/images/basic pipeline/box.gif" width="30%">
  <img src="/images/basic pipeline/duck.gif" width="30%">
  
* After implementing SSAA <br />
  <img src="/images/SSAA/truck.gif" width="45%">
  <img src="/images/SSAA/truck2.gif" width="45%"> <br />
  - Clearly, after implementing SSAA, the aliasing problem decreases. If you look carefully at the outline of the truck, the left one is more tooth-shaped.

* Implementing UV texture mapping with [bilinear texture filtering](https://en.wikipedia.org/wiki/Bilinear_filtering#Sample_code) and [perspective correct texture coordinates](https://www.scratchapixel.com/lessons/3d-basic-rendering/rasterization-practical-implementation/perspective-correct-interpolation-vertex-attributes) <br />
  <img src="/images/texture mapping/board.gif" width="45%">
  <img src="/images/texture mapping/board1.gif" width="45%"> <br />
  - After implementing these two features, we can see the difference. With the left original result, the perspective is weird and the texture resolution is not as good as the right one. The right result looks much more comfortable.
  


### Credits

* [ScreenToGif(used in this project)](https://www.screentogif.com/)
* [tinygltfloader](https://github.com/syoyo/tinygltfloader) by [@soyoyo](https://github.com/syoyo)
* [glTF Sample Models](https://github.com/KhronosGroup/glTF/blob/master/sampleModels/README.md)
