# GTU 02

#### 1. Please try to guess, test, and then understand following examples:

Suppose that
```javascript
var a = {
    valueOf: function() {
        return 'hello';
    }
};
var b = {
    valueOf: function() {
        return 3;
    }
};
var c = {
    valueOf: function() {
        return new Number(3);
    }
};
var d = {
    toString: function() {
        return 123;
    }
};
var e = {
    toString: function() {
        return new Number(3);
    }
};
```
and suppose that `f` isn't declared

* binary `+` operator
  1. `null + undefined`
  2. `null + true`
  3. `null + false`
  4. `null + 3`
  5. `null + NaN`
  6. `null + 'hello'`
  7. `null + a + b + c + d + e + f`
  8. `undefined + true`
  9. `undefined + false`
  10. `undefined + 5`
  11. `undefined + NaN`
  12. `undefined + 'hello'`
  13. `undefined + a + b + c + d + e + f`
  14. `true + false`
  15. `true + 2`
  16. `true + NaN`
  17. `true + 'hello'`
  18. `true + a + b + c + d + e + f`
  19. `false + 4`
  20. `false + NaN`
  21. `false + 'hello'`
  22. `false + a + b + c + d + e + f`
  23. `5 + 3`
  24. `5 + NaN`
  25. `5 + 'hello'`
  26. `5 + a + b + c + d + e + f`
  27. `'hello' + NaN`
  28. `'hello' + a + b + c + d + e + f`

* try the same also for binary `-`, `*`, `/`, `%`, `|`, `&`, `^`, `<<`, `>>`, `>>>`,
 `==`, `===`, `<`, `>`, `>=`, `<=` operators
 as you did for binary `+` operator

* unary `-` operator
  1. `-null`
  2. `-undefined`
  3. `-true`
  4. `-false`
  5. `-5`
  6. `-'hello'`
  7. `-'234'`
  8. `-'234.32e3'`
  9. `-new Number(NaN)`
  10. `-new String('hello')`
  11. `-(/google.com/)`
  12. `-([])`
  13. `-([2])`
  14. `-([2, 3])`
  15. `-(function() { })`
  16. `-(a)` // test the same also for b, c, d, e and f

* try the same also for both postfix and prefix `++` and `--` operators
 as you did for unary `-` operator

* postfix and prefix `++` & `--` operators
  1. for each one of `a`, `b`, `c`, `d`, `e`, `f` try the following
    `console.log(a, a++, a);` & `console.log(a, ++a, a);`
  2. do the same also for `--` operator

* `%` operator
  1. `234 % 2`
  2. `234 % 3`
  3. `23.23 % 2 === 1.23`
  4. `234.23 % 2.223`

* try the same also for `~`, `!`, `typeof`, `void` operators
 as you did for unary `-` operator

* `?` operator
  1. `1 ? 234 : 32`
  2. for each one of `a`, `b`, `c`, `d`, `e`, `f` try the following
    `a[a.hasOwnProperty('valueOf') ? 'valueOf' : 'toString']()`

* `instanceof` operator
  1. `null instanceof Object`
  2. `true instanceof Boolean`
  3. `false instanceof Boolean`
  4. `1 instanceof Number`
  5. `NaN instanceof Number`
  6. `'hello' instanceof String`
  7. `(function () { }) instanceof Function`
  8. `(function () { }) instanceof Object`
  9. `a instanceof Object` // try the same also for b, c, d, e and f
  10. `new Number(1) instanceof Number`
  11. `new Number(NaN) instanceof Object`
  12. `/hello/img instanceof RegExp`
  13. `/hello/img instanceof Function`
  14. `/hello/img instanceof Object`

* `in` operator
  1. `'valueOf' in null`
  2. `'valueOf' in undefined`
  3. `'valueOf' in true`
  4. `'valueOf' in 1`
  5. `'valueOf' in 'toString'`
  5. `'valueOf' in new Number(1)`
  7. `'x' in new Number(1)`
  8. `'valueOf' in a` // try the same also for b, c, d, e and f
  9. `'toString' in a` // try the same also for b, c, d, e and f
  10. `'call' in ({})`
  11. `'call' in (function () { })`

* `delete` operator
  1. `delete ({}).valueOf`
  2. `delete 1`
  3. `delete 1.2`
  4. `delete 1.2.toString`
  5. `delete a.x`
  6. `a.y = 3; console.log(delete a.y);`
  7. `delete f`
  8. `delete z`
  9. `var x = 3; console.log(delete x); console.log(x);`
  10. `y = 4; console.log(delete y); console.log(y);`
