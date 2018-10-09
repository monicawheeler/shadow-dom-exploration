# Day 8 - Troubleshoot the Shadow DOM issue

- I dug around and found a console error. Turns out:

```js
// Console log error:
setAttribute is not defined
```

Troubleshooting this today and I was assigning a variable to a `setAttribute` method instad of chaining the variable with a `setAttribute` method

```js
// This is why I was getting the error: This is Wrong
contentArea = setAttribute('class', 'class-name');

// Fixed it, needs to chain not assign
contentArea.setAttribute('class', 'class-name');
```

### Some thoughts

- How do we make the shadow DOM elements/content accessible? Are they by default like regular DOM elements? 

- This seems like a load of work (albeit, not complicated) to put together, why bother? 