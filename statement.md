# ES6 - Default Function Parameters

Default function parameters allow formal parameters to be initialized with default values if no value or undefined is passed.

```javascript runnable
'use strict';
var getEmployee = function(empId) {
    console.log(empId);
};
getEmployee();
```
```javascript runnable
'use strict';
var getEmployee = function(empId = 101) {
    console.log(empId);
};
getEmployee();
```
```javascript runnable
'use strict';
var getEmployee = function(empId = 101) {
    console.log(empId);
};
getEmployee(201);
```

```javascript runnable
'use strict';
var getEmployee = function(empId = 101, project = 'ABC') {
    console.log(empId + ', ' + project);
};
getEmployee(undefined, 'XYZ');
```
```javascript runnable
'use strict';
var getSum = function(num1, num2 = num1 + 10 ) {
    console.log(num1 + num2);
};
getSum(10);
```
```javascript runnable
'use strict';
var a = 5;
var getTotal = function(num1, num2 = num1 * a ) {
    console.log(num1 + num2);
};
getSum(10);
```
```javascript runnable
'use strict';
var getSum = () => 5;
var getTotal = function(num1, num2 = num1 * getSum()) {
    console.log(num1 + num2);
};
getTotal(10);
```
```javascript runnable
'use strict';
var getSum = function(num1, num2 = 20 ) {
    console.log(arguments.length);
};
getSum(10);
```
```javascript runnable
'use strict';
var getTotal = function(num1 = num2, num2 = 20) {
    console.log(num1 + num2);
};
getTotal(10);
```
```javascript runnable
'use strict';
var getTotal = new Function("num = 20.00", "return num;");
console.log(getTotal());
```
# Advanced usage

If you want a more complex example (external libraries, viewers...), use the [Advanced Node.js template](https://tech.io/select-repo/442)
