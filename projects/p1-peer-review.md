# In-class P1 Peer Review

- [Project 1 - Checkpoint #1](p1-checkpoint-1.md)
- [Project 1 - Checkpoint #2](p1-checkpoint-2.md)
- [Project 1 - Final Requirements](p1-final.md)

## Instructions

- See the ***REVIEW TEMPLATE*** at the bottom of the page

## Peer review questions
- The questions below do not cover every last requirment, but hit most of the major ones

### I. All Pages
- Is there a "global" navbar on the same place on each page, and does it have embedded "you are here" cues (current page text is bolded, or similar)?
- Does the Hamburger menu still work?
- Is there a custom "brand" icon present (or is the app still using the font awesome dog icon)?
- Does each page have appropriate `<title>` tag content (or is the app still using content from the Dogfinder app)?
- Does the app still look like Dogfinder app (same colors etc) - or is it distinctive in some way?
- Naming conventions followed for file and folder names and HTML element class/id names?
- [Code style guide](330-code-style.md) followed?

### II. Home Page
- App's name or title?
- 2 or 3 sentence description of the project?
- Theme related image?

### III. App Page
- Required Controls?
- Custom "card" web component with "Favorites" button?
- UI State preservation (controls, required)?
- UI State preservation (results, optional)?
- uses `fetch()` instead of `XHR`?
- uses either Mapbox or Firebase?
- easy to use, with well-labeled and obvious controls?
- "lets the user know what's going on"?
  - example: activity indicator "spinner" on button?
  - example: "5 results found"
  - example: if a search result on a card is favorited, then the "Favorite Me!" button should change state to indicate that particular result cannot be favorited again
- "fails gracefully" and errors communicated to the user?
  - example: "No results found" message if a search comes back with no results
  - example: "Please enter a search term" if the user clicks the search button without typing anything in

### IV. Favorites Page
- [Favorites Page Requirements](p1-checkpoint-2.md#iv-functional-requirements---favorites-page) met?
  - Optional features to be added?

### V. Documentation Page
- [Required Content Present?](p1-checkpoint-2.md#v-content-requirements---aboutdocumentation-page)

### VI. Web Components
- Are there 4 components - "result-card", "app-navbar" and 2 others?
- Is the `<result-card>` following the `<sw-card>` example from **wc-3**, or the **Dogfinder-3** card example that uses Bulma card styles (which looks much better, and shows how to pass in callback code to the "Favorite" button)?

### VII. Impact

- it serves a purpose - is useful to *someone*?
- easy to use, functional, and aesthetically pleasing?
- approaching "portfolio quality" - something you would be able to show a potential employer?

### VIII. "Above and Beyond"
- Is there any current or planned "above and beyond"?


### VIII. Overall comments or suggestions from reviewer

### IX. Technical or other issues?
- List any technical or other issues that the project creator has encountered?


<hr>

- **Each Reviewer will copy/paste what's below into a Word doc**
- **Name this Word doc *<projectcreatorlastname-firstinitial>-p1-review***
  - Example: ***Johnston-J-p1-review.docx***
- **Fill out the document, then post it to the appropriate myCourses dropbox**

<hr> 
  
***REVIEW TEMPLATE***

```
Reviewer Name:
Info on Reviewed Project:
- App Title:
- Banjo Link:
- Creator of project:

Instructions
```


