# Project 1 - HTML5 App of Awesomeness
## Checkpoint #1 - Proposal & Mockup

<hr><hr>

## Project 1 Links:

- **Project 1 - Checkpoint #1**
- [Project 1 - Checkpoint #2](p1-checkpoint-2.md)
- [Project 1 - Final Deliverable](p1-final.md)
- [Project 1 - Tips & Tricks](p1-tips.md)
- [IGME-330 - Course Code Style Requirements](330-code-style.md) 

<hr><hr>

## I. Introduction

- For this project you are creating a JavaScript driven Web application that utilizes one or more Web services and/or data sources
- There is a list of possible data sources here - [Project 1 - Data Sources](p1-data-sources.md)


### I-A. Overview of final version
- Your goal is to create an application that does something useful, and is easy to use, functional, and aesthetically pleasing
- The app should serve a purpose - i.e it should be useful to *someone*
- It should be (or approaching) "portfolio quality" - something you would be able to show a potential employer
- Let's call the 3 lines above "Impact" - which is what your app should have
- Ideally the experience will run in all modern browsers, but at a bare minimum it must run in recent versions of Chrome.
- The objective of this project is for you to demonstrate your mastery of HTML5/CSS/JS "rich media" programming in a web browser context
- You will be evaluated on:
  - the quality of the experience you create
  - the soundness of your programming
  - meeting the requirements detailed below
  - how far you went beyond what we did in class, as described below

### I-B. Timeline

- Checkpoint #1 - due Wednesday night 9/28/22
- Checkpoint #2 - due Monday XX/XX/22
- Final version - due Wednesday XX/XX/22

### I-C. FAQ
- *Can I use the same API that I did for the IGME-235 Web App project?*
  - Yes, but you need to refine and improve what you did on the previous project

<hr>

## II. Requirements & Deliverables for this checkpoint

- 4 web pages: **home.html**, **app.html**, **favorites.html**, **documentation.html**
- All web pages:
  - Must utilize the Bulma CSS framework - either something you came up with on your own, or the page that you created for HW-Bulma-1:
    - do NOT use (for example) any of our demos (SW App, Greeter with Components, etc) as a starting point
  - Must have a global navigation system - this is a navigation system that appears on every page - and it contains a "cue" to which page the user is currently on (example - bolded text, or a different colored background)
  - Must contain at least 2 web components
  - Must have a descriptive `<title>`
  - Must follow course naming conventions for `id`, `class` and `name` attributes, and for file and folder names
- Page Requirements:
  - **home.html** - this is the app landing page - eventually this page will need to be visually interesting and effectively communicate what the app does to your target audience.
    - For now, it must state the app's name or title, and a 2 or 3 sentence description of the project. It also must have a theme related image on it (a "brand" or font awesome icon does not meet this requirement)
  - **app.html** - no specific content is required, but some placeholder text or UI would be nice
  - **favorites.html** - no specific content is required, but some placeholder text or UI would be nice
  - **documentation.html** - this is where you will describe:
    - the API or data source your app uses - and give us a link to the documentaton for that API
    - the major features of the app
    - an image that represents your planned interface for **app.html** and the controls that it will have. It is OK if this image is low-fidelity - you could  sketch on paper and take a picture, or use a prototyping tool like Axure, or other similar methods
    -  If you plan on building a similar (but significantly improved) version of your IGME-235 web app project, you must also provide a link to that project
- Site Structure:
  - the above site will be contained in a **330/project-1** folder on banjo and must have the following sub-directories (even if they are currently empty)
  - **src/** for JavaScript files
  - **styles/** for CSS files
  - **images/** for image files
  - **data/**  for app data files
- Code requirements:
  - make sure that the hamburger menu is functional on all 4 pages
  - you will also need to import the JS files for your 2 web components
  - the above code and imports must be contained in a JavaScript ES6 module file
  - you could name this file **init.js** or **loader.js** or **preloader.js** etc

<hr>

## III. Code quality (applies to this and future checkpoints)
- [IGME-330 - Course Code Style Requirements](330-code-style.md)

<hr>


## IV. Required Technologies (in future/final deliverables)

- Valid HTML5 (must pass validation without errors or warnings)
- Valid CSS (must pass validation without errors or warnings)
- Bulma CSS framework (site must be responsive & mobile friendly)
- JavaScript ES6 modules
- Web Components (at least 4 distinct ones used on project)
- Ajax (utilizing the `fetch()` API)
- `.localStorage` for storing app favorites and UI state
- At least ONE of the following:
  - Firebase (probably for populating a "Community Page")
  - MapBox (to display locations of significance)


<hr>

## V. Evaluation / Rubric

- Grade weight is 10% of project 1 (which is 25% of your final course grade)
- Late submissions will not be accepted without prior approval
- Rubric (out of 10 points):
  - (-5) points for each missing web component, not using Bulma, missing HTML files
  - (-5) no interface sketch/mockup present on **documentation.html** page
  - (-2) if the hamburger menu and/or navigation system do not function properly
  - (-1) point for each instance of not following code & naming standards detailed in [IGME-330 - Course Code Style Requirements](330-code-style.md)
  - (-1) point for each other unmet requirement
- This checkpoint is designed to get you started - which is usually the hardest thing to do whenever one is faced with a task
- Once you have come up with your idea - this checkpoint shouldn't take too long to complete - so get 'er done! And be sure to meet ALL of the requirements
- See myCourses dropbox for submission instructions
