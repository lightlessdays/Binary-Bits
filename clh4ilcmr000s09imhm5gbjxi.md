---
title: "What is Software Testing?"
datePublished: Mon May 01 2023 07:23:59 GMT+0000 (Coordinated Universal Time)
cuid: clh4ilcmr000s09imhm5gbjxi
slug: what-is-software-testing
canonical: https://github.com/lightlessdays/Software-Testing/blob/main/01.%20What%20is%20Software%20Testing%3F.md
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682925947850/cf154015-f111-4163-b567-861384b459da.png
tags: software-testing

---

Software testing is a process where we **validate** that the product developed is as per the requirement of the client. Software is ensured that it is **defect free**, **safe to use**, and **validated against different metrics**. Software is tested for security, user experience, speed, performance, load capacity, and many other parameters. Software development and software testing both are ongoing processes as every time a new functionality gets added, it is tested for its accuracy.

This article is part of a series on software testing. Explore all articles in this series here: [https://binarybits.hashnode.dev/series/software-testing](https://binarybits.hashnode.dev/series/software-testing)

### Benefits of Software Testing

But why should we do Software Testing? Well... software testing has several benefits. Here are some benefits of software testing:

1. **Accuracy:** Software testing answers all the necessary questions like how much load a server can take, the speed of the site, and the safety of data to define the reliability of the product.
    
2. **Saves cost:** It's a well-known concept in the software development world that the earlier the defect is detected, the cheaper its cost of fixing. Because once that defect goes to the user's end, the damage could cost the company.
    
3. **Saves time:** Software testing **saves time in the long run** as it does not lead the new changes to go to the next stage till has been tested properly but the testing team against all the necessary parameters which ensures a high-quality product is going every next stage.
    
4. **Product quality:** Since the product is tested against the necessary metrics, **product quality improves**. A well-tested product reaches the market.
    
5. **Trust factor:** Software testing builds trust in the company as well as among users. As the product is well tested, the company remains confident in handling any possible outburst. And that confidence gets reflected in their product marketing and hence among users.
    

### Steps of Software Testing

Software Testing can be divided into two steps:

1. **Verification:** Software testing ensures that the product we are building is defect free, and secure, as per the client's requirement and user's expectations. It is tested against all the parameters to deliver a quality product.
    
2. **Validation:** Validation in software testing emphasizes where the product is being built is the right fit for the market. For instance, when Google Glass was built, it was a high-quality product that checked all the technical parameters. But when Google Glass was brought into the industry, it was immediately banned by a lot of governments because of security and privacy obligations. So, Google Glass was a well-verified but not validated product.
    

Let us tabulate the differences between verification and validation to properly understand the difference between them.

| **Verification** | **Validation** |
| --- | --- |
| Verification focuses on building a technically sound product. | Validation focuses on building the right product for the market. |
| Verification is done on all the technical parameters like performance, load, and security. | Validation focuses on market size, pricing of products, industry requirements, use cases, etc. |
| Verification can only be done by the testing team. | Validation is done mainly by the Business Analyst team. |
| Verification is done after a feature is developed. | Validation is done before a feature goes into development. |

### Principles of Software Testing

Software Testing is guided by seven principles. These seven principles, known as the principles of Software Testing, are listed below:

1. **Testing shows the presence of defects:**
    
    One important aspect of testing is that it shows the presence of a defect and not the absence of it. The purpose of testing is not to ensure that the product is 100% bug-free but to work hard, finding creative ways to locate a bug in the software. It's not about writing 1000 test cases that are passed, but writing those 10 cases which are more likely to fail.
    
2. **Exhaustive Testing is not possible:**
    
    Before testing any application, one thing to remember is that you cannot test every test case scenario. Neither manually nor automate it. The reason for the same would be add-on cost on time and budget. Also, it's not even feasible to replicate the exact and every possible test environment. Hence, testing is done on a priority basis. And that's one of the reasons why every bug is given priority and severity.
    
3. **Early Testing**
    
    Currently, in the industry, Agile methodology is used instead of waterfall. Agile signifies testing, and development is a parallel process. It's a well-known fact that the earlier the bug is predicted, the cheaper its cost is to fix. And with time, cost increases exponentially. Suppose the code is in the development stage. The damage a bug would do can still get controlled. But the same bug, when it reaches production, can cost millions. So, the earlier the testing better it is.
    
4. **Defect Clustering**
    
    Clustering means grouping. It's an observed phenomenon that only a few modules carry the most amount of bugs. And usually, the ones that have the main integration going on. And the reason is also when testing is done via lack of creativity. Manual testing is a skill set developed over the years and helps to identify those risky modules.
    
5. **Pesticide Paradox**
    
    In the agriculture field, when the same pesticide is used over a decent duration. Insects develop resistance to the pesticide and get unaffected. The same lies with software testing. When the same techniques, strategies, and tools are used for every functionality, crucial bugs remain in the software. And software testing is a skill where regular upskilling is a necessity. Even the tools that come up are based on the limitations of previous tools. Continuous upgrade with technology is a necessity to survive in the testing industry.
    
6. **Testing is context-dependent**
    
    Testing is context-dependent, meaning the same testing strategy cannot be used within the same product or even for different functionalities in the same product. For instance, the thought process for testing UI is more validation centric, whereas an API is more security-centric. Testing strategy changes with the technology also. Testing a website on ReactJs and Angular would involve different performance metrics. And when testing any e-commerce site, security and payment become huge risks and priority factors.
    
7. **Absence of errors fallacy**
    
    The absence of errors fallacy comes from the concept of verification and validation. Software tested with multiple rounds of testing and proven to be 99% defect free can still not be validated in the market. For example, highly advanced drones for surveillance and testing to give accurate results still be not allowed by the government for privacy concerns. So, the goal is not only to create a bug-free product but also a usable one.
    

### Software Testing Tools

Software testing tools have made automation testing possible. We integrate these Software Testing Tools into the script, and they run the test case. Based on the result, a report is attached to them.

For example, the Selenium automation tool is used to automate the browser. We write a script in Java/Python/javascript called the Selenium web driver using Selenium libraries, and with the help of libraries only, we automate the webpage. Once the execution is done, an extensive report is attached to it. The entire run is done on the testNG library.

But there are also tools like Bugzilla, and Jira, which do not help automate a test case but act as bug management. Jenkins, for instance, is used as CI/CD tool. So all these in a single automation framework work in collaboration. Below, we are going to list the different types of Software Testing Tools we have.

#### Types of tools

There are eight kinds of software testing tools:

1. **UI automation tool:** UI automation software testing tools are used to automate the user experience with the application. Scripts are written by clicking a button, filling out the form, scroll down the screen. Selenium has been the most used in the industry for many years now. Cypress is for javascript developers, and Katalon Studio is built on top of Selenium to provide a GUI interface for UI automation.
    
2. **API automation tool:** API automation software testing tools like Postman, RestAssured, and SoapUI are used to test web services and API. These tools don't require much coding, but one can validate if an API is working and if requests and responses attach to it.
    
3. **Performance tool:** Performance software testing tools like LoadRunner and Apache Jmeter test the server's load. You can send multiple requests to the server, and within a few seconds, a response time graph is obtained—for both load and stress testing.
    
4. **Test case management:** Test management tools like JIRA with XRays automate the test case management process. Earlier the entire entry was done manually in Excel sheets. Now JIRA can be integrated into source code and generate reports of test cases pending.
    
5. **Bug management tool:** Bugzilla is a popular tool that helps identify a bug's status. Who is assigned to it, severity, and priority of the bug? Earlier, this was all done in an Excel sheet which was challenging to manage.
    
6. **Mobile automation tool:** Appium is used to automate mobile experience. The same Selenium does with browsers, Appium does with mobile automation. Tester writes a script and adds Appium libraries which replicate user interaction of click, scroll, volume, etc., features.
    
7. **Build automation tool:** Jenkins is one of the most used tools. It is a CI/CD tool that is used to automate the build so that a tester can schedule the test execution time. The build would automatically run, and the associated report would be generated.
    
8. **Test Environment tools:** LambdaTest, SauceLabs, and BrowserStack provide test environments that allow testers to run their code on desired system configuration.
    

Let us now explore some famous tools that every tester must know, starting with Selenium.

#### Selenium

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682924951938/febbb385-c3d0-4e23-9e59-fce7a4353243.png align="center")

