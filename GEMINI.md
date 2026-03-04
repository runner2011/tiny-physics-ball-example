# GEMINI.md - Tiny Physics Ball Example

This project demonstrates a simple 3D physics simulation of balls bouncing inside a box, implemented in three ways:
1.  **Canvas 2D API:** Uses a basic perspective projection and depth sorting to simulate 3D.
2.  **WebGL2:** Uses GPU-accelerated rendering with a perspective projection matrix.
3.  **WebGL2 GPGPU:** Performs both rendering and physics calculations on the GPU using shaders and textures, allowing for thousands of balls at high performance.

## Project Structure

- `src/tiny physics ball-canvas.html`: Pure JavaScript/Canvas 2D implementation with UI controls.
- `src/tiny physics ball-webgl.html`: WebGL2 implementation with shaders and adjustable ball limits.
- `src/tiny physics ball-webgl gpgpu.html`: High-performance GPGPU implementation (requires `EXT_color_buffer_float`).
- `res/`: Contains screenshots/previews of the simulations.

## Features

- **UI Controls:** Adjust bounding box dimensions, ball count, and camera distance in real-time.
- **FPS Monitoring:** Real-time performance tracking integrated into each simulation.
- **Interactivity:** Click on the canvas to add balls dynamically (GPGPU version).

## Physics Implementation

- **Integration:** Semi-implicit Euler integration.
- **Collisions:** 
    - 3D AABB (Axis-Aligned Bounding Box) for the container walls.
    - Ball-to-ball impulse-based collisions with position correction.
- **Constraints:** Fixed time-step with sub-stepping for stability.
- **GPGPU Version:** Uses texture-based state storage and fragment shaders to process physics updates in parallel on the GPU.

## Contribution Guidelines

- Keep the core physics logic simple and readable.
- If adding new features (e.g., friction, different shapes), implement them in all versions (Canvas, WebGL, GPGPU) if possible to maintain parity.
- Use Vanilla JavaScript; avoid external dependencies unless absolutely necessary.
- Ensure any UI or interactive elements work smoothly across different screen sizes.

## Testing

- Manually verify that balls do not escape the bounding box.
- Check for "tunneling" issues when adding many balls or increasing velocities.
- Verify that performance remains stable (target 60 FPS).
- Test GPGPU version with different numbers of balls to find hardware limits.
