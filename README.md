# Grey-Scott Reaction-Diffusion Simulator

This project implements the **Grey-Scott reaction-diffusion model** using [NGSolve](https://ngsolve.org/), a high-performance finite element library. It simulates the emergence of complex patterns from simple chemical interactions and visualizes how parameters affect the evolution of these patterns over time.

![Sample Output](./images/grayscott-output.png)

## What is Reaction-Diffusion?

Reaction-diffusion systems model how substances react and diffuse through space. The **Grey-Scott model** is a two-variable system that simulates how an "activator" and an "inhibitor" interact. Despite its simplicity, it produces a wide variety of natural-looking patterns like spots, stripes, and waves.

## Inspiration

This model is inspired by the work of Pearson (1993) and Gray & Scott (1984). It's widely used in morphogenesis studies to explore how simple reaction rules lead to rich natural patterns.

## Features

- Full implementation of the Grey-Scott model in 2D
- Customizable parameters (diffusion, feed, kill rate, time step)
- Interactive visualization of pattern formation
- Periodic boundary conditions for seamless pattern tiling
- Support for different mesh geometries (square, circular, etc.)
- Efficient FEM discretization via NGSolve

## Parameters and Control

You can experiment with the following model parameters:

| Parameter | Description                       | Typical Values      |
|----------:|-----------------------------------|---------------------|
| `D_u`     | Diffusion rate of U (activator)   | 0.01 – 0.08         |
| `D_v`     | Diffusion rate of V (inhibitor)   | ~0.5 * D_u          |
| `F`       | Feed rate                         | 0.03 – 0.07         |
| `k`       | Kill rate                         | 0.055 – 0.065       |
| `dt`      | Time step                         | 1 – 2               |
| `iterations` | Number of time steps          | 1000 – 5000         |

## Running the Simulation

To run the simulation, use the sagma function with your parameters. For example:

```python
sagma(D_u=0.064, F=0.035, k=0.057, dt=1, iterations=3000)
```


