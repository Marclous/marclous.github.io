---
title: "Assignment 3 Forces"
date: 2025-02-12
categories: [The Nature of Code]
tags: [javascript, p5js]     # TAG names should always be lowercase
---
# Magnetic Metal Shards in p5.js
[Link to Project](https://editor.p5js.org/Marc1ous/full/um5YVONkO)
---
## What I Originally Intended to Create

I wanted a simple simulation of objects being attracted to a magnet. Rather than ordinary circles, I imagined fractured shards inspired first by broken glass, but styled as metallic. My goal was for these shards to behave somewhat realistically—sticking to the magnet once they got close enough.

---

## The Process of Creating the Sketch

1. **Basic Magnet & Particles**  
   I began with a barebones p5.js setup: a red circle at the center representing the magnet, and a function to create particles (initially just circles) at the mouse click position.

2. **Inverse-Square Attraction**  
   Next, I added the physics. Each particle experiences an inverse-square attraction (`F ~ 1/d^2`) toward the magnet. Particles far away feel a weaker pull, and those up close feel a strong pull.

3. **Shaping the Shards**  
   To give each particle a fractured look, I generated an irregular polygon by picking a random number of vertices (5–8), distributing them around a circle with slight offsets, and varying their radii. This produced jagged outlines.

4. **Metallic Appearance**  
   I tapped into the native canvas API for a metallic finish. Using `drawingContext`, I created a radial gradient that moves from a bright, reflective center to darker edges. This mimics the look of metal.

5. **Stopping on Contact**  
   Finally, I made each shard “stick” to the magnet instead of flying past. I gave the magnet a physical radius matching its visual size, and each shard has a bounding radius. If the shard collides with the magnet, I clamp its position right at the point of contact and zero out its velocity.

---

## Resources and Influences

- **p5.js Reference**: Essential for vectors, drawing shapes, and mouse events.  
- **Particle System Examples**: Helped me structure the particle class.  
- **MDN (Mozilla Developer Network)**: Guided me on creating radial gradients with raw Canvas calls.

Some older tutorials had confusing or outdated JavaScript conventions, but most community examples and official references were quite helpful.

---

## Problems and Discoveries

- **Extreme Close Distances**: At very close range, the force could explode. Constraining the minimum distance helped avoid runaway acceleration.  
- **Canvas Gradients in p5.js**: It took trial and error to merge p5.js calls with native canvas methods—remembering to `beginPath()` and `closePath()` was crucial.  
- **Collision Clamping**: Getting shards to rest against the magnet required precisely calculating the sum of the magnet’s radius and the shard’s bounding radius.

---

## Conclusion

This project transformed from a simple magnetic pull demo into something visually and physically engaging. Randomizing shapes, adding a metallic style, and implementing collision-based stopping made it feel more lifelike. 

**Next Steps**: Maybe add multiple magnets or even shard-to-shard interactions. For now, I'm satisfied watching these floating shards drift in and snap onto their magnetic center.
