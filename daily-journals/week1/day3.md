# Day 3 - Definitions and reviewing those definitions

*TODO's Today* 

[X] - Review and reread MDN article to make sure the notes from yesterday make sense
  - https://developer.mozilla.org/en-US/docs/Web/Web_Components/Using_shadow_DOM

Notes:

- Terminology 

  - Shadow host

  - Shadow root

  - Shadow tree

  - Shadow boundary 


- The *Shadow host* is the regular DOM node that "hosts" the shadow tree

- The *Shadow root* is the root node of the shadow tree

- The *Shadow tree* is the DOM tree _inside_ of the shadow host

- The *Shadow boundary* is where the Shadow DOM ends and the regular DOM begins

So in summary, the Shadow DOM consists of a host (regular DOM node that hosts the shadow tree), a shadow root (the start of the shadow tree, or root of the shadow tree), and from that root the shadow tree is created. The shadow tree is the DOM tree within the shadow host. The shadow boundary is the container (or where the shadow DOM ends) of this whole thing.

MDN has a pop-up info widget example that demostrates how you can create a Shadow DOM off of an element, in this case it's a label with a nested custom element called `<popup-info>`. 

This spawned a side review of how custom elements are created. I spun up a quick example on CodePen. I did not style within the component, but you would want to. This leaves any outside styles separate and _untouched_. Something I found is that the element is inline by default unless defined in the contructor. [CodePen here](https://codepen.io/frogmcw/pen/yReRoM)


Questions from Day 2 reading:

- [X] How does the hidden DOM trees get added?

  - You can attach a shadow root to any element using the `Element.attachShadow()` method

    - This takes an options object as its parameter with one option, `mode` with a value of `open` or `closed`

    - It is less complicated to simply set the mode to `open`

- [ ] How does the hidden DOM trees get removed? 

- [X] What is the shadow boundary and shadow root?

  - The shadow boundary is where the Shadow DOM ends and the regular DOM begins

  - The shadow root is the root node of the shadow tree


Questions:

- [X] How do you manipulate the element after it's attached? 

  - You would use the same DOM APIs as you do for regular DOM manipulation

- [ ] Why set the mode to `open` verses `closed`, or more specifically what are the ramifications? 

- [ ] What is the support for Shadow DOM?

