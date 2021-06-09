
# Test Plan Template

## Table of contents

- [1. Introduction](#1-introduction)
  * [1.1 Purpose](#11-purpose)
  * [1.2 Scope](#12-scope)
  * [1.3 Intended Audience](#13-intended-audience)
  * [1.4 Document Terminology and Acronyms](#14-document-terminology-and-acronyms)
  * [1.5  References](#15--references)
  * [1.6 Document Structure](#16-document-structure)
- [2. Evaluation Mission and Test Motivation](#2-evaluation-mission-and-test-motivation)
  * [2.1 Background](#21-background)
  * [2.2 Evaluation Mission](#22-evaluation-mission)
  * [2.3 Test Motivators](#23-test-motivators)
- [3. Target Test Items](#3-target-test-items)
- [4. Outline of Planned Tests](#4-outline-of-planned-tests)
  * [4.1 Outline of Test Inclusions](#41-outline-of-test-inclusions)
  * [4.2 Outline of Other Candidates for Potential Inclusion](#42-outline-of-other-candidates-for-potential-inclusion)
  * [4.3 Outline of Test Exclusions](#43-outline-of-test-exclusions)
- [5. Test Approach](#5-test-approach)
  * [5.1 Initial Test-Idea Catalogs and Other Reference Sources](#51-initial-test-idea-catalogs-and-other-reference-sources)
  * [5.2 Testing Techniques and Types](#52-testing-techniques-and-types)
    + [5.2.1 Data and Database Integrity Testing](#521-data-and-database-integrity-testing)
    + [5.2.2 Functional Testing](#522-functional-testing)
    + [5.2.3 Business Cycle Testing](#523-business-cycle-testing)
    + [5.2.4 User Interface Testing](#524-user-interface-testing)
    + [5.2.5 Performance Profiling](#525-performance-profiling)
    + [5.2.6 Load Testing](#526-load-testing)
    + [5.2.7 Stress Testing](#527-stress-testing)
    + [5.2.8 Volume Testing](#528-volume-testing)
    + [5.2.9 Security and Access Control Testing](#529-security-and-access-control-testing)
    + [5.2.10 Failover and Recovery Testing](#5210-failover-and-recovery-testing)
    + [5.2.11 Configuration Testing](#5211-configuration-testing)
    + [5.2.12 Installation Testing](#5212-installation-testing)
- [6. Entry and Exit Criteria](#6-entry-and-exit-criteria)
  * [6.1 Test Plan](#61-test-plan)
    + [6.1.1 Test Plan Entry Criteria](#611-test-plan-entry-criteria)
    + [6.1.2 Test Plan Exit Criteria](#612-test-plan-exit-criteria)
    + [6.1.3 Suspension and Resumption Criteria](#613-suspension-and-resumption-criteria)
  * [6.2 Test Cycles](#62-test-cycles)
      - [6.2.1 Test Cycle Entry Criteria](#621-test-cycle-entry-criteria)
      - [6.2.2 Test Cycle Exit Criteria](#622-test-cycle-exit-criteria)
      - [6.2.3 Test Cycle Abnormal Termination](#623-test-cycle-abnormal-termination)
- [7. Deliverables](#7-deliverables)
- [7.1 Test Evaluation Summaries](#71-test-evaluation-summaries)
- [7.2 Reporting on Test Coverage](#72-reporting-on-test-coverage)
- [7.3 Perceived Quality Reports](#73-perceived-quality-reports)
- [7.4 Incident Logs and Change Requests](#74-incident-logs-and-change-requests)
- [7.5 Smoke Test Suite and Supporting Test Scripts](#75-smoke-test-suite-and-supporting-test-scripts)
- [7.6      Additional Work Products](#76------additional-work-products)
  * [7.6.1     Detailed Test Results](#761-----detailed-test-results)
  * [7.6.2     Additional Automated Functional Test Scripts](#762-----additional-automated-functional-test-scripts)
  * [7.6.3     Test Guidelines](#763-----test-guidelines)
  * [7.6.4     Traceability Matrices](#764-----traceability-matrices)
- [8. Testing Workflow](#8-testing-workflow)
- [9. Environmental Needs](#9-environmental-needs)
  * [9.1 Base System Hardware](#91-base-system-hardware)
  * [9.2 Base Software Elements in the Test Environment](#92-base-software-elements-in-the-test-environment)
  * [9.3 Productivity and Support Tools](#93-productivity-and-support-tools)
  * [9.4 Test Environment Configurations](#94-test-environment-configurations)
- [10. Responsibilities, Staffing, and Training Needs](#10-responsibilities--staffing--and-training-needs)
  * [10.1 People and Roles](#101-people-and-roles)
  * [10.2 Staffing and Training Needs](#102-staffing-and-training-needs)
- [11. Iteration Milestones](#11-iteration-milestones)
- [12. Risks, Dependencies, Assumptions, and Constraints](#12-risks--dependencies--assumptions--and-constraints)
- [13. Management Process and Procedures](#13-management-process-and-procedures)

## 1. Introduction

### 1.1 Purpose

The Test Plan should help us to gather all the information we need to plan our testing effort and it describes our aproach to testing the software.

### 1.2 Scope

In our testing we will have Unit and installation tests.

### 1.3 Intended Audience

This dokument is mostly writen to be read by developers on this project and interestet people.

### 1.4 Document Terminology and Acronyms

| Abbr | Abbreviation                        |
|------|-------------------------------------|
| API  | Application Programmable Interface  |
| CI   | Continuous Integration              |
| CD   | Continuous Delivery/Deployment      |
| n/a  | not applicable                      |
| SRS  | Software Requirements Specification |
| tbd  | to be determined                    |
| UI   | User Interface                      |
| VC   | Version Control                     |
| TDD  | Test Driven Development             |

### 1.5  References
| Title                                                                   | Date       | Publishing organization   |
| ------------------------------------------------------------------------|:----------:| ------------------------- |
| [Blog](https://work2playtogether.wordpress.com/blog/)                   | May. 2021  |                  |
| [GitHub Code Repository](https://github.com/rbnsch/Work2Play)           | May. 2021  |                  |
| [UC1 Task](./UseCases/CRUD-Task.md)                                     | May. 2021  |                  |
| [UC2 Reward](./UseCases/Crud-Reward.md)                                 | May. 2021  |                  |
| [Test Plan](./TestPlan.md)                                              | May. 2021  |                  |
| [SRS](./SRS.md)                                                         | May. 2021  |                  |
| [SAD](./SAD/SAD.md)                                                         | May. 2021  |                  |

### 1.6 Document Structure

n/a

## 2. Evaluation Mission and Test Motivation

### 2.1 Background

Testting is used to ensure that written code does what we wanted it to do. It also helps to find existing faults in the code.

### 2.2 Evaluation Mission

- find as many bugs as possible

- find important problems

- assess perceived quality risks

- advise about perceived project risks

- verify a specification

- satisfy stakeholders

- advise about testing

- fulfill process mandates

### 2.3 Test Motivators

Our testing is motivated through the fact that testing helps keeping the code running and realizing errors early. It also helps to see if your implementation is doing what the application is supposed to do.

## 3. Target Test Items

In the list below you can see what our targets for testing are.
- Databasehelper
- FragmentTask
- FragmentRewards

## 4. Outline of Planned Tests

We plan to use Unittesting for our Project.

### 4.1 Outline of Test Inclusions
*Frontend: Android Client*:

- UI testing of views/fragments
- Unit testing
- Deployment testing

*Backend: Java Application*:

- Unit testing
- Integration testing
- Deployment testing


The tests themself will not be tested and will not account into code coverage.

### 4.2 Outline of Other Candidates for Potential Inclusion

n/a

### 4.3 Outline of Test Exclusions

n/a

## 5. Test Approach

TBD

[The Test Approach presents the recommended strategy for designing and implementing the required tests. Sections 3, Target Test Items, and 4, Outline of Planned Tests, identified what items will be tested and what types of tests would be performed. This section describes how those tests will be realized.
One aspect to consider for the test approach is the techniques to be used. This should include an outline of how each technique can be implemented, both from a manual and/or an automated perspective, and the criterion for knowing that the technique is useful and successful. For each technique, provide a description of the technique and define why it is an important part of the test approach by briefly outlining how it helps achieve the Evaluation Mission or addresses the Test Motivators.
Another aspect to discuss in this section is the Fault or Failure models that are applicable and ways to approach evaluating them.
As you define each aspect of the approach, you should update section 10, Responsibilities, Staffing, and Training Needs, to document the test environment configuration and other resources that will be needed to implement each aspect.]

### 5.1 Initial Test-Idea Catalogs and Other Reference Sources

TBD

[Provide a listing of existing resources that will be referenced to stimulate the identification and selection of specific tests to be conducted. An example Test-Ideas Catalog is provided in the examples section of RUP.]

### 5.2 Testing Techniques and Types

#### 5.2.1 Data and Database Integrity Testing

n/a

#### 5.2.2 Functional Testing
TBD

[Function testing of the target-of-test should focus on any requirements for test that can be traced directly to use cases or business functions and business rules. The goals of these tests are to verify proper data acceptance, processing, and retrieval, and the appropriate implementation of the business rules. This type of testing is based upon black box techniques; that is, verifying the application and its internal processes by interacting with the application via the Graphical User Interface (GUI) and analyzing the output or results. The following table identifies an outline of the testing recommended for each application.]

|                       | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
|Technique Objective    |  [Exercise target-of-test functionality, including navigation, data entry, processing, and retrieval to observe and log target behavior.]  |
|Technique              |  [Exercise each use-case scenario's individual use-cases flows or functions and features, using valid and invalid data, to verify that:; the expected results occur when valid data is used; the appropriate error or warning messages are displayed when invalid data is used; each business rule is properly applied]  |
|Oracles                |  [Outline one or more strategies that can be used by the technique to accurately observe the outcomes of the test. The oracle combines elements of both the method by which the observation can be mad, and the characteristics of specific outcome that indicate probable success or failure. Ideally, oracles will be self-verifying, allowing automated tests to make an initial assessment of test pass or failure, however, be careful to mitigate the risks inherent in automated results determination.]  |
|Required Tools         |  [The technique requires the following tools:; Test Script Automation Tool; base configuration imager and restorer; backup and recovery tools; installation-monitoring tools (registry, hard disk, CPU, memory, and so on); data-generation tools]  |
|Success Criteria       |  [The technique supports the testing of:; all key use-case scenarios; all key features ] |
|Special Considerations |  [Identify or describe those items or issues (internal or external) that impact the implementation and execution of function test.]  |

#### 5.2.3 Business Cycle Testing
n/a
#### 5.2.4 User Interface Testing

tbd
[User Interface (UI) testing verifies a user's interaction with the software. The goal of UI testing is to ensure that the UI provides the user with the appropriate access and navigation through the functions of the target-of-test. In addition, UI testing ensures that the objects within the UI function as expected and conform to corporate, or industry, standards.]

|                       | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
|Technique Objective    |  [Exercise the following to observe and log standards conformance and target behavior:; Navigation through the target-of-test reflecting business functions and requirements, including window-to-window, field-to- field, and use of access methods (tab keys, mouse movements, accelerator keys).; Window objects and characteristics can be exercised-such as menus, size, position, state, and focus.]   |
|Technique              |  [Create or modify tests for each window to verify proper navigation and object states for each application window and object.]   |
|Oracles                |  [Outline one or more strategies that can be used by the technique to accurately observe the outcomes of the test. The oracle combines elements of both; the method by which the observation can be made and the characteristics of specific outcome that indicate probable success or failure. Ideally, oracles will be self-verifying, allowing automated tests to make an initial assessment of test pass or failure, however, be careful to mitigate the risks inherent in automated results determination.]   |
|Required Tools         |   [The technique requires the Test Script Automation Tool.]  |
|Success Criteria       |   [The technique supports the testing of each major screen or window that will be used extensively by the end user.]  |
|Special Considerations |   [Not all properties for custom and third party objects can be accessed.]  |

#### 5.2.5 Performance Profiling

n/a

#### 5.2.6 Load Testing

n/a

#### 5.2.7 Stress Testing

n/a


#### 5.2.8 Volume Testing

n/a

#### 5.2.9 Security and Access Control Testing

n/a

#### 5.2.10 Failover and Recovery Testing

n/a

#### 5.2.11 Configuration Testing

n/a

#### 5.2.12 Installation Testing

 tbd

[Installation testing has two purposes. The first is to ensure that the software can be installed under different conditions (such as a new installation, an upgrade, and a complete or custom installation) under normal and abnormal conditions. Abnormal conditions include insufficient disk space, lack of privilege to create directories, and so on. The second purpose is to verify that, once installed, the software operates correctly. This usually means running a number of tests that were developed for Function Testing.]

|                       | Description                                                         |
|-----------------------|---------------------------------------------------------------------|
|Technique Objective    |   [Exercise the installation of the target-of-test onto each required hardware configuration under the following conditions to observe and log installation behavior and configuration state changes:; new installation: a new machine, never installed previously with Project Name; update: a machine previously installed Project Name, same version; update: a machine previously installed Project Name, older version]  |
|Technique              |   [Develop automated or manual scripts to validate the condition of the target machine.; new: never installed; same or older version already installed; Launch or perform installation..; Using a predetermined subset of Function Test scripts, run the transactions.]  |
|Oracles                |   [Outline one or more strategies that can be used by the technique to accurately observe the outcomes of the test. The oracle combines elements of both the method by which the observation can be made and the characteristics of specific outcome that indicate probable success or failure. Ideally, oracles will be self-verifying, allowing automated tests to make an initial assessment of test pass or failure, however, be careful to mitigate the risks inherent in automated results determination.]  |
|Required Tools         |   [The technique requires the following tools:; base configuration imager and restorer; installation-monitoring tools (registry, hard disk, CPU, memory, and so on ] |
|Success Criteria       |   [The technique supports the testing of the installation of the developed product in one or more installation configurations.]  |
|Special Considerations |   [What transactions should be selected to comprise a confidence test that application has been successfully installed and no major software components are missing?]  |


## 6. Entry and Exit Criteria

### 6.1 Test Plan

#### 6.1.1 Test Plan Entry Criteria

n/a

#### 6.1.2 Test Plan Exit Criteria

n/a

#### 6.1.3 Suspension and Resumption Criteria

n/a

### 6.2 Test Cycles

##### 6.2.1 Test Cycle Entry Criteria

n/a

##### 6.2.2 Test Cycle Exit Criteria

n/a

##### 6.2.3 Test Cycle Abnormal Termination

n/a


## 7. Deliverables

## 7.1 Test Evaluation Summaries

n/a

## 7.2 Reporting on Test Coverage

tbd
[Provide a brief outline of both the form and content of the reports used to measure the extent of testing, and indicate how frequently they will be produced. Give an dication as to the method and tools used to record, measure, and report on the extent of testing.]

## 7.3 Perceived Quality Reports

n/a

## 7.4 Incident Logs and Change Requests

TBD
[Provide a brief outline of both the method and tools used to record, track, and manage test incidents, associated change requests, and their status.]

## 7.5 Smoke Test Suite and Supporting Test Scripts

n/a

## 7.6      Additional Work Products

n/a

### 7.6.1     Detailed Test Results

n/a

### 7.6.2     Additional Automated Functional Test Scripts

[These will be either a collection of the source code files for automated test scripts, or the repository of both source code and compiled executables for test scripts maintained by the test automation product.]

### 7.6.3     Test Guidelines
n/a

### 7.6.4     Traceability Matrices
n/a



## 8. Testing Workflow

tbd

[Provide an outline of the workflow to be followed by the test team in the development and execution of this Test Plan.
The specific testing workflow that you will use should be documented separately in the project's Development Case. It should explain how the project has customized the base RUP test workflow (typically on a phase-by-phase basis). In most cases, we recommend you place a reference in this section of the Test Plan to the relevant section of the Development Case. It might be both useful and sufficient to simply include a diagram or image depicting your test workflow.
More specific details of the individual testing tasks are defined in a number of different ways, depending on project culture; for example:
* defined as a list of tasks in this section of the Test Plan, or in an accompanying appendix
* defined in a central project schedule (often in a scheduling tool such as Microsoft Project)
* documented in individual, "dynamic" to-do lists for each team member, which are usually too detailed to be placed in the Test Plan
* documented on a centrally located whiteboard and updated dynamically
* not formally documented at all
Based on your project culture, you should either list your specific testing tasks here or provide some descriptive text explaining the process your team uses to handle detailed task planning and provide a reference to where the details are stored, if appropriate.
For Master Test Plans, we recommend avoiding detailed task planning, which is often an unproductive effort if done as a front-loaded activity at the beginning of the project. A Master Test Plan might usefully describe the phases and the number of iterations, and give an indication of what types of testing are generally planned for each Phase or Iteration.
Note: Where process and detailed planning information is recorded centrally and separately from this Test Plan, you will have to manage the issues that will arise from having duplicate copies of the same information. To avoid team members referencing out-of-date information, we suggest that in this situation you place the minimum amount of process and planning information within the Test Plan to make ongoing maintenance easier and simply reference the "Master" source material.]

## 9. Environmental Needs

Here the non human recources will be listed and shown.

### 9.1 Base System Hardware

The following table sets forth the system resources for the test effort presented in this Test Plan.

| Resource                                                                | Quantity | Name and Type |
|-------------------------------------------------------------------------|----------|---------------|
| Client Test PCs                                                         |          |               |
| - Include special configuration requirements                            |          | TBD           |
| Test Repository                                                         |          |               |
| - Network or Subnet                                                     |          | TBD           |
| Test Development Device                                                 |          | TBD           |

### 9.2 Base Software Elements in the Test Environment

The following base software elements are required in the test environment for this Test Plan.

| Software Element Name |  Type and Other Notes                        |
|-----------------------|----------------------------------------------|
| IntelliJ              | Test Runner / IDE                            |
| Mockito               | Unit testing library                         |
| Espresso              | UI testing library                           |
| Cucumber              | human readable test definitions              |


### 9.3 Productivity and Support Tools

n/a

### 9.4 Test Environment Configurations

n/a

## 11. Iteration Milestones

We want to keep over [50]% code coverage.

## 12. Risks, Dependencies, Assumptions, and Constraints

| Risk                                    | Mitigation Strategy                                           | Contingency (Risk is realized)                                                                              |
|-----------------------------------------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Test data proves to be inadequate.      |  Customer  will ensure a full set of suitable and protected test data is available. br/  Tester  will indicate what is required and will verify suitability of test data. | redefine test data review Test Plan and modify Components, consider Load Test Failure |

## 13. Management Process and Procedures

n/a
