# API testing

### Soap UI

SoapUI is a tool for all kind of Web services testing.
More information about it we can find in official [user guide](https://www.soapui.org/articles/user-guide.html).

On official page we can find such points like:
* Main information about SoapUI;
* Tutorials;
* Trainings;
* World of API testing;
* SoapUI News;

SoapUI provides extensive options for scripting, using either Groovy or Javascript (since SoapUI 3.0) as its scripting language.

The plus of SoapUI is that You can run test via CMD, more info about running from *cmd* can be found [here](https://www.soapui.org/test-automation/running-from-command-line/functional-tests.html).

 
**What is SoapUI:**
https://www.guru99.com/introduction-to-soapui.html

**SoapUI installation and configuration guide:**
https://www.guru99.com/soapui-installation-configuration.html

**SoapUI beginner tutorial:**
https://www.guru99.com/webservice-testing-beginner-guide.html

**How SoapUI works/how to deal with it:**
https://www.youtube.com/watch?v=izA_Xgbj7II 
#
### REST API testing in Java: Feign, Swagger Code Generator
There are a lot of ways how to test service. Main goal is to determine if API meets expectations for functionality, reliability, also performance testing is mostly focused on APIs. Idea is simple – send a request and analyze response if all needed information is in place. The first option – generate request manually, wait for response and then manually extract information from it. Simple, but not very fast implementation, plus need to foresee network problems and include error processing.

**Feign**<br>
Hopefully there is a tool named [Feign](https://github.com/OpenFeign/feign) developed by Netflix. This is a Java to HTTP client binder, which sends request to service, waits for response and serializes response. What does it mean for us: we need to create a class for expected response and point Feign to use this class to serialize the response. Response serialization into class makes comparison of received values much easier. Also, all communication with API is being handled on Feign side. Just need to check if there was any kind of network error. Tutorial and code examples on Feign is [here](https://howtoprogram.xyz/2016/07/18/java-rest-client-using-netflix-feign/).

**Swagger Code Generator**<br>
Using just Feign library slows tests development, especially when small changes comes to response structure. Hopefully there is a tool named [Swagger Code Generator](https://github.com/swagger-api/swagger-codegen), which can generate response classes by swagger file. So, you can spend all your time on tests. Classes generation can be triggered from command line or maven plugin. Java is one of supported language. Project page contains information how to install and use examples of code generator. A nice article how to use swagger code generator with Maven in [real project](https://blog.philipphauer.de/enriching-restful-services-swagger/)
#
### Public Services and UI
**Public APIs or public services** – open is a publicly available application programming interface that provides developers with programmatic access to a proprietary software application or web service. As testers we can use them for training our automated integration testing skills.
Here a few public APIs to try yourself integration/service tests:
* http://httpbin.org/ 
* https://jsonplaceholder.typicode.com/
* https://reqres.in/
* http://www.hostip.info/use.html

**UI**:
There are a lot of technologies for front end. A huge library of pages with different technologies available [here](https://www.awwwards.com/websites/).


