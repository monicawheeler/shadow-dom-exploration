# Day 7 - Continue creating the banner custom element

TODO's 

- [ ] Let's add a Shadow DOM to the custom element

- [ ] Review the inital notes and evaluate where I am after a week.

## Notes:

I put together a living CodePen that will be used to demo this custom element and explore the use of the Shadow DOM:
(Custom Element)[https://codepen.io/frogmcw/pen/EdNOKm]

### What do I need the banner to do and to have? 

- The banner needs to have a content area with text only, an icon to the left that gives a visual of if this banner is a warning or something positive, a banner type for (positive, warning, success), and a close button. 

  - Icon

  - Text

  - Banner type: positive (indicates a blue color), warning (indicates a red color), success (indicates a green color) 

  - Close button

So, for today I will add a shadow root and some custom inner elements. 

```js
// Create the shadow root
const shadow = this.attachShadow({mode: 'open'});

// Create custom elements
const wrapper = document.createElement('div');
wrapper.setAttribute('class', 'custom-banner');
const contentIcon = document.createElement('span');
contentIcon = setAttribute('class', 'custom-banner__icon');
const contentArea = document.createElement('p');
contentArea.setAttribute('class', 'custom-banner__content');
const closeIcon = document.createElement('span');
closeIcon.setAttribute('class', 'custom-banner__close');

// Take attribute content from `data-contentArea` and populate the content area

const dataContentArea = this.getAttribute('data-contentArea');
contentArea.textContent = dataContentArea;
```

We have to attach the custom elements to the Shadow DOM!

```js

shadow.appendChild(wrapper);
wrapper.appendChild(contentIcon);
wrapper.appendChild(contentArea);
wrapper.appendChild(closeIcon);
```

So we can see the awesome work above, register the custom element using the `define()` method:

```js
customElements.define('custom-banner', CustomBanner);
```

The Shadow DOM is not being created, for tomorrow's work:
`https://codepen.io/frogmcw/pen/EdNOKm`