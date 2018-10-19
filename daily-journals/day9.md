# Day 9 - Connect all the pieces to the Shadow DOM and play with variations

[This is the CodePen I have been working in](https://codepen.io/frogmcw/pen/EdNOKm)

- Added in some base styles and appended the style element to the Shadow DOM

- Add conditional to determine what type of banner it is:

  - Success: checkmark icon

  - Warning: triangle alert icon

  - Neutral: comment bubble icon

## Notes:
So far, the ability to encapsulate a component is really great. I can still use BEM for styling and I have the flexbility to update the CSS as I need to. Also, the ability to keep this whole component separate from any other Shadow DOM or regular DOM components is really cool to demo. This custom banner has a `container` class and then I modify it for state changes.