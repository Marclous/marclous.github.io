---
title: "Assignment 5 Particle System"
date: 2025-02-26
categories: [The Nature of Code]
tags: [javascript, p5js]     # TAG names should always be lowercase
---
# Exploring the Cosmos: An Interactive Solar System Simulation

**[Solar System Simulation](https://editor.p5js.org/Marc1ous/sketches/YP3Nq5Om7)**

*An interactive p5.js visualization that brings our solar system to life with elliptical orbits, planetary rotation, and day/night cycles.*

## Summary

This project creates an interactive simulation of our solar system using p5.js. The planets follow elliptical orbits based on Kepler's laws, complete with proper inclinations and eccentricities, while maintaining visibility and interactivity.

The simulation features the Sun at the center with all eight planets orbiting at scaled distances. Each planet displays a day/night cycle based on its actual rotation period, with Venus and Uranus correctly showing retrograde rotation. Major moons are included for Earth, Mars, Jupiter, and Saturn, each following orbital mechanics around their parent planets. Saturn's iconic rings are represented visually.

Interactive elements allow users to:
- Adjust simulation speed to observe orbital periods
- Zoom in/out to focus on specific regions
- Toggle orbit paths and labels
- Select and follow individual celestial bodies
- View astronomical data for any selected object

A notable aspect of the simulation is how it balances scientific principles with visual clarity. While the actual size ratio between the Sun and planets would make the planets nearly invisible, I've used a logarithmic scaling approach that preserves relative size relationships while keeping everything visible. Similarly, distances are compressed to fit within the screen while maintaining relative proportions.

The code architecture uses object-oriented principles with a base `CelestialBody` class that handles common properties and behaviors, while specialized classes (`Star`, `Planet`, and `Moon`) implement specific characteristics. This approach makes the code modular and extensible, allowing for future additions like comets, asteroids, or exoplanetary systems.

## Inspiration

My inspiration for this project is from a simple thought to simulate a natural system in code. The solar system presented an ideal choice - a complex, dynamic system. The project became an exercise in translating the natural system into a programmatic representation. Rather than building from specific artistic or scientific references, the simulation emerged from a straightforward goal: to capture the essence of our solar system's movement in an interactive digital format.

## Process

The development started with a simple circular orbit system with planets represented as basic spheres. The first major challenge was implementing Kepler's laws for elliptical orbits, which required working with the polar form of the ellipse equation and managing the true anomaly calculation.

Adding the day/night cycle visualization proved surprisingly complex. I needed to rotate each planet on its axis independent of its orbital position, while ensuring that retrograde planets (Venus and Uranus) rotated in the correct direction. Achieving this visually with the arc() function required careful consideration of rotation angles and fill colors.

One persistent struggle was finding the right balance for size and distance scaling. Too accurate, and planets became invisible dots; too simplified, and the educational value diminished. I experimented with different scaling algorithms before settling on a logarithmic approach for sizes and a compressed linear model for distances.

The moon systems required a nested orbital calculation approach, as each moon needed to orbit its planet while the planet orbited the Sun. Managing this parent-child relationship in the code architecture was challenging but ultimately successful.

The UI elements were implemented toward the end, with each control iteratively refined based on testing. Adding the ability to select bodies by clicking required implementing proper coordinate conversion between screen space and simulation space, accounting for zoom level and view offsets.

## Code References

- The elliptical orbit calculations were adapted from NASA's orbital mechanics equations available at [NASA Orbital Mechanics](https://www.grc.nasa.gov/www/k-12/rocket/orbmeca.html)
- The basic p5.js structure was influenced by Daniel Shiffman's Coding Train tutorials, particularly the "Solar System in Processing" tutorial: [Coding Train](https://thecodingtrain.com/)
- The day/night visualization technique was inspired by examples from the p5.js forum: [p5.js Forum](https://discourse.processing.org/)
- The UI slider implementation was based on p5.js examples: [p5.js Examples](https://p5js.org/examples/)
- The logarithmic scaling approach was adapted from techniques in Mike Bostock's D3.js visualization library: [D3.js](https://d3js.org/)

## Next Steps

1. **Texture Mapping**: Replace the solid-color planets with actual texture maps to show surface features.

2. **Asteroid Belt Representation**: Add a procedurally generated asteroid belt between Mars and Jupiter.

3. **Historical Positions**: Allow users to input a date and see the actual configuration of the solar system on that date.

4. **Gravitational Force Visualization**: Add visual representations of gravitational fields and how they affect orbital mechanics.

5. **Spacecraft Trajectories**: Add historical or current spacecraft trajectories to visualize how we navigate between planets.
