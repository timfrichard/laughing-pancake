![Protractor, Jasmine and Typescript](./images/protractor-jasmine-typescript.png?raw=true "Protractor, Jasmine and Typescript")

# Protractor, Jasmine and Typescript Setup Guide

This is Test Automation framework designed using Protractor, Jasmine and TypeScript

## Framework Structure

```
├───.circleci                       # This contains CircleCI config.yml file
├───images                          # This folder contains sample report image
├───page-objects                    # This folder contains page object, page helper and page contants
│   ├───common
│   └───pages
│       ├───common
│       └───super-calculator
├───temp                            # This folder contains JS file which are generated after compiling TypeScript files
├───test-results                    # This folder contains test result (includes html report and screenshots)
└───test-suites                     # This folder contains spec/test files
```

## To Get Started

### Pre-requisites

- Download and install Chrome or Firefox browser.
- Download and install Node.js
- Download and install any Text Editor like Visual Code/Sublime/Brackets

### Setup Scripts

- Clone the repository into a folder
- Install Protractor: `npm install -g protractor`
- Update necessary binaries of webdriver-manager: `webdriver-manager update` or `npm install -g webdriver-manager`
- Go to Project root directory and install Dependency: `npm install`
- While still in the root directory run the following command: `npm run webdriver-update`
- All the dependencies from package.json and ambient typings would be installed in node_modules folder.

### How to write Test

- Add new spec under test-suite folder
- Name the file as <testname>.spec.ts (e.g. super-calculator.spec.ts)
- Create folder under page-objects/pages as <page-name> (e.g. super-calculator)
- Under page folder create constant, helper and page object file.
  - <page-name>.constants.ts (e.g. super-calculator.constants.ts)
  - <page-name>.helper.ts (e.g. super-calculator.helper.ts)
  - <page-name>.po.ts (e.g. super-calculator.po.ts)

### How to Run Test

- Run complete Test Suite: `npm test`

### How to Update local npm packages

- Go to Project root directory and run command: `npm update`

### How to Run Update WebDriver

- Go to Project root directory and run command: `npm run webdriver-update`

### How to Clean Artifacts from Previous Run

- Go to Project root directory and run command: `npm run clean`

## See the following page for how-to

- https://github.com/timfrichard/laughing-pancake/tree/main/protractor-to-webdriver-demo


## Things that need to be checked from a Protractor perspectve
- import { browser } from "protractor" .getCapabilities .element .wait 
- import { browser, by, ElementFinder, ExpectedConditions } from 'protractor' ExpectedCondition.presenceOf
- import { $, by, ElementFinder, ExpectedConditions } from 'protractor'
- import { browser, by, ElementArrayFinder, ElementFinder, ExpectedConditions} from 'protractor'
- import { browser, by, element, ElementFinder, ExpectedConditions } from 'protractor'

