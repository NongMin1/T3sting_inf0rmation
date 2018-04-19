# Apache JMeter

Official page for all information you will need: https://jmeter.apache.org/

Useful Udemi learnings to Complete: [JMETER - Master Performance & Load Testing(Basics + Advance)](https://ibm-learning.udemy.com/jmeter-tutorial/?src=sac&kw=jmeter)

#### What is different between: Load / Performance / Stress testing?
http://toolsqa.com/software-testing/differences-between-performance-load-and-stress-testing/

#### Apache JMeter features include:
* Ability to load and performance test many different applications/server/protocol types: 
    * Web - HTTP, HTTPS (Java, NodeJS, PHP, ASP.NET, …)
    * SOAP / REST Webservices
    * FTP
    * Database via JDBC
    * LDAP
    * Message-oriented middleware (MOM) via JMS
    * Mail - SMTP(S), POP3(S) and IMAP(S)
    * Native commands or shell scripts
    * TCP
    * Java Objects
* Full featured Test IDE that allows fast Test Plan **recording (from Browsers or native applications), building and debugging**.
* [Command-line mode](https://jmeter.apache.org/usermanual/get-started.html#non_gui) ([Non GUI / headless mode](https://jmeter.apache.org/usermanual/get-started.html#non_gui)) to load test from any Java compatible OS (Linux, Windows, Mac OSX, …)
* A complete and [ready to present dynamic HTML report](https://jmeter.apache.org/usermanual/generating-dashboard.html)
* Easy correlation through ability to extract data from most popular response formats, [HTML](https://jmeter.apache.org/usermanual/component_reference.html#CSS/JQuery_Extractor), [JSON](https://jmeter.apache.org/usermanual/component_reference.html#JSON_Extractor) , [XML](https://jmeter.apache.org/usermanual/component_reference.html#XPath_Extractor) or any [textual format](https://jmeter.apache.org/usermanual/component_reference.html#Regular_Expression_Extractor)
* Complete portability and **100% Java purity**.
* Full multi-threading framework allows concurrent sampling by many threads and simultaneous sampling of different functions by separate thread groups.
* Caching and offline analysis/replaying of test results.
* Highly Extensible core: 
    * Pluggable Samplers allow unlimited testing capabilities.
    * Scriptable Samplers (JSR223-compatible languages like Groovy and BeanShell)
    * Several load statistics may be chosen with pluggable timers.
    * Data analysis and visualization plugins allow great extensibility as well as personalization.
    * Functions can be used to provide dynamic input to a test or provide data manipulation.
    * Easy Continuous Integration through 3rd party Open Source libraries for Maven, Graddle and Jenkins



### Useful links:
#### Jmeter Tutorial - Testing REST Web Services:
* https://www.testingexcellence.com/jmeter-tutorial-testing-rest-web-services/
* https://www.blazemeter.com/blog/rest-api-testing-how-to-do-it-right

```markdown
Performance testing - Test example:

Performance Test Authentication Thread Properties:

    * Number of Threads: 10 or 15
    * Ramp-Up Period: 5
    * Loop Count: 15

Number of Threads(users):
    Described the total number of threads or users used to execute test plan.
    Each and every user will execute full test plan.

Ramp-Up Period (In Seconds):
    Describes time to load all users given in "Number of Threads(users)" Property.
    
Loop Count:
    Describes how many times your test plan will be executed.
    If you will set it 5 then full test plan will be executed 5 time.
    If you will select "Forever" check box then your test plan will run your test plan forever time.
    You have to stop its execution manually if you selected "Forever" check box.
    If I have set Loop Count = 2, jMeter will run test plan only 2 times.
```
```
Number of Threads VS Ramp-Up Period Example:
    If you will set Number of Threads(users) = 10
    and Ramp-Up Period (In Seconds) = 100
    then Jmeter will load all 10 users in 100 seconds means every
    1 user will be loaded after every 10 seconds (100(seconds)/10(Users) = 10 seconds).
```

Running Jmeter from laptop or desktop PC has some user (thread) limitation: 50 users for laptops and up to 100 for powerful desktops. If you need a higher load, you may need to use a [remote testing](http://jmeter.apache.org/usermanual/remote-test.html) or there is always a way to use paid services for load testing, such as [BlazeMeter](https://www.blazemeter.com/). They tipically support Jmeter project file, all you need to setup a proper configuration and choose which servers to use for a load generation.