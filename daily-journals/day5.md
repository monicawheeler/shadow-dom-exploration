# Day 5 - Create a Web Component! 

TODO's 

- [ ] Create a custom banner web component

- [ ] Review the challenges

## Notes:

- Create a custom element:

```js
customElements.define('custom-banner', CustomBanner);
```

This makes a custom element called `custom-banner` and uses the class `CustomBanner`.

- Create a class for the custom element:

```js
class CustomBanner extends HTMLElement {
  constructor() {
    // Always call super first in constructor
    super();

    // Element functionality written in here

  }
}
```

The class is using ES 2015 syntax.