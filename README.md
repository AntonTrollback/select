## SUIT CSS component: select
> A component providing a solid base for redesigning the native select element

Read more about [SUIT CSS's design principles](https://github.com/suitcss/suit/).

## Installation

npm install suitcss-select

## Available selectors
- `.Select` – [core] The core button component, used as a wrapper
- `.is-disabled` – [state] For disabled-state styles (also include the `disabled` attribute on the `select` element)
- `.Select-control[:hover|:focus|:active]` – [descendant] The `select` element
- `.Select-figure` – [descendant] The custom "arrow"
- `.Select-control[:hover|:focus|:active] + .Select-figure` – Be creative

## Example

```html
<div class="Select Select--myModifier">
  <select class="Select-control">
    <option>Option 1</option>
    <option>Option 2</option>
  </select>
  <svg class="Select-figure" viewBox="0 0 2 1.5">
    <polygon points="0,0 2,0 1,1.5" fill="currentColor">
  </svg>
</div>
```

The custom arrow (`.Select-figure`) is optional and can be any element of choice.

```
@import "suitcss-select";

.Select--myModifier {
  margin: 2em 0;
}

.Select--myModifier .Select-control {
  background: #ccc;
  color: #333;
  border: 0;
}

...

```

## Known issues
- Dotted inner focus outline in Firefox
- Falling back to the native arrow (hiding the custom one) in IE<10 & Firefox<35
- Blue focus state in IE<10
- Custom arrow is unclickable in IE10 unless the figure is a svg element