Selenium is an open-source tool used for browser automation. It supports multiple languages like Ruby, Java, Python, and C#.

Three selenium tools are available: selenium web driver, selenium grid, and Selenium IDE. Selenium grid is used for cross-platform testing, and Selenium IDE is a code-less tool that records the script based on user interaction with the site.

To get started with the selenium web driver, you need to install selenium libraries in your project, and then you can call its methods for various keyboard and mouse actions.

Some important selenium features:

1. Selenium is a free and open-source tool
    
2. It supports multiple programming languages like Java, Python, C#, etc.
    
3. It has three tools- Selenium web driver, Selenium grid, Selenium IDE
    
4. Selenium webDriver is used for automating browsers in the same platform.
    
5. Selenium Grid is used for automating browsers in cross-platform, i.e., different systems using a hub and node concept
    
6. Selenium IDE is for codeless automation. It generates a script by recording user actions on the website.
    
7. Selenium supports multiple web drivers like Chrome, Edge, Firefox, etc.
    

#### Appium

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682924988324/b867f5a4-dd4f-4e6a-b601-159871eb2054.png align="center")

Appium is an open-source tool used to automate native, hybrid, or mobile web applications. It uses the webDriver protocol. It supports multiple programming languages.

To start the Appium, you need to install the node.js server. It runs in the background. Appium is integrable with emulators for a better testing experience. It also helps in automating the backend.

