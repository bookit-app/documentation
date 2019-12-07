# Testing Strategy

 - [Introduction](#Introduction)
 - [Scope](#Scope)
    - [In Scope](#In-Scope)
    - [Out of Scope](#Out-of-Scope)
 - [Quality Objective](#Quality-Objectives)
 - [Roles and Responsibilities](#Roles-and-Responsibilities)
 - [Assumptions and Limitations](#Assumptions-and-Limitations)
 - [Test Methodology](#Test-Methodology)
 - [Overview](#Overview)
 - [Test Levels](#Test-Levels)
 - [Bug Triage](#Bug-Triage)
 - [Test Completeness](#Test-Completeness)
 - [Test Deliverables](#Test-Deliverables)
 - [Resource & Environment Needs](#Resource-&-Environment-Needs)
 - [Testing Tools](#Testing-Tools)
 - [Test Environment](#Test-Environment)
 - [Terms/Acronyms](#Terms/Acronyms)

## Introduction

A Test Plan is a document which describes the scope of testing, Test strategy, objectives, efforts, schedule and resources required. Its main purpose is to guide the whole testing process.

### Scope

#### In Scope

Book IT mobile app functionality listed in the Functional Requirement Specification Document (FRS) will be tested as a part of entire Testing activity. This functionality includes:

- Client Account Creation
- Client Login
- Client Profile Maintenance
- Service Provider Searching
- Booking Appointment
- Update and Cancel Appointment
- Appointment History Review

#### Out of Scope

Requirements not included as part of the Book IT Functional Requirements document will not be tested in this testing effort Quality Objective

### Quality Objectives

- To ensure the Book IT mobile application confirms the functional and Non functional requirements.
- To ensure the Book IT mobile application bugs and issues are identified and fixed.

### Roles and Responsibilities

All the team members have equal contribution in different roles and responsibilities in a collaborative manner.

### Assumptions and Limitations

- Book IT mobile application considered to be compatible with mobile devices.
- All supporting systems (e.g., Internet Explorer, Microsoft Office Products) considered market-proven by the industry will not be validated.

## Test Methodology

### Overview

The testing for BookIT mobile application is conducted in Agile Methodology.

### Test Levels

- **Unit tests** are implemented for each repository. The unit tests are run in an automated fashion at various levels:

  - When code is committed the unit tests are automatically triggered. If they fail the commit is blocked. This is to ensure all changes are appropriate tested and that there are no unintended consequences.
  - When the Pull Request is opened on github the unit tests as well as linting is performed to ensure high quality of the code.

- **Integration, System, and Security tests** are implemented via a set of Postman collections and integrated with the CI/CD pipeline to be run periodically and automatically.
  - Refer to the [Integration Test Runner](https://github.com/bookit-app/integration-test-runner) for details on the scenarios, and what is currently covered.
  - Access to the integration tests are located in Cloud Build and can be accessed [here](https://console.cloud.google.com/cloud-build/builds?project=bookit-app-260021&query=tags%3D%20%22integration-tests%22). Note requires authenticated access to the GCP Project.

- **E2E Mobile Application Testing** are performed manually.

### Bug Triage

As the process of the triage, the resolution type and priority level for each bug is discussed and scheduled with a goal to Achieve maximum possible resolution.

### Test Completeness

- 100% unit test coverage confirmed through automated execution during build process and reported via Coverals within gitrepos
- Through backend end to end automated testing and verification with traceability
- All Manual & Automated Test cases executed
- All open bugs are fixed

## Test Deliverables

Following are the list of all the Test Artifacts that has been delivered at the during different phases of the testing lifecycle.

- Test Plan
- Unit test implementation within the code base
- Test Cases through Dev Azure
- Requirement Traceability Matrix
- Automated test report output: [Test Results Report](https://storage.cloud.google.com/bookit-integration-test-runner-output/report.html)
- Bug Reports

## Resource & Environment Needs

### Testing Tools

The tools that are used in Testing the Book IT Mobile application are as follows

- Requirements Tracking Tool - Azure Devops
- Bug Tracking Tool - Azure Devops
- Automation Tools 
    - Coveralls for coverage tracking
    - Postman and Newman nodeJS client for automated backend E2E tests

### Test Environment

The minimum **hardware** requirements that will be used to test the Application.

- \*Android or iOS Device

For automated testing Google Cloud Platform project with Cloud Build is required to automated execution

### Terms/Acronyms

Make a mention of any terms or acronyms used in the project

| TERM/ACRONYM | DEFINITION |
| --- | --- |
| API | Application Program Interface |
| AUT | Application Under Test |