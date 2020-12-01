# Live-Poll Software Requirements Specification

## Table of contents
1. [Introduction](#1-introduction)
    + [1.1 Purpose](#11-purpose)
    + [1.2 Scope](#12-scope)
    + [1.3 Definitions, Acronyms and Abbreviations](#13-definitions-acronyms-and-abbreviations)
    + [1.4 References](#14-references)
    + [1.5 Overview](#15-overview)
2. [Overall Description](#2-overall-description)
    + [2.1 Vision](#21-vision)
    + [2.2 Use Case Diagram](#22-use-case-diagram)
3. [Specific Requirements](#3-specific-requirements)
    + [3.1 Functionality](#31-functionality)
    + [3.2 Usability](#32-usability)
    + [3.3 Reliability](#33-reliability)
    + [3.4 Performance](#34-performance)
    + [3.5 Supportability](#35-supportability)
    + [3.6 Design Constraints](#36-design-constraints)
    + [3.7 Online User Documentation and Help System Requirements](#37-online-user-documentation-and-help-system-requirements)
    + [3.8 Purchased Components](#38-purchased-components)
    + [3.9 Interfaces](#39-interfaces)
    + [3.10 Licensing Requirements](#310-licensing-requirements)
    + [3.11 Legal Copyright and Other Notices](#311-legal-copyright-and-other-notices)
    + [3.12 Applicable Standards](#312-applicable-standards)
 4. [Supporting Information](#4-supporting-information)

## 1. Introduction
### 1.1 Purpose
This SRS describes all specifications and use cases for Live-Poll. Live-Poll is a live-polling application which elevates your presentation and lets you interact with your audience while presenting. This document includes a detailed description of the expected application functionalities as well as non-functionality requirements.

### 1.2 Scope
This SRS applies to the entire Live-Poll project. 

Actors: 
- Polling Creator: Person who creates and presents a poll.
- Polling Participant: Person who participates in a poll.

Subsystems:
- Admin Dashboard
- My Polls
- Poll
- Poll Item
- Presentation Mode
- Q&A
- User live participating mode

### 1.3 Definitions, Acronyms and Abbreviations
| Abbreviation |                                       |
| ----------- | -------------------------------------- |
| SRS         | Software Requirements Specification    |
| UCD         | Use Case Diagram                       |
| n/a         | not applicable                         |
| FAQ         | Frequently Asked Questions             |
| Q&A         | Question & Answers                     |

| Definition                          |     |
| ----------------------------------- | --- |
| Software Requirements Specification | Software Requirement Specification is a document, which captures the complete software requirements for the system, or a portion of the system. |
| Use case                            | A Use case is a list of actions or event steps, typically defining the interactions between a role (known in the Unified Modeling Language as an actor) and a system, to achieve a goal. |

### 1.4 References
|Title                                             |Date      |Publishing Organization|
|--------------------------------------------------|----------|-----------------------|
|[Live-Poll Blog](https://blog.live-poll.de)|2020-10-18|Live-Poll              
|[Live-Poll GitHub](https://github.com/livepoll)|2020-10-18|Live-Poll
|[UC Create multiple choice item](use-cases/create-multiple-choice-item/README.md)|2020-10-20|Live-Poll
|[UC Create new poll](use-cases/create-new-poll/README.md)|2020-10-20|Live-Poll
|[UC Create item](use-cases/create-item/README.md)|2020-12-01|Live-Poll
|[UC Login/Logout](use-cases/login-and-out/README.md)|2020-12-01|Live-Poll


### 1.5 Overview
The following chapters are structured in the following way: In the next chapter `Overall Description` our vision is described and the `Use Case Diagram` gives an overview over the expected functionality. The third chapter provides more detailed information about the requirements. First, the expected features of the Live-Poll application are presented. After that, further requirements like usability, reliability or performance are listed. In the last chapter you can find supporting information.
## 2. Overall Description
### 2.1 Vision
Live-Poll embodies the vision of an open-source live-polling application that you can use totally free, no matter if you’re a private person, school, university, society, small or big business etc. Our idea arose from the lack of free live voting/polling software on the Internet that has a nice user flow and is easy to use.

Live Poll will elevate your presentation and let you stand out from the crowd. It is an online tool allowing your audience to live-interact with the presenters, e.g. to answer questions, quizzes, multiple choice questions, word clouds and so much more.

### 2.2 Use Case Diagram
![Live-Poll Use Case Diagram](../media/live-poll-ucd.svg)
## 3. Specific Requirements
### 3.1 Functionality
This section lists and explains every functional requirement. Every subsystem from the UCD is represented through its own subsection.
#### 3.11 Admin Dashboard
On the landing page, the user can log in to Live-Poll or create a new account (Sign up). Having logged in, the user lands on the admin dashboard, the entry point of our application. Account settings can be managed here and the user can switch to the "My Polls" page.
#### 3.12 My Polls
On this page all polls are listed. The user can navigate to specific polls and edit or delete them. Also, new polls can be created here.
#### 3.13 Poll
On the Poll page a single poll can be edited and the user can start the presentation mode. In order to create and edit the poll, different poll items can be added. Furthermore, every poll owns a Q&A page which can be accessed from here too.
#### 3.14 Poll Item
The user can choose between following item types:
- Quiz
- Multiple choice
- Rating
- Open text
- Word cloud

Depending on the type selected, different details can be entered. In order to see how the poll item looks in the presentation, the presentation mode for an item can be entered directly from it.
#### 3.15 Presentation Mode
The poll items can be presented to the audience by entering the presentation mode. The presenter can switch between the prepared poll items and can show or hide their results. This mode also includes a view for Q&A questions. The questions to be shown are chosen by a moderator. The functionality for the moderation is explained in the next subsection.
#### 3.16 Q&A
The Q&A can be moderated on the Q&A page. Here, the moderator can select questions which should appear in the presentation and questions can be answered via text message.
#### 3.17 User live participating mode
This page can be accessed by participants via a customizable URL, QR code or an event ID that the user can enter on the landing page. The page shows the current poll item from the presentation and the user can enter his answer here.

### 3.2 Usability
Our goal is to build a modern and easy to use application. For participating users, a login won't be necessary, so that they don't need to register in order to take part of Live-Poll.
### 3.3 Reliability
We will try to reduce the server downtime to a minimum. Updates or other changes will be applied during nighttime.
### 3.4 Performance
Especially the page for the live participants should load fast. Many simultaneous inquiries must not reduce the speed.
### 3.5 Supportability
To be able to test and publish updates quickly, we use docker containers. This also allows for better scaling possibilities.
### 3.6 Design Constraints
The Angular frontend should implement the MVC pattern.
There should be a RESTful API for communication between client and server. We've chosen to use the Spring framework for our backend.
### 3.7 Online User Documentation and Help System Requirements
To make the application easy to understand, we will create a FAQ that is easily accessible on the landing page.
### 3.8 Purchased Components
A server will be rent to run the application.
### 3.9 Interfaces
#### 3.9.1 User Interfaces
n/a
#### 3.9.2 Hardware Interfaces
n/a
#### 3.9.3 Software Interfaces
Our application will support all common browsers (Chrome, Opera, Firefox). The Internet Explorer will not be supported. We will offer an interface to communicate with applications included in the Microsoft Office suite.
#### 3.9.4 Communication Interfaces
For the communication between client and server, we will use the HTTPs protocol together with Web Sockets.
### 3.10 Licensing Requirements
We will deploy our app under the MIT license.
### 3.11 Legal Copyright and Other Notices
The Live-Poll team will not take responsibility for incorrect or lost data. Our app will be compliant with all GDPR regulations.
### 3.12 Applicable Standards
The following code standards are going to be applied to the code as far as possible:

1. Intuitive names of variables and methods (camel case) 
2. Use of comments to make code easy to understand
3. Each method is responsible for one task

## 4. Supporting Information
For more information visit our [blog](https://blog.live-poll.de) or contact us: contact@live-poll.de

© Live-Poll 2020
