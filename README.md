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