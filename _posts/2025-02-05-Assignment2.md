---
title: "Assignment 2 Vectors"
date: 2025-02-05
categories: [The Nature of Code]
tags: [javascript, p5js]     # TAG names should always be lowercase
---

[Link to Project](https://editor.p5js.org/Marc1ous/sketches/dyjvTtS7J)

## Dynamic Acceleration 

I started by thinking of some of the ways that could interact with the ecosystem and give it dynamic acceleration

A dynamic acceleration system changes over time based on multiple factors, such as:

- Proximity to other flies (avoidance or attraction)
- Time-based oscillation (e.g., sine waves for smoother acceleration)
- External influences (mouse interaction, wind force, etc.)
- Personality-driven behavior shifts (flies adapting to surroundings)

I chose to make the mouse interaction with the movement of flies. 

Effect:
If the mouse gets too close, flies move away dynamically.
Otherwise, they wander randomly as before.

```javascript
{
    let mouse = createVector(mouseX, mouseY);
    let dir = p5.Vector.sub(mouse, this.pos); // Direction to mouse
    let distance = dir.mag();
  
    if (distance < 100) 
    {  
        // If close to the mouse, react
        dir.setMag(map(distance, 0, 100, this.maxSpeed, 0)); // Stronger acceleration if closer
        this.acc = dir;
    } 
    else 
    {
        if (random(1) < this.turnChance) 
        {
            const angle = random(TWO_PI);
            this.acc = p5.Vector.fromAngle(angle).mult(0.5);
        }
    }
}
```