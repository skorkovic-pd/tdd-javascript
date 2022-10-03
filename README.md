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
// package.json

{
   ...other package.json stuff
   "scripts": {   
     "test": "jest" // this will run jest with "npm run test"
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


## Important commands

Run tests:
```bash
npm run test
```




Use the package manager [pip](https://pip.pypa.io/en/stable/) to install foobar.
