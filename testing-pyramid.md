# Testing Pyramid

Talking about test automation most people thinks about end to end tests or UI tests. However, there are 3 types of automated tests:
End to end (E2E) or UI tests – tests which simulate user actions – launch browser, navigate to certain page, enters something or click buttons.
Integration tests – tests, that verifies individual software modules combined as a group.
Unit tests – tests for individual units of source code
Each test type has its’ pros and cons:

* | Pros | Cons
-----|-----|----- 
**UI** | Go end to end, See what user would see | Expensive, Slow
**Integration** |	Web services and APIs, Connectivity |	Not most precise
**Unit** |	Amazingly fast, Extremely versatile |	Miss integrations

The testing pyramid show the way to combine all tests types for best result:
* We want to have as much unit tests to cover everything that possible with tests and that why the amount of that kind of tests is biggest
* We need to have a full set of integration tests to check connectivity between modules, but the variation count is much less than on the unit level, which mean less integration tests count
* We may want to cover everything with E2E tests, but they are very time consuming, so we tend to use them sparingly

<img width="700" alt="testingpyramid" src="https://media.github.ibm.com/user/57353/files/0a88b908-31cc-11e8-9dca-58b46531a544">

Fig 1. Testing pyramid