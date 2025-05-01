---
title: "Final Prject"
date: 2025-04-15
categories: [The Nature of Code]
tags: [javascript, p5js]     # TAG names should always be lowercase
---
### Final Project Proposal: **"Personality in Motion"**

---

**[Link to Sketch](https://editor.p5js.org/Marc1ous/sketches/dyjvTtS7J)**

#### **Description**
"This is an interactive ecosystem where flies with distinct personalities create emergent patterns as they respond to each other, predator, and user interaction."

---
#### **Inspirations**
My inspiration for this project comes from a previous work I developed that explored simulated behaviors. I was fascinated by how simple rules could create complex, lifelike movements and wanted to expand on this concept by adding personality traits to virtual entities. The current fly simulation serves as a foundation that I'm excited to build upon and refine.

---

#### **Source Material**
1. **Visuals**:
   - The existing code base with flies of different personalities
   - Reference images of insect movement patterns
   - Color palettes that effectively communicate different personality types

2. **Code**:
   - My base simulation code [Link to Project](https://editor.p5js.org/Marc1ous/sketches/dyjvTtS7J)
   - Additional sketches exploring particle systems and emergent behavior
   - References for implementing more complex interaction patterns

---

#### **Context**
This project simulates a small ecosystem populated by virtual "flies," each assigned one of four distinct personalities: nervous, chill, aggressive, or playful. These personalities dictate fundamental behavioral parameters such as maximum speed, turning frequency, tendency to make sudden jumps, interaction radius, and visual size. The simulation utilizes p5.js vectors for position, velocity, and acceleration to create realistic physics-based movement.

The flies exhibit several layers of behavior. They wander randomly based on their personality's turning chance but also react dynamically to their environment and each other. Flies maintain personal space through a separation steering behavior, pushing away from nearby flies with a force influenced by their personality (e.g., aggressive flies push harder). User interaction is incorporated through mouse movement, causing flies to either flee (nervous, aggressive) or potentially investigate, depending on their nature. Furthermore, clicking the mouse creates a temporary "food source" that attracts flies based on their personality-driven attraction force, overriding the mouse interaction temporarily.

A key feature is the "safe zone," a designated rectangular area where flies are protected from the simulation's predator. Inside this zone, flies exhibit calmer behavior (slowing down, jumping less) and have the opportunity to reproduce. Reproduction occurs based on a set probability (reproductionRate) for flies within the zone, provided a cooldown period has passed and the total fly population hasn't exceeded a defined maximum (maxFlies). Offspring inherit the parent's personality.

Adding conflict and population control, a predator navigates the space outside the safe zone. It actively seeks the nearest fly, ignoring those within the safe zone, and pursues it. If the predator catches a fly, the fly is removed from the simulation. The predator itself is programmed to actively avoid entering the safe zone using a steering behavior that pushes it away from the zone's boundaries. The simulation uses a semi-transparent background to create visual trails, illustrating the flies' recent paths and enhancing the sense of motion. The flies themselves are rendered using simple geometric shapes (body, head, wings) oriented according to their velocity vector, giving them a more distinct visual identity than simple points.

---

#### **Questions and Concerns**
1. Which personality types are most visually distinct and interesting to watch?
2. What additional interactive elements would make this more engaging?
3. Should I focus more on the visual aesthetics or the behavioral complexity?
4. Would adding environmental factors (like food sources or obstacles) enhance the experience?
5. Is the current level of interactivity sufficient, or should users have more control?

---

#### **Uncertainties**

**Conceptual:**
- How can I make the personality differences more meaningful and noticeable?
- Should I incorporate a narrative element or keep it purely abstract?

**Technical:**
- How can I optimize the code to handle more flies without performance issues?
- What's the best way to implement more complex interactions between flies with different personalities?
- Should I add visual elements beyond the basic circles to better represent the flies?

---

#### **Next Steps**
1. If more time were available, potential next steps could include:

2. More Complex Interactions: Implement fly-to-fly interactions based on personality (e.g., aggressive flies chasing others, playful flies grouping up).

3. Predator Enhancements: Give the predator more sophisticated hunting strategies or introduce multiple predators. Maybe predators could also reproduce or have limited lifespans/energy.

4. Environmental Complexity: Add more environmental features, like obstacles, areas with different physics (e.g., "sticky" zones), or varying food source types/permanence.

5. Fly Evolution/Adaptation: Introduce a simple genetic algorithm where personality traits could change slightly upon reproduction, potentially leading to population shifts over time based on survival success.

6. Visual Refinements: Improve the visual representation of flies and the predator further, perhaps adding subtle animations (like wing beats). Add more visual feedback for fly states (e.g., highlighting a fly being targeted).

7. Sound: Incorporate subtle sound effects using Tone.js for fly movement, predator presence, or interactions.

8. UI Controls: Add sliders or buttons to allow the user to adjust parameters like reproductionRate, maxFlies, predator speed, or the number of initial flies in real-time.
