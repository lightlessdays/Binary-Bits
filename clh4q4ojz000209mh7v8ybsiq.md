---
title: "Software Testing Lifecycle (STLC)"
datePublished: Mon May 01 2023 10:54:58 GMT+0000 (Coordinated Universal Time)
cuid: clh4q4ojz000209mh7v8ybsiq
slug: software-testing-lifecycle-stlc
canonical: https://github.com/lightlessdays/Software-Testing/blob/main/02.%20Software%20Testing%20Lifecycle.md
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682938480773/a40b3df0-c6c0-446f-a6bc-d6b3a0b484da.png
tags: software-testing

---

The software testing life cycle is a process of testing an application that goes through sequential phases. Each phase has a distinctive role to play and should be handled separately. After one phase of STLC is done, only move to another phase in the testing cycle.

This article is part of our series on Software Testing. Read the entire series here: [https://binarybits.hashnode.dev/series/software-testing](https://binarybits.hashnode.dev/series/software-testing).

![3 Ways to Accelerate Your Software Testing Life Cycle](https://www.codium.ai/wp-content/uploads/2023/03/post-866-1.jpg align="center")

## Characteristics of STLC

1. STLC is a testing process part of the software development life cycle.
    
2. The STLC process remains the same irrespective of the SDLC methodology used.
    
3. In STLC, once the first phase is done, only the tester moves to the next phase of the process.
    

## STLC Phases

![Software Testing Life Cycle (STLC) - GeeksforGeeks](https://media.geeksforgeeks.org/wp-content/uploads/20190510015920/ppp10.png align="center")

#### **Requirement Analysis**

Requirement analysis is the first step in STLC where the product manager and test lead understand the requirement. All points are noted and maintained in the document. Getting the requirement right is extremely crucial as it would lay down the foundation for the rest of the process.

#### **Test Planning**

In the Test planning phase, the entire STLC process is planned out. How long would the testing cycle be, how much would be automated vs how much would be manually tested, what tools are required, and if staff needs to be trained and create RTM(requirement traceability matrix). The lead takes all these important decisions based on them, and tasks are allocated to senior QA and QA members.

#### **Test Case Development**

The first step is to lay down the test framework—the tools required like Selenium, maven, log4j, reports, etc. Then, manual test cases and automated test cases are written. The goal is to automate repeated test cases, and all the creative, exploratory, and random test cases are manually tested.

#### **Test Environment Setup**

Because of SauceLabs, and BrowserStack, the test environment can be easily created virtually. Test environments for multiple combinations of the operating system, browser, and processors can be created, allowing further testing accuracy to expand further. When these options were unavailable, setting up the environment was a costly affair.

#### **Test Execution**

Test execution signifies running the test cases, generating the report, if a bug is found, then assigning the bug to the developer and resolving it. Regression testing to ensure previous code is still working and retesting to ensure the system is bug-free.

#### **Test Cycle Closure**

The test cycle needs to close at the right time as lots of resources are involved, and the code needs to reach the production stage. The closure is where we have a definite idea of the extent of testing done, both functional and non-functional.

### Entry and Exit Criteria

Entry criteria signify the prerequisite one should have before entering the phase, and exit criteria denote after what criteria we can say the phase has ended. Let's have a look in detail below.

| **Phase** | Entry Criteria | **Activity** | Exit Criteria |
| --- | --- | --- | --- |
| Requirement Analysis | Requirement document prepared by the manager which is signed by both client and manager. | Understand the client's requirements and prepare the Requirement Traceability Matrix(RTM) | All functional and non-function requirements are noted and both parties have agreed to the terms. |
| Test planning | All functional and non-functional requirements of the product are known. | Making decisions like The entire STLC How much to process had been automated, tool planned out with requires, training overview of what and needs for the staff, how much the duration of the test cycle | The entire SDLC process has been planned with an overview of how much to automate. |
| Test Case Development | The entire road map to STLC has been laid out. | Test cases are written both manually and in automation. In the case of automation, a framework has been created so that the testing process is more manageable. | All manual and automation test cases are created. In the case of automation, a framework is laid out. |
| Test Environment Setup | All test cases have been written and there is a clear picture of what to automate. | Setting up the test environment on the server or using Sauce Labs and BrowserStack features. | Once the test environment is setup which is reliable and has high test case coverage |
| Test Execution | The test environment is set up. The test environment could be a server or a paid service provider application. | Test cases are executed, reports are prepared and bugs found are assigned. Bugs are resolved and the application is retested. | All bugs are resolved and a detailed report is generated |
| Test cycle closure | Reports are prepared and the application is bug-free. | STLC cycle is closed and the product reaches the production stage. | Bugs are resolved. The application has gone through retesting and regression testing. |

## Requirement Traceability Matrix

The Requirement Traceability Matrix (RTM) is a document prepared by the test manager to map the requirements listed by the client to that of test cases that would run against them. It is a many-to-many document prepared on an Excel sheet. It indicates the extent of testing on every functionality to ensure quality in time and budget constraints.

### Importance of RTM

RTM is important because of the following reasons:

1. RTM acts as a tracker to know which functionalities have been tested and which are pending for both the development and testing teams.
    
2. Preparing RTM is crucial for the next step in STLC, test planning. Based on RTM, the entire test architecture is laid down.
    
3. RTM contains the current states of test cases, i.e., which have been passed, failed, and pending.
    
4. RTM ensures all functionalities have been tested and nothing is left. Updating this document ensures that.
    

### Parameters in RTM

Following are the pointers that are mentioned in the RTM.

1. Information about Requirement, i.e., Req Id, Req Description,
    
2. Test case mapping Test Scenario, Test Case Id, Test Case Description, and Test status. Only mapping of test cases is done here.
    
3. Defects are also mapped using Defect Id and Defect status.
    
4. Lastly, the Requirement Coverage status is mentioned here. The terminology here is Partial, Complete, and None.
    

### Types of Traceability Test Matrix

A traceability test matrix can be created for three primary purposes:

* **Forward traceability:** This ensures that all requirements have been mapped to test cases in RTM. That is, test case coverage is the primary concern. It keeps track of test cases, what is the current status, and if there are any bugs.
    
* **Backward or reverse traceability:** RTM can also be used to ensure no unnecessary code. All test cases have been covered, and the requirement is satisfied, but the developer has added more cases. Then that aspect can also be a useful feature in reverse traceability.
    
* **Bi-directional traceability:** RTM document created to ensure all test cases are covered and no unnecessary code added to ensure the SDLC cycle is going in the correct path is bi-directional traceability.
    

### Creating a Requirement Traceability Matrix

**Step 1:** Map the Requirements in an Excel document. There is already a separate document for a requirement where the absolute requirement is listed in detail.

**Step 2:** Map the test cases to requirements. Again, only the test case is attached to the requirement. We don't write detailed test case columns like steps, expected results, etc.

**Step 3:** Map defects to the test cases. The only objective here is to know the defect's status to that of the requirement to keep a tracker.

**Step 4:** Requirement coverage status is updated after test planning is done. It is further updated after the test execution stage.

### Advantages of RTM

1. It ensures the maximum test coverage possible.
    
2. It acts as a tracker for the testing team. The status of test execution and bugs.
    
3. RTM also keeps a tracker for bug management. Bugs are pending, and hence, keep the development team involved.
    
4. RTM is necessary to ensure the development cycle is on track and helps minimize time and effort where ever possible.
    

## Test Planning

The test plan in software testing is a testing document prepared by the test manager and test lead before starting the testing process. They already have understood the requirements of the client. In this document, they lay down the roadmap for the entire testing cycle. Test scenarios, test coverage, how much would be manually tested, which parts to automate, tools required for automation, the budget of the entire cycle, duration, and calculating if there are any training needs for the employees in the project.

### Why is Test Planning Important?

1. A test plan in software testing is a well-formed document that would be referred to at various stages of testing to keep everyone on track.
    
2. It acts as a schedule to refer to.
    
3. In case of any contradiction as to why a particular tool is used over the other, everything is measured.
    
4. It keeps the client informed about the efforts to produce a quality product.
    
5. It is a guide for the next stage of test case development.
    
6. Test plans are used to write sprints for AGILE methodology in JIRA.
    
7. It helps in predicting the time vs. effort ratio. And in case of delay, how much cost would add to the product?
    

### Guidelines for Test Planning

1. Prepare a new document for every product.
    
2. Keep the test plan updated based on the latest technologies, changes in the tool's price, etc.
    
3. The document should be well-structured and point-wise.
    
4. It should indicate who is supposed to do what task.
    
5. It should be converted into sprint format in test case management systems.
    

### Types of Test Plans

There are three types of test plans:

1. **Master Test Plan:** This includes the overall plan, roadmap, and software testing life cycle outline.
    
2. **Phase Test Plan:** A test plan gets converted to a sprint. Here the focus is on one sprint at a time.
    
3. **Specific Test Plan:** This test plan is around a particular test case scenario or tool. It has details of that one functionality and how it should be tested.
    

### How to Write a Test Plan?

While preparing the test plan document, some test attributes need to be defined, which are as follows:

**1\. Objective:** First and foremost, what is the objective of the entire test plan? How much quality in the given time company is aiming at? The extent of testing, duration, which components would emphasize more, and the direction of the entire cycle are listed here.

**2\. Test Strategy:** The test strategy discusses which components would be tested in-depth versus which would be superficially tested. The strategy is designed to optimize the resources, minimize the cost, and have a clear direction for the effort. There are also scopes mentioned which are below:

**In-Scope:** The components which would be tested in-depth **Out Scope:** The components where effort in testing would be minimum

**3\. Testing Methodology:** The testing methodology mentions how much would be manually tested, how much would be automated, and the tools and technologies that would be used. Testing methodology is also based on the requirements and objectives of the entire testing cycle.

**4\. Approach:** The approach discusses the priority components that must be dealt with. The components should be tested first, then the ones which follow. It also has two parts: High-Level Scenarios: Here, which component would be tested, like login, payment, etc? The Flow Graph: It talks about the flow of testing as in login. Also, first direct login would be tested, then Gmail, Facebook authentication, etc.

**5\. Assumptions:** In this phase, assumptions are declared, which are as follows:

* Every tester is trained in using the tool
    
* Tester has a clear understanding of the project and requirements
    
* There would be continuous support from the development team.
    

**6\. Risk:** The risk associated with the project are also listed so that everyone is on the same page. Examples of the risk are listed below:

* If the testing duration increases by a certain time, the impact on the budget.
    
* If a tester leaves the company during the testing period, it impacts the company.
    
* If the product has some untested bugs, then risk to the client's company.
    

**7\. Backup/Mitigation Plan:** In case any risk associated comes true, then the test plan document also lists backup options like:

* If there is a delay in payment by the client, then how to go about it
    
* If an XYZ employee leaves or falls sick, then who would handle it
    
* If there are new functionalities, introduce how they should be adjusted in the project
    

**8\. Roles and Responsibilities:** All the responsibilities of every person in testing are listed. Team lead, managers, senior QA, QA. **Examples:** XYZ employee: UI testing using Selenium would cover login, payment, and blog integration functionalities. PQR employee: API testing using SoapUI would cover the landing page, comments, payment, and login functionalities.

**9\. Scheduling:** The entire cycle would be divided into sprints with the start and end dates. And by that time, all functionalities that should be tested would be listed.

**10\. Defect Tracking:** All the actions that need to be taken in case a defect is found are listed here. Example: JIRA tool would be used, the manager would be XYZ, the screenshot must be attached, the developer should be mapped, and priority and severity should be written.

**11\. Test Environment:** All the hardware, software, and cloud requirements are written here. Nowadays, BrowserStack and Sauce Labs provide hardware as a service so that you can pay per use model for the utilization of resources. One doesn't physically require a system of a particular configuration. **Example:** software requirement of JDK-15, Selenium 4, Maven, TestNG hardware requirement of Windows 10, macOS, 16GB RAM, etc.

**12\. Entry and Exit Criteria:** Criteria laid by the team as to when testing should start and end. Clear guidelines on it are mentioned here.  
**Entry Condition:**

* The test environment should be setup
    
* Development must be done
    
* The requirement document must be ready
    

**Exit Condition:**

* All bugs are fixed
    
* The code is ready for production
    
* RTM has been updated
    

**13\. Test Automation:** All the test cases that will be automated are mentioned here. The general criteria are:

* Redundant test scenarios in bulk must be automated
    
* Test cases requiring precision must be automated
    
* A test case that reduces labour must be automated
    

**14\. Deliverables:** These consist of all the testing documents given to the client. It consists of a Test plan, test report, and bug report, all the sprint updates, and effort done during the testing are recorded.

**15\. Templated:** A template with all the headings mentioned needs to be prepared for every testing team member during test execution.

## Test Execution

After test planning, a framework is created to run automated test cases. Execution of both manual test cases and automated test cases, generation of reports, and identification of bugs is called test execution. This is the main step, as here the test cases run. If any bug is there, then after the bugs get fixed, test cases are executed again for quality assurance. An important aspect of test execution is documentation also. The document has a definite structure that has been followed in the industry for many years.

### Test Execution Guidelines

The following are important aspects of test execution that need to be understood before running test cases:

1. **Build:** Build is standalone software. A source code is converted into a build that is deployed on the test environment, and the build is what is tested for bugs and quality assurance.
    
2. **Test Environment:** There is a dedicated server for testing purposes. After the application is tested, it gets deployed to another server for production usage. Nowadays, Saucelabs and Browserstack provide these test environments as a service model. I could use macOS, chrome version 104 as a service instead of having the hardware available.
    
3. **Test Team Size:** Test team size is dynamic. The initial project is on test lead, then QA and senior QA are assigned tasks by the lead. The team size keeps changing based on company projects and deadlines.
    
4. **Test Cycles:** The testing process also happens in a cycle. During the initial phase, the product is tested to ensure that functionalities are working and no other bugs are left. In the next cycle, the system is retested for exploratory testing and finding deeper bugs.
    
5. **Test Execution Phase:** Test execution consists of test scripts, maintenance, and bug reporting. After the test, the environment is set up, and the build is deployed.
    
6. **Smoke and Sanity test cases:** When carried out on the build, the testing process comes under smoke and sanity testing. Sanity testing is done to ensure that functionalities are working in the build, and smoke ensures that all the bugs have been fixed in the build deployed.
    
7. **Defect Reporting:** The bug life cycle is an important aspect of test execution. Bugs found are reported and maintained in a separate document. Nowadays, we use Bugzilla and JIRA for bug report management. Defect reporting is talked about in depth below.
    

### States of Test Execution

Some important test execution states/results have a definite meaning to them.

* **Pass:** test case is executed, and the expected result is the same.
    
* **Fail:** test case is executed, and the expected result is not the same.
    
* **Inconclusive:** test case is executed, and there is no clear result.
    
* **Block:** test case cannot be executed because one of the test case preconditions is not met.
    
* **Deferred:** test case is not executed yet and will run in the future.
    
* **In progress:** test case is currently running.
    
* **Not run:** test case has not been executed yet.
    

### Bug Lifecycle

![Bug Life Cycle in Software Development - GeeksforGeeks](https://media.geeksforgeeks.org/wp-content/uploads/20200812151113/buglifecycle.png align="center")

Once a bug is reported, it goes through various stages of assignment and reporting, and then only ultimately, it is fixed, termed as a bug life cycle. The diagram below explains the various stages, but first, let's discuss these bugs' terminologies of status.

#### Bug State

A bug in its cycle goes through various states, as below.

* **New:** Every time a new bug is discovered, its status is new.
    
* **Assigned:** When a bug gets assigned to the developer, its status changes to assigned.
    
* **Open:** When the developer is working on the bug, and it has not been fixed yet, its status is changed to open.
    
* **Fixed:** When the developer completes the development changes and is resolved from the developer's end.
    
* **Pending retest:** After the bug is fixed, it is sent to the testing team to close it. During this transition, its status is pending a retest.
    
* **Retest:** During the retesting phase, its status is changed to retest, as the tester tests the code again to verify if the issue has been fixed or not.
    
* **Verified:** Once the bug has been fixed, the testing team validates that the bug status is changed to verified.
    
* **Reopen:** In case of retesting, the testing team is not satisfied, and the status of the bug is changed to reopen.
    
* **Closed:** A bug can only be closed by the one who raised it, so in case if client raised the bug and is satisfied, the status is changed to closed.
    
* **Duplicate:** Suppose the same bug is affecting two functionality, and the testing team has written two bugs, so one of them would become a duplicate.
    
* **Rejected:** If the development team feels that the bug raised by testing is not a defect, then the bug status is rejected.
    
* **Deferred:** Deferred means that the development team is aware of the bugs but will fix them in the next product release cycle.
    
* **Not a bug:** If some features do not affect the core functionality, then they are termed as not a bug.
    

#### Bug Cycle

1. During the test execution phase of the testing cycle, if a bug is discovered, the status of the bug is assigned as New
    
2. Then, the developer assigns the bug to make changes in the code and fix the defect. The status here is Assigned.
    
3. The developer would make changes in the code, and when the developer validates it's been fixed from his end, the status will change to fix.
    
4. The fixed bug would go to the testing team for retesting and would be validated if it is fixed or not. The status of the bug here is retesting.
    
5. If the testing team is satisfied with the changes made by the developer, the bug will be verified.
    
6. But, if the testing team still finds some issues left in the code, then that bug would reopen to go through the entire bug cycle again.
    
7. Now, the bug can only be closed by the person who has opened it. Suppose a client has opened the bug, then after the client validates his satisfaction, the bug would be closed.
    
8. During the cycle, if the development team denies that the bug mentioned is not a bug but a definite feature, then that bug is rejected by the development team.
    

#### Defect (Bug) Priority and Severity

* **Defect Severity** signifies the impact of the bug on the application. It's important to categorize the bug's impact so that the development team knows how severe the issue in their code is. Severity is High, Medium, and Low.
    
* **Defect Priority** is a ranking mechanism to tell a developer that if multiple bugs have been allocated to him, which one should deal with first? Priorities are mentioned in the order: Critical, Major, Moderate, and Minor.
    

## Test Metrics

A software testing metric indicates the degree to which a process, component, or tool is efficient. Here we have a quantitative measure of the effectiveness of an approach. Let's say we automated certain test cases and we have 50% test coverage using tool A. Next time the tool was changed and manual testing was also used so test coverage was 66%. Now we have solid data to justify why manual testing in combination with automation would be better to test the product.

### Importance of Test Metrics

1. Software testing metrics are used to increase the overall productivity of the development process.
    
2. It helps to make more informed choices about the tools and technologies being used.
    
3. It helps to identify unique ways and techniques that are beneficial for their system, hence increasing performance.
    
4. Software testing metrics determine the health of a process, tool, and approach used.
    

### Types of Software Testing Metrics

There are three types of software testing metrics:

1. **Process Metrics:** The quantitative measures that define the efficiency of a process based on parameters like speed, time, utilization of resources, etc. Managers can look at these numbers and set new guidelines for the phase.
    
2. **Product Metrics:** Measures to determine the quality, size, performance, and efficiency of the product come under product metrics.
    
3. **Project Metrics:** Quality and productivity of the project, utilization of resources, cost, and time come under the project metrics.
    

### Manual Test Metrics

Since manual testing is a step-by-step testing process carried out by a quality analyst, finding quantitative measures in the process are little different. These metrics are manual test metrics. There are two types of manual test metrics:

1. **Base Metrics:** The essential data taken out via the carrying testing process comes under base metrics. It comprises test cases and test cases completed.
    
2. **Calculated Metrics:** The base metrics data is further taken out to carry differential results that provide more information about the process or product. It is more useful for tracking project progress.
    

Some other metrics:

* **Defect metrics:** The measures telling about defect ratio, speed taken to fix a defect, and complexity of a defect come under defect metrics.
    
* **Schedule Adherence:** Schedule Adherence tells the expected time given for a task vs the time taken to complete it.
    
* **Defect Severity:** Defect severity talks about how much the impact that defect/bug has on the product.
    
* **Test case efficiency:** Test case efficiency covers how well a test case can determine the impact of a test case.
    
* **Defects finding rate:** It tells what is the pattern of flaws over some time.
    
* **Defect Fixing Time:** The time difference between when the defect was assigned vs when it got fixed.
    
* **Test Coverage:** How much of the requirements and functionalities are covered in the testing process comes under test coverage.
    
* **Defect cause:** The modules or components causing the defect.
    

### Test Metrics - Formulas

1. **Test Case Effectiveness:** Test Case Effectiveness = (Total defects detected / Total number of test cases) x 100
    
2. **Passed Test Cases Percentage:** Passed Test Cases Percentage = (Total number of tests passed / Total number of test cases) x 100
    
3. **Failed Test Cases Percentage:** Failed Test Cases Percentage = (Total number of test cases failed / Total number of tests executed) x 100
    
4. **Blocked Test Cases Percentage:** Blocked Test Cases Percentage = (Number of blocked/skipped tests / Total number of test cases) x 100
    
5. **Fixed Defects Percentage:** Fixed Defects Percentage = (Total number of defects fixed / Total number of defects) x 100
    
6. **Rework Effort Ratio:** Rework Effort Ratio = (Rework efforts spent in that phase/ Total efforts spent in that phase) x 100
    
7. **Accepted Defects Percentage:** Accepted Defects Percentage = (Defects Accepted by Development Team / Total number of Defects Reported) x 100
    
8. **Defects Deferred Percentage:** Deferred means that we know that there is a bug but would fix that bug in the next release Defects Deferred Percentage = (Defects deferred / Total number of Defects Reported) x 100
    

### Metrics Lifecycle

1. **Analysis:** The QA team identifies the metrics like time, effort, efficiency, etc.
    
2. **Communicate:** Communication among the testing team as to how to capture the metrics, the process of it, and what all data needs to be extracted.
    
3. **Evaluation:** All the calculation of the data happens here. Preparation of these metrics is done.
    
4. **Report:** These metrics are reported. Data is compared, and loopholes and analysis of the report are done. Measures to improve are discussed so that next time the process would be more effective.
    

This was all about STLC. Thanks for reading :)