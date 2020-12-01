---
layout: default
title: Create new poll
nav_order: 4
has_children: true
parent: Use cases
grand_parent: Project management
---
# Use Case Specification: Create new poll
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## 1. Create new poll
### 1.1 Brief Description
In this use case the user creates a new poll. A name for the poll and a publishing date must be entered.
### 1.2 Mockup
![Step 1](../../media/use-cases/create-new-poll/step-1.png)

## 2. Flow of Events
### 2.1 Basic Flow
![Activity diagram](../../media/use-cases/create-new-poll/activity-diagram.svg)

### 2.2 Feature Files
```gherkin
Feature: Create New Poll

  Scenario: Create new poll successfully
    Given User is logged in
    And  User has opened new poll item menu
    When I enter "my new poll" into input field with id "input-name"
    And I click button with id "btn-create"
    Then Notification with text "Poll successfully created" is displayed

  Scenario: Create new poll with empty name
    Given User is logged in
    And  User has opened new poll item menu
    When I enter "" into input field with id "input-name"
    And I click button with id "btn-create"
    Then Notification with text "Please enter a name" is displayed

```

### 2.3 Alternative Flows
n/a
## 3. Special Requirements
n/a
## 4. Preconditions
Following preconditions are needed:
- The user signed up.
## 5. Postconditions
The created poll must be saved on the server.
## 6. Extension Points
tbd
