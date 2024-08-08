# CT

Here's a structured summary based on the information provided:

---

### Project Summary
**VeloCT Name:** Auto-Trigger Failed Scenarios on Jenkins  
**Description:** Implements a retry mechanism to automatically rerun failed test cases within Jenkins, improving test reliability and reducing manual effort.

### Pre-requisites
- **Automation Framework:** Cucumber with JUnit
- **Technology/Frameworks Used:** Java, Selenium
- **Environment Components:** Gradle, Cucumber, Java, JUnit, Citius Tech

### Project Detail
**Market:** Market-HMT2  
**Proficiency:** QA  
**QMS Project Name:** DVF CWOW  
**Practice Name:** Automation QA Practice  
**VeloCT Type:** POC  
**Start Date:** 23/11/2023  
**Number of Lines of Code:** 254  
**Efforts Saved:** 20 minutes

### What It Does
- **Automates the re-execution of failed test scenarios** on Jenkins.
- **Reduces manual intervention** by automatically retrying failed tests.
- **Improves feedback loops** by providing quicker insights into test results.
- **Configurable retry count** to manage the number of times a scenario is retried.

### How It Does It
- **Uses an Extended Cucumber Runner** to automate retries.
- **Custom HTML formatter and JSON filter** to handle reporting and avoid duplicate sections in reports.
- **Configurable retry count** stored in a properties file for flexibility.

### What It Doesn’t Do
- **Does not eliminate the need for initial test execution.**
- **Does not prevent the scenario from failing if it consistently fails beyond the retry limit.**

### How It Runs
1. **Test Cases Execution:** Initially executed by Jenkins.
2. **Retry Mechanism:** Automated retries are triggered based on configurable criteria.
3. **Reporting:** Custom formatter and JSON filters handle report generation and duplicate data filtering.

### Code Files
- **CustomCucumber.java:** Custom runner class inheriting from ExtendedCucumber with an overridden `init` method to manage retry counts.

### Test Data and Setup
- **Test Data:** Required for running the test scenarios.
- **Setup:** Includes configuring Jenkins, setting up the automation framework, and ensuring required environment components are in place.

### Contribute to Fixes/Patches
- **Contributors:** Snehal Bhosle, Sangeeta Palankar, Soham Lohar

### Known Bugs
- **Duplicate JSON Sections:** Addressed by overriding the `done` method in `JsonFormatter` to filter out duplicates.

### Recommendations & Pitfalls
- **Retry Count Configuration:** Set the retry count to a minimum to avoid unnecessary executions. Recommended maximum idle retry count is 3.

---

Feel free to adjust or add any details as needed!
