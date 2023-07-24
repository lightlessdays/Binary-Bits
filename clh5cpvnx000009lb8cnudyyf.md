---
title: "Different Types of Testing"
datePublished: Mon May 01 2023 21:27:19 GMT+0000 (Coordinated Universal Time)
cuid: clh5cpvnx000009lb8cnudyyf
slug: different-types-of-testing
canonical: https://github.com/lightlessdays/Software-Testing/blob/main/05.%20Different%20Types%20of%20Testing.md
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682976404998/ff55f168-c480-4336-a629-fb6e4b5bc117.png
tags: software-testing

---

In this article and the next article, we will be looking at different types of software testing in the industry. This article is part of a series on software testing. Check out the entire series here: [https://binarybits.hashnode.dev/series/software-testing](https://binarybits.hashnode.dev/series/software-testing)

### Functional Testing

As the name suggests, functional testing tests the application against functional requirements and specifications. Functional requirements are the list of features specified by the client that needs to be added to the product. The specifications include UI, API, and database. For example, the client asked for an authentication system that needs to have Gmail, Facebook, and Regular signup. Testing all that scenarios for user interaction, backend operations, and core functionality.

**Types of Functional Testing**

1. Unit Testing
    
2. Integration Testing
    
3. System Testing
    
4. Regression Testing
    
5. Database Testing
    

### Non Functional Testing

Non-functional testing tests the application's behaviour, aspects like performance, stress, load, and volume of the server. These are all quantitative measures. These are not part of the features a user can see but more about the reliability factor of the application. For example, a user might not be able to know that a given instance site is capable of handling 100K users. This is not a feature for a site user but an essential product aspect. Functional and non-functional testing hence are very different from each other.

**Types of Non-Functional Testing**

1. Performance Testing
    
2. Load Testing
    
3. Stress Testing
    
4. Volume Testing
    
5. Scalability Testing
    

### Functional versus Non-Functional Testing

| Functional Testing | Non Functional Testing |
| --- | --- |
| It validates the features of the product | It validates the behaviour aspect of the product |
| Ensure the listed functionality of the application is working | Ensure Speed, Performance, and Usability factors are working |
| Exploratory and manual testing coverage is there | Non-functional testing cannot be done manually |
| Repetitive and Redundant test cases are automated | All non-functional requirements are automated |
| Testing login functionality of application through manual and automated test cases | Testing performance and load of the site using Apache Jmeter tool |

### Blackbox Testing

A black box signifies an object where one has no idea what is inside it. Black box testing methodology is also based on it, and where a tester writes test cases not considering how the code works but rather the functionality, he wants to test. For example, a tester wants to test the authentication system of a website. The tester tries with the wrong credentials and the correct credentials. If he is getting the correct response from the API. The authentication functionality is working correctly.

#### How to do Blackbox Testing?

* The requirements listed by the clients are understood. The exact functionalities he wants are noted.
    
* The test Cycle is planned from tools selection, test case execution, and bug reporting.
    
* The testing phase is planned. Which is the combination of both automated and manual test cases.
    
* Black box testing is all about running test cases by validating the output.
    
* If the expected output matches, the test case is passed else, the test case is failed.
    
* Failed test cases are reported as bugs and go through a bug cycle.
    

#### Techniques Used in BlackBox Testing

* **Equivalence Class Testing:** We all know that we can't provide every input test data. Hence, test data are divided into sub-categories where one test data from each represent the given scenario.
    
* **Boundary Value Testing:** When test case input data is at the edges of a condition. For example, we want to test a login form functionality where the password should be between 8 to 13 characters. Test data input for passwords with 7 characters, 8 characters, and 13 characters would be at the edge-changing interval.
    
* **Decision Table Testing:** Decision table testing ensures all possible combinations of test case scenarios are covered, i.e. when both username and password are correct, when either of them is correct, and when none is correct.
    
* **State Transition Testing:** Here, we write test cases when the state/ condition in the code is changing. For instance, if you are trying to provide a pin in UPI application like GPay, you are granted three attempts, and on the 4th attempt, the application locks down. Test cases would look like the below:
    
* **Orthogonal Array Testing:** OAT is a quantitative approach when input test data is huge. It helps to maximize test coverage by pairing test case scenarios. For example, there are three sections in a webpage-top, middle, and bottom. And each has an option for text to be shown or hidden.
    

#### Advantages of Blackbox Testing

1. Black box testing technique requires less knowledge of coding.
    
2. Black box testing is much faster than white box testing.
    
3. Black box testing allows random and exploratory testing as mostly manual testing is involved.
    

#### Disadvantages of Blackbox Testing

1. Writing automated test cases is impossible with the black box technique.
    
2. In the black box, since code is not getting tested, one might not be able to find excess code or code of higher time and space complexity.
    
3. Integration and data flow testing cannot be done in black box testing.
    

### Alpha Testing

Alpha testing is acceptance testing done by the Client, the members of the organization, and the testers at the Client. This testing focuses more on user interaction with the product, which is how users would perceive the software. For example, Google has a website built by the development team and tested by experienced testers at the organization. After the site was ready, it was given to the development, testing team, and DevOps team members to test as site users. Here the focus is on user experience.

The following are the features of Alpha Testing:

* **Alpha** testing is done at the development server. A development server is used when the product is still developing and testing.
    
* The members of the organization do alpha testing.
    
* **Alpha** testing is done after the product has finished both the development and testing phases.
    
* **Alpha** testing allows the people in the organization to experience the product before it reaches the market.
    

#### Entry Criteria of Alpha Testing

* The product has been developed and tested.
    
* Product has been deployed to the development server.
    
* All bugs in the product are fixed. The product has been verified.
    
* Product is ready for the production launch.
    

#### Exit Criteria of Alpha Testing

* The Client and its team accept the user experience of the software.
    
* All functionalities listed by the Client are met.
    
* There is no bug left unfixed stated by the Client.
    
* Client signs off **UAT**(User Acceptance Testing) document.
    

### Beta Testing

Beta testing is an acceptance test performed by limited users to test the product's functionalities before the application reaches worldwide. It is launched to a few people first to ensure they like the product and have a good user experience. In case people don't enjoy certain use cases, the feature can be rolled back or updated, and fixing it at this stage would still be cheaper than when the product reaches a million users.

For example, WhatsApp has a beta program where a few thousand people can enrol. But the actual user WhatsApp has billions. So when WhatsApp introduced the delete feature many years ago, it was first released to beta people. Once they liked it was introduced to the billions of users of WhatsApp.

The following are the features of Beta Testing:

* A limited number of real users perform **beta** testing to validate product experience.
    
* **Beta** testing helps capture market reactions before the product reaches the market.
    
* **Beta** testing is to validate the product. A well-tested product to validate customer reaction.
    
* **Beta** testing ensures users have the best experience of the product even when the product reaches a global scale.
    

#### Entry Criteria of Beta Testing

* Product has gone through alpha testing and is accepted by the Client.
    
* There are registered Beta testers available for the product.
    
* Product is deployed in a production environment whose access has been restricted.
    
* Beta version of the product is ready.
    

#### Exit Criteria of Beta Testing

* Feedback from the beta user is collected.
    
* All the necessary fixing obtained from the Feedback is done on the product.
    
* Product is ready for mass release.
    

### Difference between Alpha Testing and Beta Testing

| Alpha Testing | Beta Testing |
| --- | --- |
| Alpha testing is acceptance testing done by the client and client team. | Beta testing is acceptance testing done by a limited set of actual users. |
| The product is developed, tested, and bug-free. | Alpha testing is done. |
| Client signs off the Alpha testing document. | Feedback from the users is obtained, and necessary changes have been made to the product. |
| Client and its team of testers. | Limited set of actual users. |
| To get initial Feedback on the product within the organization. | To have a small market test of the product. |

### Smoke Testing

Smoke testing is done to validate if all application functionalities are working fine. Both developers and testers do smoke testing on the build. The application performance on the local system is always different from that on the server. Hence, it's a different environment setup.

After a build is deployed, say on Day 1, smoke testing is done to test functionality A, B. After 15 days, another build is deployed where smoke testing is done to test functionality A, B, C, D.

#### Features of Smoke Testing

1. Smoke testing is done to **validate** if the build is working fine on the server.
    
2. Both developers and testers do **smoke testing**.
    
3. Smoke testing tests the functionality. If **a bug** is found, the code is fixed, build is **deployed again**.
    
4. Smoke testing is done on the test environment. The application behavior on the local system vs. server is a lot different.
    

### Sanity Testing

Sanity testing is regression testing done on the build after the bugs are fixed. Regression testing ensures that changes on one part of the code have not affected the rest of the application. For example, If a site has payment integration, but Gpay had some issues. In sanity testing, Features of Gpay would be tested and ensured that the rest of the UPI integrations are working just fine.

Sanity testing is done only by the testers. Post sanity testing, only the bug is closed.

#### Features of Sanity Testing

1. Sanity testing is **regression testing** done by testers on the server.
    
2. Sanity testing is done to check whether the **bug is fixed**.
    
3. Sanity testing is done after smoke testing.
    
4. Sanity testing is reported in the **bug cycle**.
    

### Smoke Testing versus Sanity Testing

| Smoke Testing | Sanity Testing |
| --- | --- |
| Smoke testing is done to test the functionalities working fine on the build server. | Sanity testing use case is to test the build that new changes have not affected the old code. |
| Smoke testing is done by both developers and testers. | Sanity testing is done only by the testers. |
| Smoke testing is done to test that all the features listed in the requirements document are working fine. | Sanity testing is done for regression testing. That is rest of the product is working fine. |
| Smoke testing results are reported in RTM. | The sanity testing result is reported in the bug cycle. |
| Testing features of a site on a testing environment. | Regression testing ensures the bug is fixed and the rest of the features also work fine. |

### Regression Testing

Regression testing ensures new code changes have not affected the unchanged code. It has a specific meaning attached because some functionalities have been added and are working fine. Still, their integration with the rest of the application should work perfectly.

For instance, on a website to log in, there was a feature to allow login from Gmail, Facebook, and basic authentication. After a few months, the organization decided not to allow Facebook login. So, developers remove the functionality to log in via Facebook. Now Regression testing here means that wherever the login data has been used is still working fine.

### Retesting

Retesting an application means that the application has been tested before. If bugs were found, they were fixed as well. Retesting is done to find more bugs and deeper levels of module testing. The first level of testing is always done to ensure basic functional requirements are working fine. An application is retested to ensure quality by making sure modules are defect-free.

Example: The login module has been tested, and bugs have been fixed. Retesting the application to ensure that now the application is bug-free because, in the first round of testing, bugs were found.

### Regression Testing versus Retesting

| Regression Testing | **Retesting** |
| --- | --- |
| Regression testing is a type of testing done to ensure the changed code has not affected the existing code. | Retesting of an application is done to validate if the bugs have been fixed. |
| Regression testing can only be done when there is a requirement change, or some functionalities are getting added. | Retesting is done to close the opened bugs. |
| Regression testing is done for the passed test cases. | Retesting is done for the failed test cases. |
| Regression testing is part of the Software testing life cycle. | Retesting is part of the bug/defect life cycle. |
| Regression testing doesn't test the changed code. | Retesting is done only on the code which was broken. |

### Verification Testing

1. Verification testing is involved in the requirement-gathering phase, product planning, and product development
    
2. Verification testing ensures the process is going correctly. Requirements are correct, and development is going in accordance.
    
3. Verification helps to find the **bugs and issues** at the earlier stage of development. Verification testing is **cheaper**.
    
4. The **quality assurance** team does verification testing.
    

### Validation Testing

1. Validation testing is done in the **testing phase of SDLC**. Validation is also done at the **maintenance stage**.
    
2. Validation testing is done to **find the correct way of a process**. And also ensuring that the process chosen is the best.
    
3. Validation is a **costlier affair**. If process A is used, after that, process B is found to be better. The validation testing took a duration of finding the better approach.
    
4. The **product team** does validation testing.
    

### Verification Testing versus Validation Testing

| Verification Testing | Validation Testing |
| --- | --- |
| Verification testing is done by the testers to ensure the SDLC process is correct. | Validation testing is done by the product team to ensure the correct product is being built. |
| Verification testing is done by the testers. | Validation testing is done by the product and marketing team. |
| It is cheaper than validation testing. | Validation testing is costlier than verification testing. |
| Verification is done from requirement gathering, product planning, and product development phases. | Validation testing is done during the testing phase itself. |
| Verification ensures the process is going correctly. | Validation testing is done to ensure the best process is used for the product. |

### Web Application Testing

Web application testing is a specific type of testing centric around websites only. Websites have many components like responsiveness for different screens, OAuth integration of Gmail and Facebook, payment gateway integration, UI elements like images and carousel, API integrations, database integrations, server load, and virtual server deployment. Hence, web application testing covers all these domains.

#### Types of Web Application Testing

1. **Static Website Testing:** Static websites are where data on the UI is directly displayed from the database. There is no user interaction via the form. There is no contact us, comment section, or login element. Static Website testing is about fonts, colours, images, and user experience.
    
2. **Dynamic Website Testing:** Any website with a form is dynamic. Forms indicate user interaction. The data is sent from UI to the server, which stores the data in the database. Dynamic site testing includes UI/UX testing, API testing to ensure API is working, and API endpoints security testing. Finally, database testing tests that data is stored in the correct format.
    
3. **E-Commerce Website Testing:** E-commerce sites like Amazon and Flipkart, from where users can place their orders, are heavy on user interaction as with every button press, and location change - the data updates in a fraction of a second. Payment integration is also a crucial element of the e-commerce site. Testing all these functionalities is a part of the e-commerce site.
    
4. **Mobile-Based Web Testing:** Nowadays, all the sites are responsive. That is, the site is adjustable to the device's screen size. For example, the same site would have a different user experience based on screen size. The user experience of a site on the mobile screen, tablet screen, and laptop would be different as per the screen dimensions. This is a crucial element in mobile-based web testing.
    

#### How to test web applications?

* **Functionality Testing of a Website:** Functionality testing includes testing all the features on the website. The login, comment section, UI, contact us form, payment gateway, maps integration, etc., are all working. Data is coming from the backend, and the update is working. Forms validation is working, and links not broken are all part of functional testing.
    
* **Usability testing:** Also known as user experience testing, it ensures users can navigate pages without any issues, the site is responsive, and the icon size is visible on the smaller screen. Speed of the site and ensuring the site is user-ability.
    
* **Interface Testing:** Interface testing is a huge part of website testing as the user enters data in the form of the site. That data goes back to the backend and is inserted into the database. Response from the backend is sent back to the client. Ensuring data flow is maintained and correct data is stored in the database.
    
* **Database Testing:** Database testing in websites is all about ensuring data is getting in the correct format in the database. The transactions, rollback events, speed of getting the huge list, and password encryption are all maintained in database testing. Performance and speed of transactions are also an integral part of here.
    
* **Compatibility testing:** Compatibility testing is about hardware compatibility, but in the case of websites, it is linked with browser/cross-browser testing. The experience of the website across all browsers should be good. There is always a difference in date format shown in Firefox vs. date format in Google Chrome. So, ensuring the smooth experience of the entire site across tens of browsers we have.
    
* **Performance Testing:** Load and stress testing of the site using JMeter and parallel tools come under performance testing. Ensuring the site doesn't crash in case of bulk of users. Server load capacity, testing servers and load balancers are all part of the performance testing.
    
* **Security testing:** Penetration testing, SQL Injections, and ensuring there are no loopholes in API endpoints come under security testing. Authorization is also an integral part of the sites where the Admin can have to delete/edit rights which a normal user cannot. Also, Payment gateway integration testing comes under security testing.
    

### Accessibility Testing

Accessibility testing is a type of **software testing** where the main objective of the **tester** is to validate that the **product is equally usable** by people with disabilities. This definition on a broader level would also include people having hardware technical challenges as well.

#### Purpose of Accessibility Testing

1. **To cater to people with disability section:** Accessibility testing ensures specially abled section of society is also having a par user experience.
    
2. **Allow product to be used in case of hardware failures:** In case **microphone, speaker, or keyboard failures** of laptop or mobile. Still, people can enjoy the features of the web and mobile applications.
    
3. **To promote Inclusivity:** The product which promotes **inclusivity gains trust** among the people. Trust becomes a huge factor as the company grows. As more people would use the product, the company would also grow.
    

#### Challenges of Accessibility Test

1. Integration Testing: Accessibility testing is used for integration testing. Integration testing with an **external application** where data flow, testing in itself is tricky.
    
2. **Setting up test environment:** Enviornment setup for test cases for use of cases like **special keyboards** is tough as it involves medical expertise as well.
    
3. **Validating test cases:** Validating if the test case has passed, the **efficiency** of it again requires a huge medical dependency.
    

#### How to do Accessibility Testing?

**1\. Visual disability:**

* People with weaker eyesight must have magnification, light adjustment and text-to-speech features.
    
* Screen readers should be operatable via voice commands as Alexa operates in Amazon.
    
* The keyboard also should be operatable from voice commands.
    
* Alerts have sound features.
    

**2\. Hearing disability:**

* Having subtitles for videos and audio content.
    
* Keyboards with vibrations for every sound-based command.
    
* Navigations have text for routes to take.
    

**3\. Speech disability:**

* Text-to-speech integration at the microphone.
    
* Shorter ways to write text using shortcuts and mouse actions.
    
* Using AI tools to predict user patterns of text based on geolocations and previous searches.
    

### Browser Compatibility Testing

Browser compatibility signifies that all the features of a website have been tested to work smoothly across all browser versions. Forward compatibility in the browser means that the website will function well in upcoming browser releases, and backward compatibility means that the older browser versions to be smoothly working. Now for all the tests, automation is used to manually test hundreds of functionalities and ensure no bug is left, which manually is not feasible.

#### What is Cross Browser Testing?

Cross-browser testing is a non-functional testing where the website's functionality is tested across all browsers -Chrome, Safari, Edge, and Internet Explorer. It also ensures the site is working across all the versions of the browser as well. The following reasons explain why cross-browser testing is mandatory:

* Some HTML tags are not compatible with all the browsers
    
* Some CSS classes are unacceptable in the browsers
    
* Some technologies are not supported in older technologies like SVG
    
* Some image formats are not uniform across all the browsers
    

#### Workflows for Cross Browser Testing?

Planning -&gt; Development -&gt; Testing -&gt; Maintenance

1. Test planning phase includes the features that need to be tested for cross-browser functionality—listing the features that must be automated vs. manually tested. And which browsers are for a particular functionality. It uses tools like Saucelabs and BrowserStack for the same.
    
2. Test case development involves writing test cases and generating reports. The repeated tasks are automated using selenium script, cypressUI, etc.
    
3. Test cases are executed, the bugs are fixed, and the code is merged into the main pipeline. If the first two phases are designed well, running test cases is the easiest step. Nowadays, there are online tools for hardware requirements like Browserstack, etc.
    
4. Code maintenance is extremely crucial. A framework needs to be efficiently designed. Best practices for automation are used here.
    

### Usability Testing

Usability testing is a software testing methodology where the product is tested for **user-friendly behaviour**. The defect is reported if the font size, color, typography, and ease of using the application have issues. Usability testing focus on the **user experience** as every placement affects the business application. For instance, the logout option is always placed below so that users never log out.

#### What is the Purpose of Usability Testing?

1. Usability testing is done on the earlier stages of the product before final implementation starts
    
2. Usability testing is done on the **prototype** to ensure the final product is **user-friendly**
    
3. Usability testing adds a **Unique Selling Point** to the product to differentiate products in the similar category
    
4. The high competition market makes it mandatory for the client to have a **simpler and smoother interface**.
    
5. In the future, you cannot make major changes to the UI as people are already comfortable with the existing one.
    

#### Features of Usability Testing

1. **Effectiveness** of the system. How easy is it for the user to operate the application?
    
2. **The efficiency** of the application. Is the user able to easily navigate to the desired webpage or the link he was looking for.
    
3. **The accuracy** of the application is equally important. There shouldn't be any broken links. The system should be reliant.
    
4. The system has to be **user-friendly**. No advanced terms. Users must not require formal training to operate the application.
    

#### Phases of Usability Testing

**1\. Requirement Analysis:** The initial step is clearly understanding the **client's requirements**. What is the issue product is trying to resolve, and is the center of the application? Understanding functional requirements, non-functional requirements, and market analysis are all crucial.

**2\. Test Case Designing:** The usability test cases are all **manual test cases**. Finding experienced manual testing and having good design knowledge is crucial. Usability testing is mostly R&D based task. One needs to do a thorough market and competitor analysis.

**3\. Test Cases:** Test cases development to have maximum test case coverage. This needs to ensure all the features are covered, like **memorability and efficiency**, and the product is error-free. The same product in different screen sizes should provide a good experience.

**4\. Data Analysis:** Usability testing is all about data analysis. How much time does the user take to reach the payment screen in multiple options of **UI derived**. The impact of advertisements in particular sections of the product on revenue. Changing certain features has helped gain/lose traffic.

**5\. Report Generation:** Reports give a clear understanding of the entire **STLC**. The gain/loss is evident. Having experimented with the user interface in starting stage is mandatory. Otherwise, at a later stage, it could have adverse damage and impact on the company.

#### Parameters Covered by Usability Testing

* **Efficiency:** The efficiency of the product is how well the product works without making mistakes. The application should allow the user all the features of **edit/delete**. Users should be free to make mistakes, make changes, and edit on the same screen he is.
    
* **Memorability:** The application shouldn't be too hard to use. For instance, the logo is always home. Contact us, the about section is always at the bottom. In the menu, the logout option is always at the bottom. So, these norms should be followed so that the user can **freely navigate** to the screen of his choice.
    
* **Accuracy:** The application should be accurate. Everything has to be accurate, including calculations, promo codes, and taxes. The product needs to be **secured and bug-free**, for that matter. Every little piece of information that is displayed must be correct.
    
* **Learnability:** The application should be able to learn users' choices and patterns, and that is possible because of **artificial intelligence and machine learning technology**. All the products nowadays must have a learning model which has been well-trained as well.
    
* **Satisfaction:** There has to be a sense of satisfaction for the user using the product. A product that is **slow, non-reliable**, or has too many advertisements would automatically be a non-pleasant experience for the user. For instance, a user wants to order food from Zomato. He installs the application and does simple mobile authentication. But if the application had a huge form to fill, the user would switch the application in no time.
    
* **Errors:** A **bug-free** application is a must. The application has to be well-tested for all the parameters. If payment is not made, money must not be deducted—subscription when expires again, money must not be deducted. The user must have confidence in the application, hence the company.
    

#### Advantages of Usability Testing

* Usability testing gives **real-time** feedback to the development team about market validation.
    
* Usability testing is **cheaper** at the development stage as once the product reaches production, exponential money investment is required.
    
* It helps to make the product **efficient and applicable**.
    

#### Disadvantages of Usability Testing

* Usability testing **increases the budget** and time manifolds which is tough for any startup.
    
* Usability testing can lead to the **leak of private information** about the product and company.
    
* Finding the correct users is always challenging as everyone works in a fixed job. So, finding good volunteers is tough.
    

### Security Testing

Security testing is a type of software testing where testers find possible scenarios where there could be an information leak. It ensures the application is secured and doesn't have any loopholes or **vulnerabilities**. Security testing is the utmost priority of every company, as loss of information could put the company into legal trouble.

#### Principle of Security Testing

* **Confidentiality:** The data must remain secured and password encrypted.
    
* **Integrity:** The user's privacy of data and information must not be misused.
    
* **Authentication:** The **secure authentication** system where the user gets a safe gateway to the application.
    
* **Authorization:** Only the user with authorization for certain application sections should get it. For example, **Admin** must have access to all the information in the system except the user's password.
    
* **Availability:** The system must remain secure at all times.
    
* **Non-repudiation:** The system must not refuse the authorized user's access to the system.
    

#### Types of Security Testing

* **Vulnerability Scanning:** The system uses an automation testing tool that checks for common security patterns like **SQL injection**.
    
* **Security Scanning:** **Security scanning** is done manually and through automation to ensure both the system and network are secured.
    
* **Penetration Testing:** Penetration testing is done to check there is no **malicious attack** from a third party to get unauthorized access to the system or data.
    
* **Ethical Hacking:** Ethical hacking comes under a **bug bounty program** that companies host, where professionals let companies know their bugs so that the system can be ensured even further.
    
* **Posture Assessment:** Combination of all the **security scanning** to tell the company how to secure their product and solutions to make their system even more secure.
    

#### How to do Security Testing?

* **Security Testing at Requirement Gathering phase:** At this phase, the information about use cases and the list of functional and **non-functional requirements** are kept secure to not leak to competitors.
    
* **Security Testing at System Design Phase:** At this phase, design the areas where security testing needs to be implemented. For instance, UI, API, Message pass, Database, and servers like EC2 are identified.
    
* **Security Testing at the Development Phase:** The **software performs** unit and integration testing for vulnerabilities and attacks. System testing for any loopholes.
    
* **Security Testing at the Testing Phase:** Every module performs a security checkup for any vulnerability.
    
* **Security Testing at Maintenance Phase:** Through bug bounty and third-party vendors, the system goes through continuous penetration and vulnerability testing.
    

#### Techniques for Security Testing

1. **Tiger Box:** Tiger Box Testing is done by a system with security testing tools to check vulnerabilities and defects in the system.
    
2. **Black Box:** Black box testing in security is done on the network topology.
    
3. **Grey Box:** Grey box is a combination of both tiger box and black box as tools are used here, and network topology is also tested.
    

### Risk-Based Testing

Risk-based testing is a software testing methodology where the functionalities are tested on the probability of risk from higher to lower. The risks are categorized based on impact on the application, defect clustering, business result, and complexity.

#### When to Implement Risk-Based Testing?

* Any long-term project on development and maintenance. The longer the project, the tougher, the management of it.
    
* Project involving research & development. Any new innovative approach is challenging to manage.
    
* Large scaled projects with a huge budget, large teams, bigger databases, and heavy loads.
    
* Projects following incremental and iterative models.
    

#### Types of Risk

Risk is any unprojected event that could change the designed series of tasks. These risks can change the series of projected events, costs, timelines, and, ultimately, functionalities.

Risks are of two types:

1\. Positive risks: Positive risks that could bring better deals in the future. Investment in better technology and features could bring more traffic to the product.

2\. Negative risks: Risks that, on failure could bring huge losses like issues in the team, economic recession, war, climate changes, etc. These add threats to the cycle of the project.

#### Characteristics of Risk-Based Testing

* **Risk-based Testing matches the order of Testing** Always from test cases with the higher risks to the lower ones. This also helps minimize the risk because the riskier for the business is already well-tested.
    
* **More efforts to higher the risk value** Once the higher-risk ones are sorted, the entire cycle eases out. Higher risks are mostly to new functionalities or requiring tons of R&D.
    
* **Risk identification is a continuous cycle** Risk needs to be broken down into sub-parts as the big chunk of risk would also have smaller units in it. Also, after every task is done, the risk changes to the upcoming one as that is the priority. Also, some tasks that were the low priority of risk can have tons of complications in them as well
    

#### Risk Management Process

1. Risk Identification: Risk identification is a brainstorming session where everything is considered requirements, SDLC planning, cost, time, resources, \`previous experiences, etc. At this stage, a spreadsheet of risks is maintained. And risks are further divided into smaller sub-risks which is called risk breakdown.
    
2. Risk Analysis: The risk Analysis session prioritize the risk based on frequency, impact, significance to the product, budget, etc. The product lead and technical lead do this session. After this, we have a sheet with risks in the order of priority.
    
3. Risk Response Planning: We have a sequential list of risks based on priority. Here comes the crucial element of how to handle the risks. The SDLC process would be altered to manage the risks figured. Risk mitigation is a process to reduce the impact of the risk by following the measures, which includes more effort on heavier risk tasks. Risk Contingency is associated with having a backup plan in case risk gets out of control. The measures to take are associated here.
    
4. Risk Monitoring: The entire cycle is done to minimize risks. But these risks need to be closely monitored as risks would never be eliminated. Quantitatively measuring the risk at every stage and checking up on the status comes at this phase.
    

#### Risk-Based Testing Approach

1. **Analyzing the requirement phase closely:** When the client brings a new project or a requirement to add/update, a functional requirement document is prepared with lists of all the function and non-function requirements. An RTM(Requirement Traceability Matrix) is maintained. All the risks associated with the process are identified at this stage.
    
2. **Finding risks in the development cycle:** A SDLC cycle is developed around functionalities. An action plan of execution is done. Sprints are divided, the staff is trained, duration is set. Since the process is getting even more magnified images, we now have sub-tasks. We now have definable risks.
    
3. **Developing a Test cycle around the risks:** The testing cycle is developed so that features with higher risks are getting more effort to contain the risk.
    
4. **Risk Contingency Test plans:** In case risks are unavoidable or cannot be eliminated, what possible measures can be taken so that the risk is minimized are planned at this stage. The below example would clear the picture.
    

### Compliance Testing

Compliance testing or Conformance testing is a software testing technique where the product is certified to follow the practices and guidelines under regulations set by the organizations like IEEE, W3C, etc. The certifications ensure the product follows the institution's functional and non-functional testing guidelines.

#### Why do we need Compliance Testing?

1. Conformance testing ensures the system is being designed following best practices.
    
2. Best practices themselves ensure reliable software is being developed.
    
3. The certifications assure the client that the product of high quality is being developed.
    
4. Conformance testing gives the team direction on building scalable products.
    

#### How to do a Compliance Test?

1. **Getting a deeper sense of requirements:** Understanding the requirements is paramount. A test plan has to be developed around that. Certifications are made to ensure the requirements are met following the standardizations. Completeness in the requirements set is crucial.
    
2. **Risk analysis:** Finding loopholes and risk parameters are important. The majority of the bugs are in 10% of the modules. The security and robustness of these modules have become a subject of high priority.
    
3. **Profile:** Profile is a requirement specification where a set of users have been assigned the system's functionality. Examples are login profile, payment profile, etc. It makes it easier to identify the major component sections of the application.
    
4. **Levels:** Requirments are further specified based on levels. The basic requirements are -- Level 1 example can be UI, blog section, Level 2 can be Login, and Payment Integration being Level 3.
    
5. **Modules:** Modules are collective standardizations and specifications, i.e., signup and sign-in together come under the authentication module. User profile, his activity is part of the user module, and so on.
    

#### Conformance/Compliance Testing Process

1. **Standards and Specifications are analyzed:** Standards and specifications are as per the requirements and system design. The goal is to analyze the risk areas and ensure those are protected and kept secure.
    
2. **Tool Selection:** Tool selection differs for every test scenario. UI testing requires tools like Selenium, Appium, API testing, Rest Assured library, postman, etc.
    
3. **Testing Process Development:** Test case development here is done to validate the quality standards are met. The standards are the test case scenarios. In test case failure, code is redone to ensure those are met. Here white box testing is given the primary significance.
    
4. **Specifications validations:** Once the conformance testing is passed. Another round of validations is done before the certification is provided.
    
5. **Certifications:** The certification is provided based on level. The higher the level, the more specified and in-depth the testing is done.
    

### ETL Testing

ETL Testing stands for Extract-Transform-Load Testing. Nowadays, in the industry, there is a famous architecture called MVC, which stands for the Model View Controller. Where the controller acts as middleware. Data is taken from the database, which is mapped to a model schema for the data. Now that data in the controller is further cleaned and processed. That processed data is sent to the front end via API.

For example, there is a tutorial site and the user registers on the site, then data is stored in the database as full name, DOB, education qualification, etc. Now Admin wants to see on its portal - how many users registered today. This data from API goes to the backend, where the date filter is passed. That filtered data which we have after the query is sent to UI where the admin can see the final count.

In ETL testing, this entire process, from storing the data to validating it, cleaning it, verifying, and ultimately manipulating the data to extract results, comes.

* **Extract:** Get the data from the table in the data source or from an Excel sheet.
    
* **Transform:** Validate the data is stored correctly. Validate the schema, normalization is maintained, and keys are used. Clean the database if required. All these operations are done directly in the database. Hence, the backup must be maintained. Also, deleting or editing an entry directly in the database is prohibited, so that must be taken care of. Database management systems also create metadata that can also be used.
    
* **Load:** Load the data into the data warehouse, where all the raw data from all the sources is kept. An aggregate of all the data is kept in the warehouse.
    

#### Process of ETL Testing

ETL testing is a 5 stage testing process. Testing is done at each stage of ETL.

1. **Maintain the data sources:** Data generates at various stages in the product. The user might be uploading an Excel sheet, data backups getting maintained, the actual database, database credentials, etc.
    
2. **Data acquisition:** Creating an API to transfer the data to the database, connecting both the endpoints of the application and database, sending GET/POST requests, and ensuring encryption and data security.
    
3. **Dimensional Modelling:** Implementing the business logic that is the architecture of the entire database management system and creating schema structure, Keys, backups, rollbacks, maintaining atomicity of transactions, and how data would be mapped to the controller via models. They ensure the data synchronization on the model and database of complicated data types like date and time.
    
4. **Populate the data:** Populate the data, and create an API to push the data to the database. If the data is in an Excel sheet, automate the reading and transfer it to the database. Add exception handling and error logging to the system. Parallel execution is to be maintained as well.
    
5. **Report generation:** Data mining and result report is generated. These results are the outcome of the queries, and efficient queries are used as data is usually huge. Reports are generated when the data goes to the system, and their data is manipulated at the controller level.
    

#### Types of ETL Testing

1. **Production Validation Testing:** The database at the production server is tested here for accuracy. Usually, the testing is done at the UAT server, but ensuring the database connected to the live action is correct comes under production validation.
    
2. **Source-to-Target Testing:** During data transfer via an API, data is validated to be correct and comes under source-to-target testing.
    
3. **Application Upgradation Testing:** When the product upgrades, that is, new features are added, and some might be removed, the database is still fine. Also, upgradation impact database schema. So, previous data is protected, and new changes are validated here.
    
4. **Metadata Testing:** Metadata tests the data type, length, constraints, index, and keys, i.e., database schema.
    
5. **Data Completeness Testing:** Data completeness testing ensures the exact data is stored in the database. The transaction is maintained, and multiple tables reflect the data. In case of failure, rollback is done from all the affected tables.
    
6. **Data Accuracy Testing:** Correct data is stored with the data type, and data is transferred similarly.
    
7. **Data Transformation Testing:** Data insertion is different from the data. For example, in a database, usually, everything is saved in uppercase, dates are stored differently, data is inserted into different tables, and some mathematical and pattern operations are done. Validating these operations come under data transformation testing
    
8. **Data Quality Testing:** Data quality testing ensures null checks are maintained and references and unique IDs are maintained.
    
9. **Incremental ETL testing:** Incremental testing ensures updates and inserts are working correctly on the data.
    
10. **GUI/Navigation Testing:** This testing ensures the data on the front-end application is correct.
    

#### Types of ETL Bugs

1. GUI bugs: Bugs related to the GUI of the application, that is, the font, colour, alignment, etc.
    
2. Boundary Value Analysis Bug: Bugs at the minimum and maximum values.
    
3. Equivalence Class Partitioning Bug: Bugs at validation.
    
4. Input/Output Bug: Invalid output or valid input not accepted bugs.
    
5. Calculation Bug: Bugs in mathematical or pattern operations.
    
6. Load Bug: Functionality breaking down on load on the server.
    
7. Version Control Bug: Version information not maintained bug.
    
8. Hardware Bug: Hardware devices not working/responding bug.
    

### Data Flow Testing

Data flow testing is a white box testing type concerned with the flow of variables and not the module's flow. It follows where the variable is referenced. Data flow testing makes use of control flow graphs and associations.

#### Types of Data Flow Testing

1. Static Data Flow Testing: Declaring the variables, using the variables, and finding the values all happen without the code execution is static data flow testing. Control flow graphs are used for the same.
    
2. Dynamic Data Flow Testing: The variables and their value are examined with the code execution in dynamic data flow testing. The changes in the variable and their references are observed with the requirement that the code must be executed.
    

#### Advantages of Data Flow Testing

1. Data flow testing helps to redefine the flow of code.
    
2. It helps to identify the excess code if it exists.
    
3. It helps to identify computational variables.
    
4. It tests the code without executing it.
    

#### Disadvantages of Data Flow Testing

1. Since it is white-box testing, coding knowledge is required.
    
2. It is a time-consuming testing process.
    
3. It requires a good amount of manual testing.
    
4. It is a slow process as a lot of manual intervention is required.
    

#### Data Flow Testing Coverage

1. All definition coverage: It covers all the sub-paths from each definition.
    
2. All definition-c use coverage: It covers all the computation use sub-paths from each definition
    
3. All definition-p use coverage: It covers all the predicate use sub-paths from each definition
    
4. All-use coverage: It covers all the c-use and p-use sub-paths from each definition.
    
5. All definition use coverage: It covers all the sub-paths from definition to their respective use.
    

This was all about different kinds of testing. Thanks for reading :).