# Day 20

Today I am starting a series on Pluralsight called "Vanilla Web Components Practical Guide". The remaining portion of this month will be spent noting what I've learned in this course.

## Notes:

- What is a "vanilla" web components. 

  - Polymer, SkateJS, and x-tag are libraries that create web components for you and often add additional features.

  - Vanilla, means using the web components specs, just vanilla JS

- Haven't we been building web components for a long time now? 

  - We have, in various ways but not fully encapsulated

  - React, for example uses class based components

- Style encapsulation via the Shadow DOM

- Fewer dependencies

- Framework/library agnostic

- Longer life components

### Web Components brings together these 4 Standards

- Custom Elements

- Shadow DOM

- HTML Templates

- HTML Imports

### Native DOM elements

- Created a demo based on the pluralsight instruction: https://codepen.io/frogmcw/pen/KGBrzB

- Cool thing I learned, is that you can trigger the creation of the custom element via JS (timeout or any other event)
  
- You can also trigger actions like, tracking attribute changes (`attributeChangedCallback()`) and also when the element is removed from the DOM (`disconnectedCallback`)