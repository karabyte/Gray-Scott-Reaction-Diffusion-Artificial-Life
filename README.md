# Gray-Scott-Reaction-Diffusion-Artificial-Life
GPU-accelerated artificial life simulation using CUDA and the Gray-Scott reaction-diffusion model to generate emergent biological patterns through massively parallel cellular interactions.
### Technical Overview
This project implements a GPU-accelerated Gray–Scott reaction-diffusion system using CUDA and C++. The simulation models the interaction and diffusion of two chemical fields, producing complex emergent patterns from simple local rules.

The Gray–Scott equations are discretized using a finite-difference scheme with a weighted 9-point Laplacian stencil:

∂U/∂t = Du∇²U − UV² + F(1 − U)

∂V/∂t = Dv∇²V + UV² − (F + k)V

Each CUDA thread updates one grid cell, allowing thousands of cells to be processed in parallel. Double-buffered GPU fields are used to avoid read/write conflicts between simulation steps.

**Core techniques:**

* CUDA C++
* GPU parallel computation
* Gray–Scott reaction-diffusion
* Finite-difference discretization
* 9-point Laplacian stencil
* Ping-pong GPU buffers
* Parallel cellular updates
* Emergent pattern formation
* Artificial life / morphogenesis
