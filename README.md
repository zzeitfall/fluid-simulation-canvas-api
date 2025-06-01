# Fluid Simulation Journey

## What is it?

This is a [personal project](https://github.com/zzeitfall/fluid-simulation-canvas-api) created for exploritary and learning purposes. The field of interest is fluid dynamics based on Navier-Stokes equations for incompressible flow. The goal is to understand the numerical methods behind the fluid simulation solver and implement them.

## Implementations

- [Attempt #1](https://zzeitfall.github.io/fluid-simulation-canvas-api/pages/first.html). This was my first attempt at diving deep into fluid simulation based on Navier-Stokes equations. I had a really tough time with all this math involved for the simulation, as well as translating it to the functional code. This solver uses a simple collocated grid to represent vector and scalar quantities. Also, it uses simple Jacobi method to solve the Poisson equation for pressure. I am sure this solver has numerous inaccuracies and simplifications, primarily due to the gaps in my math. Anyways, this attempt was an essential step toward understanding fluid dynamics and translating theoretical concepts into functional code. The implementation primarily drew inspiration from [GPU Gems by Nvidia](#gpu-gems) and [Real-Time Fluid Dynamics for Games by J. Stam](#stam-fluid)

- [Attempt #2](https://zzeitfall.github.io/fluid-simulation-canvas-api/pages/second.html). My second attempt was focused on achieving greater accuracy and refinement. With a better understanding of the underlying math, I switched to a staggered (MAC) grid for vector quantities such as the velocity field. This solver uses the Red-Black Gauss-Seidel (RBGS) method to solve the Poisson equation for pressure. Also, I intentionally dropped the viscosity term (i.e. the diffusion step), as I believe it doesn't add significant value to the simulation. These improvements result in faster convergence and better simulation performance (1.5-2x). That said, one thing I still haven't figured out is how to properly implement boundary conditions to make the smoke reflect off the walls. Hopefully, I'll get this in the future and finish the solver! It worth to mention [Fluid Notes by Robert Bridson](#fluid-notes) article, which helped me a lot - I highly recommend it. \
_P.S._ [This video](https://www.youtube.com/watch?v=iKAVRgIrUOU) is legendary! The author does a fantastic job explaining how to enforce incompressibility using the Gauss-Seidel method with over-relaxation, which dramatically reduces the number of iterations. Moreover, this method requires two iterations (or even more with over-relaxation) less through the grid.

## Useful Links

1. <a id="fluid-notes" href="https://www.cs.ubc.ca/~rbridson/fluidsimulation/fluids_notes.pdf" target="_blank">Fluid Notes by R. Bridson</a>
2. <a id="gpu-gems" href="https://developer.nvidia.com/gpugems/gpugems/part-vi-beyond-triangles/chapter-38-fast-fluid-dynamics-simulation-gpu">GPU Gems by NVidia</a>
3. <a id="stam-fluid" href="https://graphics.cs.cmu.edu/nsp/course/15-464/Spring11/papers/StamFluidforGames.pdf">Real-Time Fluid Dynamics for Games by J. Stam</a>

## Contact Me

- [Github (@zzeitfall)](https://github.com/zzeitfall)
- [Mail (zzeitfall@gmail.com)](mailto:zzeitfall@gmail.com)