Some important Appium features:

1. Appium requires a node.js server
    
2. Appium supports multiple languages like Python, C#, and Java.
    
3. Appium is an open-source tool
    
4. Appium contains a UI Automator for logging experience.
    
5. Appium is easily integrable with TestNG, which is a unit testing framework in Java
    
6. Appium can be used with emulators for enhanced user testing experience
    
7. Appium supports cross-platform compatibility, enabling the same test to run on multiple platforms.
    

#### Cypress

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682925086939/19a64e28-e2cd-408e-8bc0-d9118dae9043.png align="center")

Cypress's popularity has increased in the last few years. Cypress is javascript based web automation tool. Cypress is open source tool.

It enables developers and testers to write test cases in javascript, which is the native language to build any website. Cypress is quite different from Selenium. It takes snapshots as you run the test cases.

Some important Cypress features:

1. Cypress is an open-source tool.
    
2. Cypress is javascript based end to end framework tool
    
3. Both developers and testers use Cypress as it is written for javascript developers
    
4. Cypress reloads whenever a change is made to a test case
    
5. Cypress takes snapshots when the test cases are getting executed.
    
6. Cypress overcomes Selenium's most significant weakness for waits and async nature.
    
7. Cypress provides easy debugging by direct integration from browser dev tools.
    

#### Katalan Studio

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682925148802/e208d032-3b5a-471d-9365-e9c9ea769158.png align="center")

Katalon Studio automates both **website and mobile applications**. Katalon aims for a more codeless automation strategy. It is used for web and API automation.

Some important Katalon studio features:

1. Katalon Studio automates web base, mobile-based, and desktop-based application
    
2. It is compatible with multiple OSs and browsers
    
3. It provides codeless automation support for beginners.
    
4. Katalon Studio also supports script writing for advanced developers.
    
5. It supports integration with CI/CD tools like Jenkins and Azure.
    
6. Katalon supports Selenium scripts which can easily be imported into the platform.
    
