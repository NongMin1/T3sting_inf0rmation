# Solution for test automation project

### Java + Maven + JUnit + Selenium + Cucumber

1. There are a wide range of ways to create a UI test on Java. One of them utilize following tools: [Maven](https://maven.apache.org/ ) + [JUnit](https://junit.org/junit5/) + Selenium + [Cucumber](https://cucumber.io/).
[Maven](https://maven.apache.org/ ) is a build automation tool (widely used in Java projects).


2. [JUnit](https://junit.org/junit5/) – testing framework for Java. JUnit community is very large and an answer can be easily found in the internet.
User guide: https://junit.org/junit5/docs/current/user-guide/

3. Selenium – tool that automates browsers or in other words simulates user actions in browser. Nowadays all major browser vendors create their own drivers for selenium.

4. [Cucumber](https://cucumber.io/) - framework for Behavior Driven Development: [Getting started](https://cucumber.io/docs/reference/jvm#java),
[Cucumber on GitHub](https://github.com/cucumber/cucumber-jvm)

[Tutorial](http://toolsqa.com/cucumber/cucumber-tutorial/) which combines Maven + JUnit + Selenium + Cucumber.

Implicit Wait & Explicit Wait [in Selenium](https://www.guru99.com/implicit-explicit-waits-selenium.html)


### JavaScript + Jasmine + Gulp

**Protractor** is a main framework used for angular applications automated testing, useful links:

* Project page: http://www.protractortest.org/#/
* Protractor API: http://www.protractortest.org/#/api
* Element locators: http://luxiyalu.com/protractor-locators-selectors/

[**Jasmine**](https://jasmine.github.io/) is a behavior-driven development framework for testing JavaScript code. It does not depend on any other JavaScript frameworks. It does not require a DOM. And it has a clean, obvious syntax so that you can easily write tests. Jasmine is default framework for Protractor.

* [Getting started](https://jasmine.github.io/setup/nodejs.html)(note: that is a pure Jasmine, not with a Protractor)
* [Documentation](https://jasmine.github.io/pages/docs_home.html) (note: that is a pure Jasmine, not with a Protractor)
* Complete information about **Protractor** with Jasmine framework in presented on protractor page [link#1](https://www.protractortest.org/#/tutorial), [link#2](https://www.protractortest.org/#/toc)

Alternative description how to use page objects with **Protractor** is [here](https://moduscreate.com/blog/protractor-and-page-objects/).

**Gulp** is a JavaScript Task Runner. It help to automate any kind of tasks, such as starting web server, launching tests and etc. Simple example how to start your Protractor tests with gulp can be found [here](https://github.com/mllrsohn/gulp-protractor).


### JavaScript + CucumberJS + Gulp


Protractor is end to end testing framework used for Angular and AngularJS applications testing. Protractor runs tests against your application running in a real browser, interacting with it as a user would.
Useful links:

* Project page: http://www.protractortest.org/#/ (contains information about installation and simple example)
* Description of Protractor API: http://www.protractortest.org/#/api

Angular has specific elements attributes, which can be used for locating elements, some information about element locators in protractor: http://luxiyalu.com/protractor-locators-selectors/

Cucumber - framework for Behavior Driven Development which merges specification and test documentation into one cohesive whole.

Project page: https://cucumber.io/

Cucumber implementation for JavaScript: https://github.com/cucumber/cucumber-js

A few tutorials how to use setup both Protractor and Cucumber in one project:
* https://medium.com/osldev-blog/tutorial-creating-maintainable-e2e-tests-with-protractor-and-cucumber-513435a71db3
* https://www.eriklieben.com/protractor-end-to-end-testing-with-gherkin-syntax-and-typescript-decorators/
* https://semaphoreci.com/community/tutorials/getting-started-with-protractor-and-cucumber

[Example](https://codoid.com/protractor-cucumberjs-and-gulp-example/) on running Protractor with CucumberJs from gulp:



Might be useful to know a bit about **promises** in JavaScript, because Protractor uses them everywhere:
* https://developers.google.com/web/fundamentals/primers/promises
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise


### Xebium

[Xebium](http://xebia.github.io/Xebium/) enables us to use both Selenium IDE (low learning curve) and FitNesse (ease of maintenance) to it's fullest and provides a complete solution when it comes to automated web testing.


Xebium setup: https://www.theqacoach.com/testing-and-qc/installing-xebium-for-the-first-time

Download Xebium formatter addon for Firefox: https://addons.mozilla.org/en-US/firefox/addon/selenium-xebium-formatter/

By default Xebium runs on Firefox browser, however it’s possible to setup Safari, Chrome and IE: https://www.theqacoach.com/testing-and-qc/setting-up-ie-chrome-and-safari-drivers-to-work-with-xebium

**Important**: Xebium does not support latest Firefox versions so downgrade is required to be able to run.

If application elements do not contain unique identifiers, it’s a good practice to use XPath for targeting elements within a webpage: https://www.guru99.com/xpath-selenium.html

XPath Axes: https://www.w3schools.com/xml/xpath_axes.asp


### Python

Selenium + Python link is [here](http://selenium-python.readthedocs.io/).

### Cypress.IO

How to configure Cypress.IO you can find [here](https://angularfirebase.com/lessons/cypress-angular-testing-end-to-end/). 

### EXTRA
### Continues integration
Jenkins:
Couse and the file with information can be found [here](https://www.udemy.com/jenkins-intro/learn/v4/content)

