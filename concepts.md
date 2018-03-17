# Concepts
- Two-way data binding
	- the holy grail Web development frameworks.

## Web Components
- Custom elements
- Shadow DOM
- HTML templates and slots
- HTML imports

### Design Pattern
[Source](https://medium.com/samsung-internet-dev/lessons-learned-making-our-app-with-web-components-bf55379cfcda)
- **HTML** is used for configuration and sets the initial state of the page.
- **State** is maintained by each component individually and can be accessed by properties on the object.
- **Inter-component messaging** is handled by event listeners.

### Three Parts
- A **`<template>`** with the hidden structure of the Web Component. It may contain one or more `<slot>` for where the component’s descendants get added.
- A **`<style>`** in the `<template>` for how the element should appear.
- A definition **`class`** in JavaScript which extends from `HTMLElement`.