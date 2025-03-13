---
title: "Assignment 5 Particle System"
date: 2025-02-26
categories: [The Nature of Code]
tags: [javascript, p5js]     # TAG names should always be lowercase
---
# Aimlab
[Link to Project](https://editor.p5js.org/Marc1ous/sketches/qWE5LPdfs)
---

## Motivation

I created this game as a simplified “aim training” tool, inspired by **Aimlab** and other reaction-based practice games. The goal is straightforward: circles spawn at random positions on the canvas, and the player must click them quickly before they disappear. Each successful click rewards points and triggers a “shatter” effect—particles bursting from the circle’s center.

## How It Works

1. **Circle Spawning**  
   - Circles appear at adjustable intervals (using a slider).  
   - Random positions keep the user on their toes and help train reflexes.

2. **Circle Lifetime**  
   - Another slider controls how long circles remain on screen. A shorter lifetime forces quicker reactions.

3. **Click Detection & Score**  
   - Clicking a circle increments the score—a good indicator of performance over time.

4. **Shatter Particles**  
   - Each click spawns a burst of particles, providing visual feedback and making the target’s disappearance more satisfying.

## Why This Helps Train Aim

1. **Rapid Target Acquisition**:  
   You have to move the mouse and click on quickly vanishing circles. Over time, this helps build up both speed and precision.

2. **Difficulty Tuning**:  
   By adjusting sliders for **spawn interval** (how often circles appear) and **lifetime** (how long they stay), you can scale the difficulty as you improve.

3. **Feedback Loop**:  
   The score system offers immediate feedback on your performance. You can try to beat your personal best or see how many circles you can click in a given time.

4. **Visual Tracking**:  
   Because circles appear randomly on the canvas, your eyes and mouse hand learn to track and move more efficiently.

## Possible Extensions

- **Varying Circle Sizes**:  
  Smaller or larger circles can further tweak difficulty.  
- **Movement Patterns**:  
  Making circles move before disappearing can mimic more advanced aim training scenarios.  
- **Audio Feedback**:  
  Adding a sound effect on successful clicks can boost the sense of reward and help with reaction timing.

## Conclusion

- Though simple, this clicker game can serve as a fun, lightweight aim-training exercise. The combination of random spawning, timed disappearance, and immediate scoring forms a practice loop similar to commercial aim-training software, but in a much more customizable and lightweight format. Enjoy experimenting with the settings and watch your reflexes improve!
