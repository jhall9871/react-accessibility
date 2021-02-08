# React Accessibility
Working through a TODO list app from [Mozilla](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks/React_todo_list_beginning).

## A11y Takeaways
- `<ul role='list'` so that styling doesn't ruin screen reader behavior on lists
- `aria-labeledby="list-heading"` allows assistive technology to catelog an object

## Other Takeaways
- [NanoID](https://github.com/ai/nanoid) for generating unique ids
- Define `const` variables that will never change outside the `App()` function, and use `ALL_CAPS`. This way it's clear what they are, and they won't be recalculated each time the `<App />` renders.
- `onClick()` functions written inline when short keeps top of file clearer.
- Map over arrays returning components before the return statement, like:
```
  const filterList = FILTER_NAMES.map((name) => {
    <FilterButton key={name} name={name} />;
  });
```
- `tabindex="-1"` means "only focusable with JavaScript"
- `tabindex="0"` means "focusable with tab like a button"