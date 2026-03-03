# GEMINI.md - Tiny Physics Ball Example

This project demonstrates a simple 3D physics simulation of balls bouncing inside a box, implemented in two ways:
1.  **Canvas 2D API:** Uses a basic perspective projection and depth sorting to simulate 3D.
2.  **WebGL2:** Uses GPU-accelerated rendering with a perspective projection matrix.

## Project Structure

- `src/tiny physics ball-canvas.html`: Pure JavaScript/Canvas 2D implementation.
- `src/tiny physics ball-webgl.html`: WebGL2 implementation with shaders.
- `res/`: Contains screenshots/previews of the simulations.

## Physics Implementation

- **Integration:** Semi-implicit Euler integration.
- **Collisions:** 
    - 3D AABB (Axis-Aligned Bounding Box) for the container walls.
    - Ball-to-ball impulse-based collisions with position correction.
- **Constraints:** Fixed time-step with sub-stepping for stability.

## Contribution Guidelines

- Keep the core physics logic simple and readable.
- If adding new features (e.g., friction, different shapes), implement them in both the Canvas and WebGL versions if possible to maintain parity.
- Use Vanilla JavaScript; avoid external dependencies unless absolutely necessary.
- Ensure any UI or interactive elements work smoothly across different screen sizes.

## Testing

- Manually verify that balls do not escape the bounding box.
- Check for "tunneling" issues when adding many balls or increasing velocities.
- Verify that performance remains stable (target 60 FPS).
