---
title: "Assignment 4 Oscillation"
date: 2025-02-19
categories: [The Nature of Code]
tags: [javascript, p5js]     # TAG names should always be lowercase
---
# Oscillating Oscillation
[Link to Project](https://editor.p5js.org/Marc1ous/sketches/1zgNzE0es)
---

## What I Intended to Create
I set out to design an animated sketch using p5.js where the Chinese character "摆" is rendered through a series of vibrating lines. The goal was to bring the character to life by applying a dynamic, oscillatory effect to its outline, creating a sense of movement and energy.

---
## The Creation Process
The journey of this project involved several key steps:

1. **Font Selection and Loading**  
   I chose the NotoSansSC font for its excellent support for Chinese characters. I initially experimented with both OTF and TTF formats, ultimately deciding to load the TTF version using `loadFont('NotoSansSC-Regular.ttf')` for better compatibility with the `textToPoints` method.

2. **Extracting Contour Points**  
   Using the `textToPoints` function, I extracted the outline of the character "摆". This function converts the character into a series of points, which serve as the basis for drawing its shape. I adjusted the `sampleFactor` parameter to control the density of these points, ensuring a good balance between detail and performance.

3. **Centering the Character**  
   After extracting the points, I computed the character’s bounding box by determining the minimum and maximum x and y values. With these values, I calculated the offsets needed to center the character on the canvas.

4. **Animating the Vibration**  
   To animate the outline, I applied sine and cosine functions to each point’s coordinates. By incorporating the `frameCount` variable, the offsets change over time, creating a smooth vibrating effect. This step was crucial to achieving the dynamic visual style I was aiming for.

---
## Resources and Examples
In the process of developing this sketch, I found the following resources particularly useful:

- **p5.js Documentation:**  
  The official documentation was invaluable, especially for understanding the functionalities of `loadFont` and `textToPoints`. It provided clear explanations and examples that guided my implementation.

- **Online Tutorials and Examples:**  
  Various tutorials demonstrated creative ways to manipulate and animate shapes using p5.js. The examples that broke down the process of extracting points from text and animating them were especially helpful. However, some tutorials assumed prior knowledge of animation techniques, which was a bit challenging at first.

- **Google Fonts Integration:**  
  Although I used a local TTF file for the font, the process of embedding Google Fonts in the HTML head (using `<link>` tags) influenced the design approach. It highlighted the difference between rendering text in CSS and using font data for creative coding.

---
## Challenges and Discoveries
- **Font File Format Issues:**  
  My initial experiments with OTF files led to compatibility problems with `textToPoints`. Switching to a TTF file resolved these issues, teaching me the importance of matching font file formats to the specific requirements of p5.js.

- **Optimizing Detail vs. Performance:**  
  Adjusting the `sampleFactor` was a balancing act. A higher value produced a more detailed outline but impacted performance, while a lower value resulted in a coarser shape. Finding the optimal setting was key to the success of the sketch.

- **Creative Use of Trigonometric Functions:**  
  Experimenting with sine and cosine for the vibration effect was both challenging and rewarding. Small adjustments to the parameters led to vastly different visual outcomes, deepening my understanding of how mathematical functions can drive creative animation.

---
