# DAY 12

```js
<div id="test"></div>

<script>
  document.getElementById("test").addEventListener("click", function( event ) {
    // display the current click count inside the clicked div
    event.target.textContent = "click count: " + event.detail;
  }, false);
</script>
```
