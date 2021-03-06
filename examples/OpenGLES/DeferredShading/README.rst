===============
DeferredShading
===============

.. figure:: ./DeferredShading.png

This example demonstrates optimal deferred shading using Pixel Local Storage (PLS).

API
---
* OpenGL ES 3.0+

Description
-----------	
Traditional rendering algorithms submit geometry and immediately apply shading effects to the rasterized primitives. Complex shading effects may require multiple draw calls (one per object per light) or render passes to produce the final pixel colour, with the geometry submitted every pass. 

Deferred shading is an alternative rendering technique that submits the scene geometry once, storing per-pixel attributes into local video memory to be used in the subsequent rendering passes. 

In these later passes, light volume primitives are rendered, and the per-pixel attributes contained in the buffer are retrieved at a 1:1 mapping ratio so that each pixel is shaded individually.

With the PowerVR architecture, the developer can use fast on-chip memory instead of the render target by using the Pixel Local Storage OpenGL ES extension.

Requires the extension ``GL_EXT_shader_pixel_local_storage`` for PLS.

Controls
--------
- Action1- Pause
- Action2- Orbit camera
- Quit- Close the application