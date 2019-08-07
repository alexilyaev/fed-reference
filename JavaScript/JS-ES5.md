# JS - ES5

## Strict Mode

- [What Does "use strict" Do in JavaScript?](https://masteringjs.io/tutorials/fundamentals/strict)
- [MDN - Strict Mode](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Strict_mode)

### Highlights

- No more implied global variables (catches missing var declarations and typos in variable names)
- Function parameter names must be unique `function sum (x, x) {...}`
- `this` is not bound to the global object by function form, will be `undefined` instead
- `apply` and `call` do not default to the global object if passing `null` or `undefined` as context
- `arguments` not linked to function parameters (changing one does not affect the other)
