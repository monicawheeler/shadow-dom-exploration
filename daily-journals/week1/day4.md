# Day 4 - Exploring Web Components

*TODO's Today* 

In reviewing the use of the Shadow DOM I found that it was part of a larger picture and that is Web Components. 

MDN covers this simply, as they usually do, in their document [Web Components](https://developer.mozilla.org/en-US/docs/Web/Web_Components).

So today's TODO's:

- [X] Read and review the Web Components document to see how the Shadow DOM fits in
  - [X] Make notes!

### Notes:

What's the point, encapsulation! Reusable custom elements! Web Components consists of three main technologies:

- Custom Elements

- Shadow DOM

- HTML templates

The basic approach for implementing web components look like this:

1. Create a class (or function) to specify your web component functionality. See ES 2015 class syntax for your class.

2. Register your new custom element using the `CustomElementRegistry.define()` method.

3. If required, attach a Shadow DOM using the `Element.attachShadow()` method.

4. If required, define an HTML template. 

5. Use your custom element where ever you'd like on your page, just like a regular HTML element.

The following questions will get addressed over time.

## Unanswered questions from the previous day:

- [ ] Why set the mode to `open` verses `closed`, or more specifically what are the ramifications? 

- [ ] How does the hidden DOM trees get removed? 