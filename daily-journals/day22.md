# Day 22

In the short video I watched today, I learned that I can use the `is` attribute in the HTML element to make the custom element attach to normal DOM element. For example: 

```
  <a is="custom-anchor" href="https://www.google.com">Search at Google</a>
```

We then added a conditional that allows us to prevent the user from leaving the page before acknowledging the confirmation message. 

```
class CustomAnchor extends HTMLAnchorElement {
  connectedCallback () {
    this.addEventListener("click", e => {
      e.preventDefault();
      const result = confirm("Are you sure you want to navigate from this page?");
      if (result) {
        window.location.href=e.target.href;
      }
    });
  }
}

window.customElements.define('custom-anchor', CustomAnchor, { extends: "a"});
```

Really cool. 

- The above created a `connectedCallback` that only is invoked when the custom element is appended to a document-connected element.

- Then we added a click event that prevents the default click behavior (opening the link), creates a confirm dialog, then says if the confirm dialog returns true, to navigate to the href value. 