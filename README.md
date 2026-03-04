# Tiny Physics Ball Example

A simple 3D physics simulation demonstrating ball-to-ball and ball-to-box collisions using both HTML5 Canvas 2D and WebGL2.

## Features
- 3D Physics Integration (Semi-implicit Euler)
- Impulse-based collisions
- WebGL2 GPGPU high-performance physics
- UI Controls for Bounds, Ball Count, and Camera
- Real-time FPS counter

## WebGL Performance Benchmarks
Perform these tests on your machine and record the average FPS after 10 seconds of simulation.

| Ball Count | Implementation | Target FPS | Recorded FPS |
|------------|----------------|------------|--------------|
| 100        | WebGL2 (CPU)   | 60         | [Pending]    |
| 1000       | WebGL2 (CPU)   | 60         | [Pending]    |
| 5000       | WebGL2 GPGPU   | 60         | [Pending]    |
| 10000      | WebGL2 GPGPU   | 30-60      | [Pending]    |
| 15000      | WebGL2 GPGPU   | 20-30      | [Pending]    |
| 30000      | WebGL2 GPGPU   | 10-20      | [Pending]    |

## Usage
Open any of the following files in a modern web browser:
- `src/tiny physics ball-canvas.html`: Canvas 2D version.
- `src/tiny physics ball-webgl.html`: WebGL2 (CPU-side physics) version.
- `src/tiny physics ball-webgl gpgpu.html`: WebGL2 GPGPU (GPU-side physics) version.
