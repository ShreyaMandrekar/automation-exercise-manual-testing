# Test Plan – Automation Exercise

## 1. Document Information

| Item                   | Details                              |
| ---------------------- | ------------------------------------ |
| Project                | Automation Exercise – Manual Testing |
| Application Under Test | Automation Exercise Web Application  |
| Testing Type           | Manual Testing                       |
| Testing Approach       | Exploratory and Functional Testing   |
| Document               | Test Plan                            |
| Tester                 | Shreya Mandrekar                     |

---

## 2. Introduction

This document defines the testing approach, scope, objectives, resources, and deliverables for the manual testing of the Automation Exercise web application.

The project is a self-directed QA testing project performed on a publicly accessible practice web application. Since a client-specific Software Requirements Specification (SRS) was not provided, the testing scope is derived from the application's available functionality, documented application behavior, exploratory observations, and standard software testing practices.

---

## 3. Test Objective

The objectives of this testing project are:

* To verify that the major application functionalities work as expected.
* To identify functional and validation defects.
* To verify positive and negative user flows.
* To validate input fields and boundary conditions where applicable.
* To verify navigation and user workflows.
* To practice test scenario creation, test case design, execution, defect reporting, retesting, and regression testing.
* To document the testing process in a structured and professional manner.

---

## 4. Scope of Testing

### 4.1 In Scope

The following application areas are planned for testing:

* Home page
* User Registration / Signup
* Login and Logout
* Product listing
* Product search
* Categories
* Brands
* Product details
* Shopping cart
* Checkout flow
* Contact Us
* Newsletter / subscription functionality
* Account deletion
* API testing

### 4.2 Out of Scope

The following areas are outside the initial scope of this manual testing project:

* Source code-level testing
* Penetration testing
* Full-scale security auditing
* Production database administration
* Load and stress testing requiring dedicated infrastructure
* Internal server and infrastructure testing that is not accessible through the application

---

## 5. Requirements Basis

No client-specific requirements document or SRS was provided for this self-directed project.

Therefore, testing requirements and scenarios will be derived from:

* Available application functionality
* Application behavior observed during exploratory testing
* Available application documentation
* Documented API behavior where applicable
* Standard software testing principles and practices

The application's documented behavior will not be treated as proof that the implementation is defect-free. Actual behavior will be verified through test execution.

---

## 6. Testing Approach

The project will follow the following testing workflow:

1. Explore the application and understand available functionality.
2. Document exploratory observations.
3. Identify high-level test scenarios.
4. Design detailed test cases.
5. Prepare appropriate test data.
6. Execute test cases against the application.
7. Record actual results and test status.
8. Report genuine defects when identified.
9. Retest defects after a fix or change.
10. Perform regression testing on related functionality.

The primary testing approach will be manual testing.

---

## 7. Testing Types

The following testing types will be applied where relevant:

* Functional Testing
* Positive Testing
* Negative Testing
* Validation Testing
* UI Testing
* Integration Testing
* Smoke Testing
* Sanity Testing
* Regression Testing
* Retesting
* Compatibility Testing
* Usability Testing
* Exploratory Testing
* API Testing

Not every testing type will necessarily be applicable to every module.

---

## 8. Test Design Techniques

The following test design techniques will be used where applicable:

* Equivalence Partitioning
* Boundary Value Analysis
* Positive and Negative Test Design
* Validation-based testing
* Data variation testing

The appropriate technique will be selected based on the functionality being tested.

---

## 9. Test Environment

Testing will be performed on the publicly accessible Automation Exercise web application.

The following environment details will be recorded during test execution:

* Operating System: To be recorded during execution
* Browser: To be recorded during execution
* Browser Version: To be recorded during execution
* Application URL: Automation Exercise
* Testing Mode: Manual

Environment details may be updated if testing is performed using additional browsers or devices.

---

## 10. Entry Criteria

Testing can begin when:

* The application is accessible.
* The functionality under test is available.
* Required test data is prepared.
* Test scenarios and test cases for the selected module are ready.
* The test environment is available.

---

## 11. Exit Criteria

Testing for a module may be considered complete when:

* Planned test cases have been executed.
* Results have been documented.
* Identified defects have been recorded.
* Failed test cases have been investigated.
* Required retesting has been completed.
* Relevant regression testing has been performed.
* Test execution results have been documented.

---

## 12. Defect Management

Defects identified during actual test execution will be documented with relevant information such as:

* Defect ID
* Summary
* Description
* Steps to reproduce
* Expected result
* Actual result
* Severity
* Priority
* Environment
* Evidence such as screenshots, where applicable
* Defect status

Jira will be used later in the project for tracking genuine defects and their lifecycle.

No defect will be reported unless it is actually reproduced during testing.

---

## 13. Test Deliverables

The planned testing deliverables are:

* Test Plan
* Exploratory Testing Notes
* Test Scenarios
* Test Cases
* Test Data
* Test Execution Results
* Defect Reports
* Retest Results
* Regression Test Results
* API Testing Documentation

---

## 14. Risks and Assumptions

### Risks

* The publicly accessible application may change during the testing period.
* Application availability may affect test execution.
* Test data may need to be recreated because of account-related restrictions.
* Some internal application behavior or database information may not be directly accessible.

### Assumptions

* The application is available for testing through its public interface.
* Testing will be performed using functionality accessible to a normal user.
* Test results will be based on actual execution rather than assumptions.
* Application documentation may be used as supporting information but will not replace actual verification.

---

## 15. Test Execution and Reporting

Each test case will be executed against the application and the following information will be recorded:

* Test Case ID
* Test data used
* Actual result
* Status (Pass / Fail / Blocked)
* Defect ID, if applicable
* Comments or observations

Failed test cases will be investigated to determine whether the failure is caused by an actual application defect, incorrect test data, environmental issues, or another reason.

---

## 16. Traceability

The testing documentation will maintain the following relationship:

**Application Functionality / Requirements Basis**
→
**Exploratory Observations**
→
**Test Scenarios**
→
**Test Cases**
→
**Test Execution Results**
→
**Defects**
→
**Retesting**
→
**Regression Testing**

This structure provides traceability between the functionality being tested and the testing activities performed.

---

## 17. Document Maintenance

This Test Plan may be updated when the project scope, application functionality, testing approach, or testing environment changes.

