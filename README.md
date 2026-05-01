# Playwright
Playwright JS/TS Automation Testing from Scratch &amp; Framework


| Capability             | Selenium                | Playwright  |
| ---------------------- | ----------------------- | ----------- |
| Network mocking        | ❌ external proxy needed | ✔ native    |
| Multi-session contexts | ❌ new browser required  | ✔ built-in  |
| Trace debugging        | ❌ limited               | ✔ built-in  |
| API testing            | ❌ external library      | ✔ built-in  |
| Test runner            | ❌ external              | ✔ built-in  |
| Driver management      | ❌ manual                | ✔ automatic |


Playwright → Browser protocol

Selenium → HTTP → Driver → Browser (Automation tool → WebDriver server → Browser)

Purpose of Node.js:
Executes JavaScript outside the browser
Provides the package manager npm
Allows installing automation libraries like Playwright

nvm - Manage Node version
nvm root - Get root path will contain nodejs folders
nvm -version
nvm ls - list versions installed
nvm use - select version 
mkdir 

npm init playwright -create in project folder
You can also use terminal in vs code to run in your project folder

playwright.config.js
--similar to ApplicationSettings.xml in algoQA AF --test runner configuration
controls test execution
browser configuration
parallel runs
timeouts
retries
reporters
browsers (Chromium, Firefox, WebKit)
test folder location
headless/headed mode
base URL

Java → pom.xml
Node → package.json

Running one command creates a ready-to-use automation framework skeleton for Playwright.
playwright-project
 ├─ node_modules
 ├─ tests
 │   └─ example.spec.js
 ├─ playwright.config.js
 ├─ package.json
 ├─ package-lock.json
 └─ .github

import { test, expect } from '@playwright/test';
Here we are importing test and expect from playwright test

test('has title', async ({ page }) => {
  await page.goto('https://playwright.dev/');

Here test - we are using the imported test
'has title' - is the name of the test;

async - async marks the function as asynchronous. Means This function can use "await"
        This test will perform operations that take time

({ page }) - Give me the page object
Playwright automatically provides some objects called fixtures.
One of them is: page
page represents: a browser tab

| Tool       | Object |
| ---------- | ------ |
| Selenium   | driver |
| Playwright | page   |

=> This is an arrow function in JavaScript.
Equivalent old syntax:function(page) {
Modern syntax: (page) => {


If JavaScript did NOT use destructuring :- 
test('has title', async (fixtures) => {

   await fixtures.page.goto('https://playwright.dev')
})

JavaScript destructuring:

JavaScript allows extracting properties directly from an object.
Example:
const obj = { page: "browserPage", context: "ctx" }
const { page } = obj
Now page becomes a variable.

Equivalent to:
page = obj.page 

Advantage over Selenium :
Playwright already handles lifecycle.
Each Playwright test gets a fresh browser context.

In large automation frameworks this reduces:
setup code
boilerplate
duplicate code
flaky tests

