```js
function almostAlwaysTrue(a) {
  console.log(a == a)
}

almostAlwaysTrue(NaN) // false - this is easy

// -----

function usuallyFalse(a) {
  console.log(!a == a)
}

usuallyFalse('0')                 // true
usuallyFalse(' ')                 // true
usuallyFalse([])                  // true
usuallyFalse([undefined])         // true
usuallyFalse([null])              // true
usuallyFalse([false])             // false - outlier
usuallyFalse([0])                 // true
usuallyFalse([''])                // true
usuallyFalse([' '])               // true
usuallyFalse(['0'])               // true
usuallyFalse(new Boolean(false))  // true - in fact, this is the most bizarre
usuallyFalse(new String())        // true

// -----

function inMostCasesTrue(a) {
  console.log(a >= a)
}

inMostCasesTrue(NaN)        // false
inMostCasesTrue(undefined)  // false

// -----

function couldThisBeTrue(a) {
  console.log(a == a + 1)
}

couldThisBeTrue(2**53)  // true - float64 precision loss

// -----
```
