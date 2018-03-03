# GTU 03

#### 1. wrappers

* try to understand the difference of wrapping the following values
with their default wrappers and with string wrapper
  1. `1`
  2. `2`
  3. `1395`
  4. `true`
  5. `false`

* call `valueOf` and `toString` methods for each wrapper and each value
  of the example above

* try to find a way to change value of for string wrapper to return
  correct primitives. /if it's possible/

* wrap `true`, `false`, `'hello'`, `''`, `NaN`, `0`, `1395` with their
  default wrappers and to to convert wrapped values to boolean

#### 2. strict mode

turning the browser's console to strict mode is impossible so for enabling
strict mode for your testing you have to do one of the following
1. have a file which starts with `'use strict'`;
2. put `'use strict'` before every single thing you're testing in console
3. put your test code inside immediately called function:
```javascript
(function () {
    'use strict';
    // your code here
}());
```
or
```javascript
!function () {
    'use strict';
    // your code here
}();
```
* test all `delete` tests of [gtu-02](../gtu-02) in strict mode
* test the following examples for both strict and non-strict modes
  1. `delete 1`
  2. `delete x` // where x is undeclared variable
  3. `var a; delete a;`
  4. call the following function with any argument

      ```javascript
      function f(a) {
        console.log(delete a);
        console.log(a);
      }
      ```

  5. call the following function with any argument

      ```javascript
      function f(a) {
        console.log(delete arguments);
        console.log(arguments);
      }
      ```

  6. call the following function with any argument

      ```javascript
      function f(a) {
        console.log(delete arguments[0]);
        console.log(arguments[0]);
      }
      ```

  7. call the following function with any argument

      ```javascript
      function f(eval) {
        console.log(delete eval);
        console.log(eval);
      }
      ```

  8. `var s = new String('hello'); delete s[0];`
  9. `undeclared = 4; delete undeclared;`
    **Note:** for strict mode execute the first statement in non-strict
    mode and then execute the second in strict mode.
  10. `var eval = 3;`
  11. `var a = 01395;`
  12. `var a = 01355;`
