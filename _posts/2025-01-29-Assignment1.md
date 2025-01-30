---
title: Assignment 1 Randomness
date: 2025-01-29
categories: [The Nature of Code, Assignment 1]
tags: [javascript, p5js]     # TAG names should always be lowercase
description: [Link to Project](https://editor.p5js.org/Marc1ous/sketches/dyjvTtS7J)
---

## Initial Thought

I started experimenting with simulating something in nature. In the beginning, I tried to simulate the random trail of a fly flying. After making one, it is easy to create a bunch of flies flying around. However, the randomness only shows from the random flying trail without any order. Giving them traits. I wanted to simulate "nervous," "chill," "aggressive," and "playful" flies, each with different movement patterns, and explore how personality traits could lead to emergent behaviors in a simple system.

## Creation Process

I started by implementing a basic random walker but quickly moved to a vector-based movement system using p5.Vector for smoother, more organic motion. I created a Fly class where each instance had different personality traits affecting its speed, direction changes, and jumping behavior.

To refine the motion, I experimented with different probability values for turning and jumping, adjusting them to balance realism and variety. I also added color-coding for each fly type to make their behaviors visually distinct. Finally, I ensured they could wrap around the canvas instead of getting stuck at the edges.

## Resources
- Daniel Shiffman’s “Nature of Code” examples on randomness, Perlin noise, and autonomous agents.
- Previous random walker exercises, which helped me understand movement randomness.
- Real-world animal behaviors, particularly insects like fruit flies and bees, to model erratic or smooth motion.
- ChatGPT-o1 for debugging problems.

## Problems
- Too much randomness felt unnatural – Early on, my flies moved too chaotically, which made them seem unrealistic. Adding probability-based movement constraints helped differentiate personalities.
- Tuning probabilities was tricky – Finding the right balance for how often a fly should change direction or make a big jump took trial and error.

## Future Improvements

I’d like to explore fly interactions, introduce environmental elements like food sources, and experiment with mood changes based on surroundings. Even introduce some more organimsm to the ecosystem. 

## Screeshot
![Screenshot for project](/img/Assignment1.png)

