# Birds Flocking Simulation (BOIDs Algorithm)
## Demo
![boids-ezgif com-video-to-gif-converter](https://github.com/amin1nasim/bird-flocking-simulation/assets/49731000/eb155604-1005-446b-a455-547dd403f0f2)

## BOIDs Algorithm

The BOIDs algorithm ([wikipedia](https://en.wikipedia.org/wiki/Boids)) simulates the behavior of birds through three primary forces:

1. **Cohesion**: Boids are attracted to the center of mass of their neighbors.
2. **Alignment**: Boids align their velocity with nearby boids.
3. **Separation**: Boids avoid crowding and collisions with each other.

These forces are influenced by the immediate neighborhood of each boid, as boids have limited perception and a specific angle of view. Boids cannot see or be affected by others behind them. The dot product is used to determine if one boid is within another boid's field of view.

## Grid

To efficiently track a large number of boids and run the simulation in real time, a grid-based acceleration structure is used. A sphere is placed within the grid to keep the boids contained. Boids that venture outside the grid or into its corners are subjected to a force that pulls them back toward the grid's center.

## Avoiding Obstacles

In this project, a steering technique is employed to prevent boids from colliding with obstacles. The position and radius of obstacles can be adjusted via the control panel. When a boid approaches an obstacle, it experiences an acceleration perpendicular to its current velocity, steering it away from potential collisions.
