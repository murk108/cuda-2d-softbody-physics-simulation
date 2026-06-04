**VIDEO:**

[<img src="https://img.youtube.com/vi/C_qEfIPdrrE/hqdefault.jpg" width="600" height="300" />](https://www.youtube.com/watch?v=C_qEfIPdrrE)

**DESCRIPTION:**

High performance softbody physics simulation written from scratch in C++/CUDA/OpenGL. Scales up to around 3-4M particles on my RTX 4070 Super at 60FPS. The main things that made this possible were:

- Fast spatial partitioning that's cache friendly and has linear time neighbor query and is entirely on the GPU
- CUDA usage + CUDA/OpenGL interop to offload the simulation to the GPU massively increasing performance, minimizing CPU-GPU talk
- Efficient instanced rendering + usage of GL_POINT_SPRITE to massively reduce vertex count
- Verlet integration for particle simulation to improve numerical stability and reduce positional drift
- Structures of Arrays instead of Array of Structures to improve cache locality
- Spring like constraints between particles, emergently forming soft bodies

**CONTROLS:**

E - Generate Softbody

R - Reset World

SPACE - Pause

G - Slow mo

LEFT CLICK - Particle mover

RIGHT CLICK - Move camera

**REQUIREMENTS TO COMPILE:**

GLEW

GLFW

Cuda Toolkit

**REQUIREMENTS TO RUN:**

NVIDIA GPU

