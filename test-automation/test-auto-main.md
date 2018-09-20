# Test automation: Manual vs. Automated tests
In software testing, test automation is the use of special software (separate from the software being tested) to control the execution of tests and the comparison of actual outcomes with predicted outcomes. Test automation can automate some repetitive but necessary tasks in a formalized testing process already in place, or perform additional testing that would be difficult to do manually. In other words automated test is kind of software which is developed to verify if main application conform to specs. To develop an automated test you need to have basic [programming skills](programming-skills.md). Test automation is critical for continuous delivery and continuous testing.
### Manual

#### Pros:

* Get visual feedback. Scripts can’t provide opinions and input about how a UI looks and feels like a person can.
* The human element. You’re getting the exact kind of feedback a person would give you, and that can be invaluable. Being able to predict what your users will or won’t like—things a computer can’t give feedback on—ahead of time can influence your design and make it better from the bottom up.
* Less expensive in the short-term. If you’re only testing a simple app once, and don’t expect lots of updates, manual testing doesn’t require you to invest in expensive tools or software.
* Flexible, on-the-fly testing. Testing requires you to write, program, and review test cases for your software. But, if you really only need to test one small change, you can manually test it right then and there.

#### Cons:

* Less thorough than automation testing. You always have to account for human error. When a script is running the testing, it’s less likely to skip or miss things.
* Testing fatigue. Just like how you wouldn’t want the developers who’ve built an application to test if to QA because they’re so intimately familiar with it, there’s the risk that your QA people could get used to your application and know how it works. This can lead to testing fatigue and errors slipping through the cracks. Tedious, repetitive tasks can make testers weary, so they’re more prone to missing a mistake.
* Not reusable. If you foresee a lot of changes and updates to your app in the future, you’ll have to manually test all over again to ensure no new changes broke the build.

### Automated

#### Pros:

* Find more bugs than a human tester. Scripts can be much more thorough, catching bugs that humans might miss-due either to volume or monotony of the task.
* Get the speed and efficiency of computers. Scripts are faster than humans, so you’ll get more done in less time.
* Reusable tests for code that gets frequent updates. If you’re constantly making updates and republishing units, you don’t have to rewrite test scripts each time, you can reuse them in your regression testing.
* Gives your team a break. There’s a better chance your development team will get fatigued and weary if they’re manually testing an app after coding it. Automating testing will give them a chance to focus more on the big picture.
* Better visibility into app performance. With automation testing, it’s easier for the team as a whole to review results and be on the same page, vs. one person manually compiling testing results.
#### Cons:
* Lacks the human element. As we mentioned above, manual testing gives the added human element of an actual user interacting with an app, and all the preferences and visual cues that come along with it.
* Less UI feedback. Without that human element, you also won’t get insight into visual elements of your UI, like color choices, font size, contrast, or button sizes.
* Can get pricey. The tools (and even the up-front time) to run automation testing can be pricey, but factor in the reusability and time saved.


There’s no silver bullet for testing during the development process. Despite the wide variety of testing techniques and tools, we cannot rely on a single approach. Automated and manual testing each have their strengths and weaknesses. What we want to stress is that no matter how great automated tests are, you cannot automate everything. Manual tests play important role in software development and come in handy whenever you cannot automate the process.


# Test Automation Patterns
Test automation patters quite important to keep your code clean and maintainable. Pattern is a proven solution to solve an issue. Using a pattern you choose tried and tested solution already, which ensures stability of your tests.
#### Page Object Model
Page Object Model pattern requires to separate page elements locators from methods (tests) where these elements used. That approach makes tests more maintainable in case of page refactoring or elements change. Lets' assume you use same button in 10 scripts. With any change of that button, you will need to make a change in 10 scripts, while in case of using POM only one change will be needed. Below you will find a few links with implementation examples of POM in Java and JavaScript:
* https://github.com/SeleniumHQ/selenium/wiki/PageObjects (Java)
* https://www.pluralsight.com/guides/software-engineering-best-practices/getting-started-with-page-object-pattern-for-your-selenium-tests (Java)
* http://www.seleniumhq.org/docs/06_test_design_considerations.jsp#page-object-design-pattern (Java or JavaScript)
* http://www.seleniumeasy.com/selenium-tutorials/page-object-model-framework-introduction (Java)

