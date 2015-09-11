## .Select component

A [SUIT CSS](https://github.com/suitcss/suit/) component providing a solid base for redesigning the native select element

## Installation

```
$ npm install suitcss-select
```

## Available selectors

- `.Select` – The core wrapper element
- `.Select.is-disabled` – For disabled-state styles (must also include the `disabled` attribute)
- `.Select-control[:hover|:focus|:active]` – The `<select>` element used for most of the styling
- `.Select-figure` – The custom drop-down arrow

## Configurable variables

Use these for the widest browser support, instead of overriding.

- `--Select-color`
- `--Select-focus-color`

## Example

```html
<div class="Select">
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

```css
@import "suitcss-select";

:root {
  --Select-color: gray;
  --Select-focus-color: darkgray;
}

.Select {
  margin: 2em 0;
}

.Select-control {
  background: lightgray;
  border: 0;
  border-radius: 0.2em;
}
```

## Known issues
- Falling back to the native arrow (hiding the custom one) in IE<10 & Firefox<35
- Blue focus state in IE<10
- The custom arrow is unclickable in IE10 unless it's an svg element
