---
title: "Final Prject"
date: 2025-04-15
categories: [The Nature of Code]
tags: [javascript, p5js]     # TAG names should always be lowercase
---
### Final Project Proposal: **"Persnality in Motion"**

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

#### **Description**
"This is an interactive ecosystem where flies with distinct personalities create emergent patterns as they respond to each other and user interaction."

---

#### **Context**
This project is designed as an interactive art piece that blends entertainment with subtle behavioral study. Users will experience it through direct mouse interaction, observing how different personality types respond to their presence. The simulation is meant to be both visually engaging and thought-provoking, inviting viewers to consider how simple rules and traits can create complex systems.

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
1. Refine the existing personality types to make their behaviors more distinct
2. Experiment with visual representations (trails, shapes, sizes) that better communicate personality
3. Implement fly-to-fly interactions based on personality types
4. Add environmental elements that flies can interact with
5. Develop a more sophisticated mouse interaction system
6. Test performance with larger numbers of flies

#### **Updates**
1. Window Resizing: The canvas now resizes with the browser window.
2. Food Source: Clicking creates a temporary red circle (foodSource) that attracts flies based on their attractionForce personality trait. It disappears after a few seconds.
3. Mouse Interaction: Flies now react to the mouse only when there's no food source. Nervous and aggressive flies flee, while others might be slightly attracted or indifferent (this part is simplified but shows the concept).
4. Personality Refinements:
5. - Adjusted maxSpeed, turnChance, jumpChance for more distinct movement.
   - Added size property, making flies visually different.
   - Added repulsionForce affecting how strongly they push away from others.
   - Added attractionForce affecting how strongly they are drawn to food.
6. Fly-to-Fly Interaction (separate method): Flies now actively avoid getting too close to each other using a steering behavior. The strength of this avoidance is influenced by repulsionForce.
7. Environmental Zone (safeZone): A green rectangle is drawn. The checkSafeZone method detects if a fly is inside, and the update logic makes flies slow down and jump less frequently while within it.
8. Steering Behaviors: Introduced applyForce, seek, separate, and wander methods for clearer behavior management, based on common steering algorithms.
9. Code Structure: Cleaned up the update method to calculate forces separately and then apply them. Passed the allFlies array to update and separate for interaction checks.
Edges: Modified edges to wrap slightly off-screen based on size for smoother transitions.
10. Visuals: Added transparency to fly colors and used a lighter background. Added rounded corners to the safe zone.

I plan to iterate on this concept by gradually adding complexity while maintaining performance and visual clarity. The goal is to create a system that feels alive and responsive, where users can observe how different personality types create unique patterns of movement and interaction.