#### Page Factory
The PageFactory Class in Selenium is an extension to the Page Object design pattern. It is used to initialize the elements of the Page Object or instantiate the Page Objects itself. It is used to initialize elements of a Page class without having to use ‘FindElement’ or ‘FindElements’. Java examples:
* http://toolsqa.com/selenium-webdriver/page-object-pattern-model-page-factory/
* https://www.toptal.com/selenium/test-automation-in-selenium-using-page-object-model-and-page-factory
* https://github.com/SeleniumHQ/selenium/wiki/PageFactory

#### Page Element
When you try to incorporate all the elements of a page in one single page class, it becomes too big to read, maintain etc. The class might contain too many responsibilities to handle. It should be restructured and broken into smaller classes. The main idea and requirement – page objects to satisfy the Single Responsibility Responsible.

#### Loadable Component
The LoadableComponent is a base class that aims to make writing PageObjects less painful. It does this by providing a standard way of ensuring that pages are loaded and providing hooks to make debugging the failure of a page to load easier. You can use it to help reduce the amount of boilerplate code in your tests, which in turn make maintaining your tests less tiresome. Java examples:
* https://github.com/SeleniumHQ/selenium/wiki/LoadableComponent
* https://www.lambdatest.com/blog/loadable-components-in-selenium-make-your-test-robust-for-slow-loading-web-pages/

#### Chain of Invocations
Method chaining, also known as named parameter idiom, is a common syntax for invoking multiple method calls in object-oriented programming languages. Each method returns an object, allowing the calls to be chained together in a single statement without requiring variables to store the intermediate results.
* https://gerardnico.com/code/design_pattern/fluent_interface
* Implementation [example](https://stackoverflow.com/questions/21180269/how-to-achieve-method-chaining-in-java) in Java
* Implementation [example](https://schier.co/blog/2013/11/14/method-chaining-in-javascript.html) in JavaScript
* https://stackoverflow.com/questions/1103985/method-chaining-why-is-it-a-good-practice-or-not/

#### Decorator
Decorator is a design pattern that allows behavior to be added to an individual object, either statically or dynamically, without affecting the behavior of other objects from the same class. The decorator pattern is often useful for adhering to the Single Responsibility Principle, as it allows functionality to be divided between classes with unique areas of concern. Java examples:
* https://en.wikipedia.org/wiki/Decorator_pattern
* https://sourcemaking.com/design_patterns/decorator

#### Builder
The Builder design pattern is a creational design pattern, designed to provide a flexible design solution to various object creation problems in Object-Oriented software. The intent of the Builder design pattern is to separate the construction of a complex object from its representation. Java examples:
* https://en.wikipedia.org/wiki/Builder_pattern
* https://sourcemaking.com/design_patterns/builder

#### Proxy
A proxy, in its most general form, is a class functioning as an interface to something else. The proxy could interface to anything: a network connection, a large object in memory, a file, or some other resource that is expensive or impossible to duplicate. In short, a proxy is a wrapper or agent object that is being called by the client to access the real serving object behind the scenes. Use of the proxy can simply be forwarding to the real object, or can provide additional logic. Java examples:
* https://en.wikipedia.org/wiki/Proxy_pattern
* https://sourcemaking.com/design_patterns/proxy


# Test automation solutions([link](test-auto-solutions.md))
* Java + Maven + JUnit + Selenium + Cucumber
* JS + Jasmine + Gulp
* JS + CucumberJS + Gulp
* Xebium
* Python
* Cypress.IO
