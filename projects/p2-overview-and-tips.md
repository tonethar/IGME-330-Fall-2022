# Project 2 - *Interactive Sandbox of Awesomeness* - Overview & Tips

I. [Handy Links](#links)

II. [Executive Summary of Project](#summary)

III. [Thoughts on Project Scope](#checkpoint-feedback)

IV. [AV Tips](#av-tips)

V. [Game Tips](#game-tips)

VI. [Other Resources](#resources)

<a id="links" />

<hr>

## I. Handy Links

- [Project 2 Requirements](p2.md)
- [Project 2 Coding Standards](330-code-style.md)

<hr>

<a id="summary" />

## II. Executive Summary of Project

### II-A. Theme

- "*You will create a compelling interactive media experience that allows the user to explore a media-related theme (of your choice)*" - examples:
  - An audio visualizer - perhaps enhanced by user interaction via Teachable Machine --> https://teachablemachine.withgoogle.com/train
  - A game - *Cage Clicker* could be a good start on one --> https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-cage-clicker-1.md
  - A simulation:
    - Evolution - YouTube [Primer's Evolution Playlist](https://www.youtube.com/watch?v=oDvzbBRiNlA&list=PLKortajF2dPBWMIS6KF4RLtQiG6KQrTdB)
  - A Generative Art, Dynamical Systems or Emergence experience:
    - Here's a great blog post to give you some ideas --> https://www.artnome.com/news/2018/8/8/why-love-generative-art
    - More ideas --> [Intro to Creative Coding](https://github.com/mattdesl/workshop-p5-intro/blob/master/README.md)
    - Chaotic Systems --> see [HW - Lorenz Attractor](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-lorenz-attractor.md)
    - Periodic functions --> see [HW - Sine Wave](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-sine-wave.md)
    - Phyllotaxis --> see [HW - Algorithmic Botany](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-algorithmic-botany.md)
    - Conway's *Game of Life* --> see [HW - Life](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-canvas-life.md)
    - Reaction Diffusion --> RESOURCE: Coding Train [Coding Challenge #13: Reaction Diffusion Algorithm in p5.js](https://www.youtube.com/watch?v=BV9ny785UNc)
 
### II-B. Technologies
 - Must use:
   - JavaScript/ES6 Modules
   - Canvas
   - Bulma
   - Web Components
- Must have:
  - 3 HTML pages
    - about.html
    - app.html
    - documentation.html
  - 3 web components
    - One of these MUST be a global navigation component
  - multiple (at least 3) user interface *controls* and/or widgets so that the user can interact with the experience
  - app data loaded from a JSON file
    - rather than hard-coding values in your JS, data that your app depends on will be stored in a *local* JSON file (ex. **presets.json**, **levels.json** etc)
    - load this local data file via the `fetch()` API
    - see **presets-demo.zip** in myCourses
    - ex. The instructions for your game or experience
    - ex. Game Difficulty Settings (Easy/Normal/Impossible)
    - ex. Audio Visualizer Settings (slider positions, radio button and checkbox state)
    - ex. Conway's Game of Life patterns
 - Must demonstrate:
   - ***IMPACT*** and go beyond what we've done in class
   - The app must do something that would be meaningful to the user, allowing them to explore the chosen theme in a compelling way
   - The code & functionality must go significantly beyond any of the provided "starter" code above
   - The creator of this app should take this assignment seriously ("engage"!) and do their best work

<a id="checkpoint-feedback" />

<hr>

## III. Thoughts on Project Scope

### III-A. Go beyond the "starter" HW assignments

- ***show us what you can DO*** - you will only get project credit for code that ***you wrote***, which means that your projects MUST go well beyond any HW assignments or starter code
- ***don't overscope*** - a simple idea that is complete and well-executed often has more success than an elaborate idea which is only partially implemented

### III-B. Do not violate RIT's Academic Integrity Policy

- ***Cite ANY and ALL*** borrowed code fragments, resources, tutorials, YouTube videos, blogs, GitHub sites etc:
  - be sure to link to the actual page utilized, not just to an entire web site 
  - cite the resource on your project Documentation page AND
  - cite the resource as a code comment, right where you utilized it
  - you DO have to cite any code from any relevant IGME-330 course material - ex. AV HW assignments, Cage Clicker, Conway's Life HW etc...

### III-C. How much time should you spend on this assignment?

- project 2 is where you will demonstrate what you have learned this semester
- typically, weekly out of class work is expected to be 3 or 4 times total in-class hours - which works out to 8.5 to 10 hours a week
- allocating 4 weeks to the project (including the prototype) works out to roughly 30-40 hours of work in total


### III-D. Chrome Favicon Error Messages

- get rid of those annoying console messages by adding a favicon to your site - https://favicon.io/emoji-favicons/


<a id="av-tips" />

<hr>

## IV. AV Tips

### IV-A. Audio Visualizer Examples

- [Audio Visualizer Project Showcase Video (2181)](https://video.rit.edu/Watch/Si56JxGd) - projects are shown starting at 5:00

### IV-B. Creating reusable functions will help a lot

- DRY - multiple parts of your code can call these functions
- you can easily modify function parameters and test your ideas
- your UI can modify these function parameter values
- examples:

```js
function drawBars(ctx,audioData,barHeight=200,fillStyle="white", strokeStyle="black",lineWidth=1,numBars){
  ...
}

function drawLines(ctx,audioData,lineWidth=1,strokeStyle="white",magnitude=100,startIndex=0,endIndex){
  ...
}
```

### IV-C. You should go beyond squares, circles and rectangles

- Come up with different canvas drawing than we did in the HW assignments - ***REMINDER: you will only get credit for code that you wrote*** 
  - the AV HW just used rectangles and circles (arcs) for drawing  - what else could you use?
  - lines with `ctx.moveTo()` and `ctx.lineTo()`
  - curves with `ctx.arcTo()`, `ctx.bezierCurveTo()`, `ctx.quadraticCurveTo()`
  - gradients and images - animated or otherwise
- Resources
  - [Canvas IV - Gradients & Bezier Curves](https://github.com/tonethar/IGME-330-Master/blob/master/notes/canvas-4.md)
 


### IV-D. You should go beyond the "tint red" bitmap effect
- simple tinting and noise could be replaced with different bitmap effects
- emboss could be replaced with a different convolution effect
- we saw some other bitmap effects here:
  - https://github.com/tonethar/IGME-330-Master/blob/master/notes/demo-web-audio-6.md
  - https://people.rit.edu/~acjvks/330/shared/fotoshawp/fotoshawp-done.html


### IV-E. Sprites
 - Sprites - displayed with either canvas primitives or bitmap data - allow for experiences that are distict from the AV HW
   - see the sprite demo in myCourses
   - [Canvas VI - Canvas Sprites](https://github.com/tonethar/IGME-330-Master/blob/master/notes/canvas-6.md)
   - [Mario Sprite Sheet Example](https://github.com/tonethar/IGME-330-Master/blob/master/notes/_files/sprite-sheet-demo-mario.zip)

### IV-F. Canvas Blending Modes
- [Canvas V - Drawing images & Blending Modes](https://github.com/tonethar/IGME-330-Master/blob/master/notes/canvas-5.md)


### IV-G. Transformations
- Animated rotations and scaling can often be a nice effect:
  - [Canvas III - Transformations](https://github.com/tonethar/IGME-330-Master/blob/master/notes/canvas-3.md)  - look at the animated rotating bezier curves in **screen-saver-2.html**

### IV-H. Alternative Inputs
- For highest "Impact", you must use *customized* audio control buttons (Play/Pause/Volume) like we did in the AV HW, and add Bulma styles to them:
  - don't use the built in `<audio>` element for controls
- Web Cam
  - https://github.com/tonethar/IGME-330-Master/blob/master/notes/demo-web-audio-6.md
- Teachable Machine (web cam and/or microphone)
  - https://teachablemachine.withgoogle.com/
- ml5
  - [1 - Machine Learning with ml5 - Image Classification](https://github.com/tonethar/IGME-330-Master/blob/master/notes/1-ml-pre-trained-models.md)
  - [2 - Machine Learning with ml5 - Object Detection](https://github.com/tonethar/IGME-330-Master/blob/master/notes/2-ml-object-detection.md)
  - [3 - Machine Learning with ml5 - Pose Detection](https://github.com/tonethar/IGME-330-Master/blob/master/notes/3-ml-posenet.md)

### IV-I. Lastly, ***What else can help us create an effective audio visualization?***

1. There should be an analogous relationship between the sound data and what users are seeing on the screen - drawing should not be random like our "screen savers" HW assigments were. Can you instead help your viewer **learn** about sound & music by making new connections, and seeing new patterns, such as:
    - visualizing the "beat"
    - human voices fall into the lower frequencies
    - electronic instruments have a different "shape" than natural instruments

2. Have a good "starting state" to your visualization - the controls should be pre-set to where the visualization has a pleasing state when the user first opens it

3. Don't bore the user - have the visualization periodically change in major ways, automatically. 

<!-- Here's an example: http://igm.rit.edu/~acjvks/courses/2015-fall/330/demos/p1-demo/web-audio-example.html -->

4. Give the user controls (sliders, check boxes, pull downs) to effect the visualization. The relationship between what the controls do and what happens on the screen should be obvious

5. Other Tips:
    - Certain drawing could go beyond the raw data for the various bins (frequency ranges), it could instead be aggregate data such as average loudness of all frequencies, or changes in the average of certain frequencies, or tied to beat detection.
    - You can use `ctx.scale()` to squash or stretch shapes - to create ovals for example
    - Effects could implemented on a second canvas like we did in the "Paint" Demo (see mycourses week 13 for files)
    - Not everything has to be drawn at 60 frames/second - use `setTimeout()` or similar to achieve this 
   
6. Get inspired!

    - The power of the canvas is that you can draw *anything* on it!
    - Try googling "audio visualizations" or "data visualizations" and get some ideas!


<a id="game-tips" />

<hr>

## V. Game Tips

### V-A. What *elements* are shared by good games?
- We like this definition of a game:
  - *"A game is a series of interesting choices"* - https://en.wikiquote.org/wiki/Sid_Meier - and you should strive to give your players some - examples:
    - *"When should I use one of my limited supply of  smart bombs to clear the screen?"*
    - *"Do I try to grab the powerup, or avoid that projectile?"*
    - *"Should I build a farm, or wait to save up enough to build a factory?"*
  - Other elements found in fun games you will probably have in yours:
    - A difficulty level that's not too hard, nor too easy
    - Score
    - Levels
    - Satisfying user control with mouse and/or keyboard (see 235 "Key Daemon" aka [Smooth Keyboard Control](https://github.com/tonethar/IGME-235-Shared/blob/master/tutorial/pixi-js-0.md#vi-demos) demo)
    - Sound - both background & incidental - you might not need to use WebAudio - don't forget about [Howler.js](https://howlerjs.com/) - we used that in Cage Clicker (IGME-330) and Circle Blast (IGME-235)
    - *Feedback loops* that change the flow of the gameplay - https://learn.canvas.net/courses/3/pages/level-4-dot-4-feedback-loops
      - example from multi-player games - a canonical "rubber band"
        - [YouTube - The Blue Shell - Why Mario Kart's Most Hated Item Exists - Design Club](https://www.youtube.com/watch?v=LFfga8-3SZI)
    - *Emergent gameplay/complexity* (i.e. the players *learning* something that can improve their level success in the game) - https://learn.canvas.net/courses/3/pages/level-4-dot-5-emergence
  - Clear controls & rules
    - Instruction Screens
    - Hints
    - Teach the game though good level design? 
      - [YouTube - Design Club - Super Mario Bros: Level 1-1 - How Super Mario Mastered Level Design](https://www.youtube.com/watch?v=ZH2wGpEZVgE)

<a id="resources" />

<hr>

## VI. Other Resources

- myCourses Content area 



