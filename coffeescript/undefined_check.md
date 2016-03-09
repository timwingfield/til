### Undefined comparison

In coffeescript when doing an `undefined` comparison with `===` it will convert to `void 0`.

Coffee: `if myVar == undefined`

compiled javascript: `if(myVar === void 0)`

---

If you need to compare against undefined, use the `myVar?` syntax.

Coffee: `if myVar?`

compiled javascript: `if(myVar !== undefined && myVar !== null)`
