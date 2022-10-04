# TDD with Javascript

Repository used to setup Jest and create project for learning Test Driven Development during Prodyna Workademy.

## Set up Jest with Javascript project

Create NPM project:

```bash
npm init
```
Create **.js** (for example **id.js**) file and move it to the project's root.

Install Jest:
```bash
npm install jest --D
```
Update the package.json test script
```json

{
   ...other package.json stuff
   "scripts": {   
     "test": "jest"
   }
}
```

## Create first test and run it

Run test:
```bash
npm run test
```
You should get:
```
No tests found
In /****/
  3 files checked.
  testMatch: **/__tests__/**/*.js?(x),**/?(*.)+(spec|test).js?(x) - 0 matches
  testPathIgnorePatterns: /node_modules/ - 3 matches
```
Jest is searching a file name that contains **.spec** or **.test**.
Let's rename **id.js** to **id.spec.js**

Run test again. You should get error output:
```
FAIL  ./id.spec.js
  ● Test suite failed to run
  
Your test suite must contain at least one test.
```

So it found the file, but there are are not tests - empty file.

Let's write a first test. Use **it()** or **test()** function to define each test:

```javascript
test('Jest is working', () => {
   expect(1).toBe(1);
});
```
Run test again. Now you should get output with success message (PASS):
```
PASS  ./id.spec.js
  ✓ Jest is working (3ms)
  
Test Suites: 1 passed, 1 total
Tests:       1 passed, 1 total
Snapshots:   0 total
Time:        1.254s
Ran all test suites.
```

So our first test passed!
Let's describe how we wrote our first test:  
***test('Jest is Working')*** - define new test with title

***...() => { expect(1).toBe(1) });*** - function where we actually assert something about our code (not in that case, that will always be true)


Good practise is to organize test in groups. Function **describe()** is used for that:

```javascript
describe('First group of tests', () => {
   test('Jest is working', () => {
      expect(1).toBe(1);
   });
});

describe('Second group of tests', () => {
   test('Second test is working also', () => {
      expect(1).toBe(1);
   });
});
```

Run tests again, and you should get:
```
PASS  ./id.spec.js
  First group of tests
    ✓ Jest is working(4ms)
  Second group of tests
    ✓ Second test is working also
```

## Use TDD to create first unit
We want to develop calculator. First that we have to think about is what we expect calculator can do, and after that test can be written.

Before next steps create empty directory and do again steps for setup Jest. File for code and test can be named, for example, *calculator.js* and *calculator.test.js*


#### 1. Calculator can do the addition of two numbers
Let's create test (in your test file):
```javascript
const addCalculator = require("./calculator");

test("addition of 2 and 3 to equal 5", () => {
  expect(addCalculator(2, 3)).toBe(5);
});
```
Run test now. The test would fail because you've not developed the program for which you created the test. So, let's do that now!
Open code file and develop a program to pass the test.

```javascript
function addCalculator(a, b) {
  return a + b;
}

module.exports = addCalculator;
```
Run tests again. Output should be:
```
 PASS  ./addCalculator.test.js
  √ addition of 2 and 3 to equal 5 (2 ms)
```

#### 2. [Exercise] Using TDD implement functions for 



## Important commands

Run all tests:
```bash
npm run test
```
Run tests from specific file:
```bash
npm run test [file-path]
```

Define test
```javascript
test('test-name', () => {
   //body of test (with assertion)
});
```





Use the package manager [pip](https://pip.pypa.io/en/stable/) to install foobar.
