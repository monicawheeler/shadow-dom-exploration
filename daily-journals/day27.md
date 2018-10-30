# Day 27 

As we approach the last day of this challenge, I wanted to make some notes as to my progress and my understanding of this topic:

- The Shadow DOM is a separate DOM tree that is nested within a regular DOM element (either a custom element or a regular element)

- The Shadow DOM is beneficial because it provides isolation to HTML, CSS, and JS within that DOM tree. 

- The awesome part of this is it provides protection from this components styles and functionality from leaking into others.

- This isolation can also be problematic in terms of well written and DRY CSS. I can see this becoming a point of laziness: "It doesn't need to have BEM or a structure in it's classes, let's just style the elements directly. What could it hurt?!"
