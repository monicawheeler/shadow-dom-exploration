# Day 10 - Troubleshooting component placement and add click event

## Component placement is causing issues with the regular DOM - troubleshoot

## Add click event

### Notes

Discovered that I had to wrap the custom element in a `div` element to prevent the component from "sucking up" all of the components that followed it. Tested one of MDN's components and that same issue occurred. 

- Going to test if it needs CSS to prevent this issue

  - Adding CSS to the custom-banner element in the CSS directly does not resolve this issue

- Test if making the custom element built with existing elements, rather than Autonomous, will prevent this issue.

  - Let's try extending a `div` 

    - Well, that just breaks things in the custom-banner

    - Did some research and found a blog article that indicates the custom elements cannot be self-closing and that is how I wrote it in the CodePen. 
    
      - I closed the element and that did it. [article mentioned above](https://auth0.com/blog/web-components-how-to-craft-your-own-custom-components/)

*Important* 

Close your elements. They cannot be self-closing!

### Tomorrow, click events!
