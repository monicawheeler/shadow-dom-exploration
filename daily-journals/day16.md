# Day 16

Why should I use it? Does this solve a problem we have or will have?

The [Google guide for Web Components](https://developers.google.com/web/fundamentals/web-components/shadowdom) indicates that CSS is one of the biggest reasons to use the Shadow DOM. The guide says, "Shadow DOM fixes CSS and DOM". But is what it is fixing already solved by writing semantic, DRY CSS? 

Let's look at the points made regarding CSS:

- Using ID's causes issues because it is treated as a global variable

  - Solution: NEVER use ID's to style, please, just don't

- "`!important all the things`"

  - So this is a funny joke to good CSS developers, because we just don't `!important` pretty much anything. You should have enough awareness around what you are coding that `!important` should rarely, if ever, be used. 

- "Style selectors grow out of control"   

  - I know how this can seem true and well, in a large enough project, sure, you can get quite a few selectors. This begs the question, are you really writing DRY code? Have you separated out typography? Have you build based on components? Have you kept a clean BEM or BEM-like methodology? This should NEVER be an issue but I understand how it can happen.

- Performance concerns

  - The article referenced discussed containment and the idea that if you alter the style of something to be positioned left it could possibly cause the entire DOM to be rechecked for that element when it might only apply to a handful of elements. 
  - But this is handled with the `contain` property [discussed here](https://developers.google.com/web/updates/2016/06/css-containment)
  - One more note on this, the Shadow DOM makes the CSS entirely encapsulated to that elements DOM and containment just deals with the parts of the tree that are under consideration when styles are mutated


This Google guide has so much detail and discussion around why to use Shadow DOM. It's worth more exploration. I will revisit tomorrow.


Is it scalable?
Is it well documented?
Who created this? Why?
Who is the leading expert in this area?
Who should I be following?
Poll Slack: I haven't heard much about Shadow DOM, do you know what it is? No cheating (aka, no internet searches)!
