# Project 1 "Helpers"

<hr>

## I. Project 1 - questions about requirements?

- [Project 1 - Final Requirements](../projects/p1-final.md)

<hr>

## II. Project 1 Helper? - Creating a `likes` counter


- [4 - More Firebase - creating a likes counter for Dog names](https://github.com/tonethar/IGME-330-Master/blob/master/notes/firebase-4.md)
- ***There is a video of the above Firebase demo here --> [Demo - Firebase "Likes" Counter (13:15)](https://rit.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=d89db2ea-9682-4aef-bb54-ae46002bf7ec)***

<hr>

## III. Project 1 Helper? - Creating an "admin" page

- [5 - Firebase - deleting elements from the cloud](https://github.com/tonethar/IGME-330-Master/blob/master/notes/firebase-5.md)
- this is *totally optional* - but a few people have asked how to do it

<hr>

## IV. Project 1 Helper? - "All your web components must take a *parameter*"

- They must have a *parameter* that is passed in via attribute(s), slot(s) and/or as an object property
- Component examples are here: [Web Component Summary](https://github.com/tonethar/IGME-330-Master/blob/master/notes/wc-summary.md)

<hr>

## V. Project 1 Helper? - Suggestion: create a *firebase.js* code module

- Below is a Project 1 code snippet that some of you might find useful
- Because your Firebase code will need to be utilized by both your **app.html** page (for example to WRITE the user’s favorites to the cloud) and your **community.html** page (to READ the "most liked by everyone" favorites from the cloud) - that Firebase code should probably be broken out into a separate JS code module named **firebase.js**
- Then the necessary Firebase functionality can then be imported into **app.js** and **community.js** as needed - here is the code from the *Dog Finder* example:

**firebase.js**

```js
import { initializeApp } from "https://www.gstatic.com/firebasejs/LINK-TO-LATEST-VERSION-FIREBASE.js";
// https://firebase.google.com/docs/web/setup#available-libraries
import { getDatabase, ref, set, push, onValue, increment } from  "https://www.gstatic.com/firebasejs/LINK-TO-LATEST-VERSION-FIREBASE.js";

// Your web app's Firebase configuration
const firebaseConfig = {
  // PUT YER CREDENTIALS HERE
};

const likedDogsPath = "df-liked-dogs/";

const pushLikedDogToCloud = dog => {
  dog.likes = increment(1);
  const db = getDatabase();
  const favRef = ref(db, `${likedDogsPath}${dog.hash}`);
  set(favRef, dog); // `dog` is an object with `.title`, `.url`, `.likes` properties etc
};

// Initialize Firebase
const app = initializeApp(firebaseConfig);
console.log(app);
const db = getDatabase();

export {db,likedDogsPath,ref,set,push,pushLikedDogToCloud,onValue};
```

<hr>

## VI. Project 1 Helper? - Sorting and filtering your results

- Use [`array.sort()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort) and [`array.filter()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
- We did have an `array.sort()` example in IGME-235 - [Web Apps 8 - Arrays](https://github.com/tonethar/IGME-235-Shared/blob/master/tutorial/web-apps-8.md#iv-method-chaining)
- See examples here - [`array.filter()` & `array.sort()` Examples](https://github.com/tonethar/IGME-330-Master/blob/master/notes/array-filter-sort-examples.md)

<hr>

## VII. Project 1 Helper? - Creating a unique ID for your Firebase Favorites

- [Creating unique and repeatable keys by *hashing*](https://github.com/tonethar/IGME-330-Master/blob/master/notes/hash-as-key.md)

<hr>

## VIII. Project 1 Helper? - localStorage "helper code" - localStorage.js

- Check out **local-storage-demo-start** in week 6 of myCourses - it covered reading and writing an object literal to myCourses
- **app.js** and **localStorage.js** are 100% done - there was just a little code in **favorites.js** that you needed to write yourself

<hr>

## IX. Project 1 Helper? - Debugging your code

- [IGME-105 Debugging Slides](https://github.com/tonethar/IGME-330-Master/blob/master/presentations/Debugging.pdf)
- https://developer.chrome.com/docs/devtools/javascript/

<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**Week 7B Notes**](07B.md)     |  [**IGME-330 Schedule**](../schedule.md) | [**Week 8B Notes**](08B.md) 
