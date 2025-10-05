# Par 25 (motions / actions)

## Solution:

```js
test('adds', () => {
  expect(add(2, 3)).toBe(5)
})

const add = (a, b) => a + b
const sub = (a, b) => a - b

test('subtracts', () => {
    expect(sub(3, 2)).toBe(1)
})
```

[ ] <- Cursor starts here

```js
test('subtracts', () => {
    expect(add(2, 3)).toBe(5)
})

const sub = (a, b) => a + b
const add = (a, b) => a - b

test('adds', () => {
    expect(sub(3, 2)).toBe(1)
})
```

