
# Rust Experiments

This project contains a number of experiments in the simulation / graphics category. I frequently write Haskell projects where I delegate the performance critical, numerical code to C/C++ or offload it to the GPU. I wanted to try using Rust as a safer and more functional alternative. The application itself is written in Haskell, doing the display, user interaction and non-inner-loop parts with the actual computations done in a Rust library.

![rust-exp](https://raw.github.com/blitzcode/rust-exp/master/screenshot.png)

Experiments include...

- **Software rasterizer** using half-space functions, doing perspective and sub-pixel correct, gap-less rasterization, depth buffering, switchable between vertex and pixel shading, many different shaders implemented, does IBL based on pre-filtered irradiance cubemaps, different environments included, a selection of scenes, many with baked ambient occlusion or radiosity, build-in benchmarking, gamma corrected output, selectable backgrounds, parallelized
- Gravitational **N-Body simulation**, both a brute force O(N^2) and the O(n log n) Barnes-Hut algorithm are implemented, adjustable time step and cutoff criteria, rendering of alpha blended particles with tails, parallelized, multiple interesting initial configurations to choose from
- The famous **'Game of Life' cellular automata**, optimized and parallelized implementation, library of recallable patterns

**If you want to read actual algorithm descriptions and references for these experiments, including more, higher quality images visit the following link to my website**

[Rust projects on Blitzcode.net](http://www.blitzcode.net/rust.shtml)

The Haskell application itself might also be of interests. It features a pluggable experiment framework, modern OpenGL 3/4.x style rendering, text, quad rendering, screenshots, framebuffer system, FPS counter, GLSL, logging etc. A good starting point for your own Haskell + OpenGL adventures. Also see my other [Haskell and GLSL program containing my distance field / ray marching related experiments](https://github.com/blitzcode/ray-marching-distance-fields/).

# Building

This project uses the Stack / Cabal tools (`stack build`) for building the Haskell code and Cargo (`cargo build --release`) for building the Rust code. There's a top-level Makefile invoking both, simply do

    make

once you have Stack and Cargo / Rust installed.

# Legal

This program is published under the [MIT License](http://en.wikipedia.org/wiki/MIT_License).

# Author

Developed by Tim C. Schroeder, visit my [website](http://www.blitzcode.net) to learn more.

