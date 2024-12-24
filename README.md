# Tailwind CSS Classes Not Applied to Conditionally Rendered Elements

This repository demonstrates a common issue when using Tailwind CSS with frameworks like Vue.js: Tailwind classes not being applied to elements that are conditionally rendered or part of dynamic components.

The core problem is that Tailwind processes styles during the build process, and if the element to which a class is applied doesn't exist in the DOM at that time, the class won't be rendered.

## Bug:
The `bug.vue` file shows a basic example of a conditionally rendered div element. If the `showElement` data property is false (as it is initially), the `bg-blue-500` class won't be applied.

## Solution:
The `bugSolution.vue` file presents a solution using the `v-if` directive's ability to properly integrate with Tailwind's processing cycle and ensures that the class is applied correctly.