7. It is supported in multiple testing environments like LambdaTest, Docker, etc.
    

#### Postman

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682925271555/b1ed8dcc-5d21-4658-ad6a-3e7bac88e17f.png align="center")

Postman is a widely used API test tool that is equally popular among developers and testers. It is a **s**tandalone desktop application that is entirely GUI.

The tester can send requests to a server and attach multiple headers based on the protocol. The tool would return the response.

The tester can even write scripts in the test section to validate if the response is correct or not.

Some important Postman tool features:

1. Postman is a standalone desktop tool used for API automation.
    
2. Testers send a request to the server, and a formatted response is displayed in the tool.
    
3. Testers can attach test cases to validate if the result is correct or not.
    
4. Postman supports **continuous integration** with other applications as well.
    
5. Postman is integrable with Newman or Collection Runner to execute test cases.
    
6. In Postman, one can import/export environment and collection making it even simple to use.
    
7. Postman can be used with SOAP, REST, and HTTP.
    

#### Jira Software

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682925394224/7daaecac-e8ef-415d-9cb9-c53637bc63ee.png align="center")

Jira is a product management and bug-tracking tool by Atlassian. It supports both Scrum and Kanban frameworks. It is used by almost every company for a smooth and transparent software development process. It generates graphs, boards, and sprints. Users are here referred to as Components. Some JIRA terminologies include epic, user story, bugs, releases, etc.

Some important Jira features:

1. Jira is a product management and bug-tracking tool by Atlassian.
    
2. Jira uses Agile frameworks Scrum and Kanban.
    
3. Jira promotes transparency in the team to keep track of the updates. It has replaced Excel sheets.
    
4. Jira can also be used for test cases by **XRay plugin integration**.
    
5. Jira generates Word and Excel reports. Data can also be imported into Jira.
    
6. Jira can be integrable with tools like BitBucket, Jenkins, etc.
    
7. Jira also provides customizable workflows and extended graph reports to meet deadlines.
    

#### SoapUI

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682925511382/8b88ee62-5945-4960-a633-fadbaaa82c01.png align="center")

SoapUI is an API automation tool that tests API based on SOAP, REST, and GraphQL. SoapUI is easily integrable with CI/CD tools. Using SoapUI, the tester can do API functional testing, API performance testing, and API security testing. SoapUI also supports data-driven testing and test reporting.

Some important SoapUI features:

1. SoapUI is used for API test automation.
    
2. It supports testing all sorts of APIs-SOAP, Rest and GraphQL
    
3. SoapUI supports **CI/CD integration**.
    
4. SoapUI supports API functional testing, i.e., APIs work when the required conditions are met.
    
5. SoapUI supports API performance testing, i.e., how much load the API can take in.
    
6. SoapUI supports API security testing, i.e., to test any vulnerability that might have been left out.
    
7. SoapUI has support for both data-driven testing and test reporting.
    

#### Apache JMeter

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682925601343/f8caa033-05be-49a3-b826-f9ccb18eb5f2.png align="center")

Apache Jmeter is an open-source tool made on JAVA for load testing and application performance testing. It can test **S**OAP, REST APIs, and web services. The best part of the tool is that it generates extensive reports. The tool is made on the multi-threading concept of JAVA.

Some important Jmeter features:

1. Apache Jmeter is an open-source tool
    
2. Apache Jmeter is used for load testing for APIs and Webservices
    
3. Apache Jmeter supports REST, SOAP, and web services.
    
4. Jmeter is a standalone application that is built on JAVA.
    
5. Jmeter is used for Distributed Testing, Recording Tests, JUnit sampler
    
6. Jmeter is compatible with Gradle, Maven, and Jenkins.
    
7. Data analysis and visualization plugins show comprehensive reports.
    

There are other famous software testing applications as well such as LoadRunner, LambdaTest, SauceLabs and RESTAssured, but we will not be discussing each one of them. The Software Testing industry is not limited to these softwares and new softwares keep coming in every then and now.