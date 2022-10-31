# T2A2 - API Webserver Project


Project: An admin portal for a start up Landscaping Business.

1. [Link to Project Documentation](https://docs.google.com/document/d/1_dzeT4baEx9C4u5cQbMgJiJ_pbRsguKYKNvxqlA5ojc/edit?usp=sharing)


2. [Link to Project Tracking (Trello)](https://trello.com/invite/b/06cHHz3x/ATTI6045b9cf1328ade946408c89e0871c76D3A87865/api-web-server-project)

3. [Virtual WhiteBoard](https://miro.com/app/board/uXjVPVaYOmE=/)

____________________________________

## Table of Contents

### Project Overview 
* [Introduction](#introduction)
* [Brief](#brief) 

### Project Planning
With the use of Trello, the project is tracked in Phases

[Phase 1: Design of Database](#phase1)

* [Requirement 1](#req1)
* [Requirement 2](#req2)
* [Requirement 3](#req3)
* [Requirement 4](#req4)
* [Requirement 5](#req5)
* [Requirement 6](#req6)
* [Requirement 7](#req7)
* [Requirement 8](#req8)
* [Requirement 9](#req9)
* [Requirement 10](#req10)

[Phase 2: Software Development Plan](#phase2)
1. Overview of Project
2. Set Up (incl. Third Party Dependencies)
3. Development
4. CRUD (Create, Read, Update, Delete)
5. Authorisation and Authentication
6. Validation and Error Handling
7. Testing 
8. Deployment 


### Resources
* Important Links
* References


____________________________________

# Project Overview

## Introduction<a name="introduction"></a>
To solidify your knowledge of core web server concepts and show your ability to work with web servers at a fundamental level, you should be able to write code to create a functioning web API server.

## Brief<a name="brief"></a>
Design a functioning web server in the relevant programming language. Your web server must contain valid, functioning code and adhere to the following requirements:

**Requirements**

1. Planning
2. Code

____________________________________

# Project Planning
[Link to Project Tracking (Trello)](https://trello.com/invite/b/06cHHz3x/ATTI6045b9cf1328ade946408c89e0871c76D3A87865/api-web-server-project)


## Phase 1: Design of Database<a name="phase1"></a>

**Documentation Requirements**

Complete a planning stage before developing the application, which requires the development of these items:
* An entity relationship diagram (ERD) that represents the normalised relational database to be used in this web server
* An explanation of the ERD, with reference to the models and associations to be used with the web server
* An explanation of the chosen database system, including comparisons to other types of database systems
* A software development plan


## Requirement 1<a name="req1"></a>
**Identification of the problem you are trying to solve by building this particular app.**

Recently I have picked up the hobby of gardening.
The opportunity I want to create is to start a side business where I can offer my services of maintaining a garden for someone else.

The **problem** I want to solve with the API Webserver Project is to build an Admin portal for a Landscaping business.

"As a Business Owner

I want to create a admin portal for a Landscaping business

So that I can track customers, jobs and invoicing"

_

## Requirement 2<a name="req2"></a>
**Why is it a problem that needs solving?**

There are other methods to start a customer database, however I can imagine it would create more problems in the future as the business grows.
If I did not create a database, It would be difficult to expand. Such as tracking customers, add staff and invoicing would be very difficult and time consuming. 

To make sure I am on the right track that this is a problem that needs solving, I asked myself (as the potential business owner) the following question:

“How will I use this API?”.

What does it need to do? Below is a list of requirements.

**Landscaping Business - Build a API Web Server Admin Portal:**

* Log in (securely) - To protect myself and my customer information.
* Enter in a new customer
* Search for an existing customer
* Book a job for a customer
* Select the type of job for the customer
* Add a new user to access the Admin Portal
* Update a job (update/ cancel)
* Invoice a customer from their completed job

Already from the list above, if this was done manually, it would create human errors.

This is a problem I want to solve as a future business owner that expects this business to grow successfully and ensure privacy/security of data.

_

## Requirement 3<a name="req3"></a>
**Why have you chosen this database system. What are the drawbacks compared to others?**

The chosen database for this project is a **Relational Database Management System**.

Reason for this type of database is that it is characterized by its intuitive relationships of representing data in tables. Especially for a business where the importance of data integrity is integral.

However without reviewing other types of databases I wouldn’t have been able to come to this conclusion.

A comparison between a Relational Database Management System and a Non-Relational Database Management System, the only drawback I could find is the potential complexity of a relational database. Especially when it comes to storing data in a tabular form, which can make it difficult to represent complex relationships between objects.

![Comparing Relational Database Management Systems](/images/DBMS_Compare.png)

Image from Medium, 2020, "Document vs Relational Databases"

However there are more advantages in this case to use a Relational Database Management System than any other database management system due the nature of the data for this project.

_

## Requirement 4<a name="req4"></a>
**Identify and discuss the key functionalities and benefits of an ORM**

ORM, Object Relational Mapping refers to a library that implements the technique to write the query in your chosen programming language rather than relying on SQL to execute a query.

Even though there is still a need for a fundamental understanding of SQL and databases when using an ORM.

Benefits of an ORM are:

* That you can write in your chosen programming language. In this case using Python as the Programming Language.
* Abstracts away from the database system so that there is no need to switch from MySQL to PostgreSQL.
* There are a lot of advanced features that support transactions, connection pooling, migratations, and seeds as an example.
  
In this project, the ORM we will be using is **SQLAlchemy**.

_

## Requirement 5<a name="req5"></a>
**Document all endpoints for your API**



_


## Requirement 6<a name="req6"></a>
**An ERD for your app**

![Entity Relational Diagram of Landscaping ADMIN database](Assignments/T2A2-API/images/Landscaping_T2A2.png)
_


## Requirement 7<a name="req7"></a>
**Detail any third party services that your app will use**

_

## Requirement 8<a name="req8"></a>
**Describe your projects models in terms of the relationships they have with each other**

Cardinality defines the numerical attributes of the relationship between two entities.

Different types of cardinal relationships are:
* One-to-One Relationships
* One-to-Many Relationships
* Many-to-Many Relationships

**Cardinality**

1. Customers book a Service
- Customers book Services that requires a Reference Id (to track the status) (One-to-Many relationship)
- A customer can request multiple quotes, or have a quote and a job in progress or completed.
- There can only be one Reference of a job per customer

2. Service (lawn care/garden care) belong to a Reference of a Job
- A Service belongs to a Reference of the Job (For the customer). 
- A customer can requesr lawn care and or garden care.
- One to many (One service (lawn care and or garden care) on the Reference of the job, otherwise it becomes another job.

3. Reference status belongs to a Reference of a job.
- A reference status can belong to a reference of a job, one at a time (this is a one to one relationship).
- A reference of a job can not be in progress and completed at the same time.
  
4. An Employee belongs to a Reference of a job
- An Employee belongs to a Reference of a job. 
- An employee can have a many-to-many relationship with reference of a job.
- An employee can quote a job and own that reference, they can be in progress of a job and then can have completed a job.
_

## Requirement 9<a name="req9"></a>
**Discuss the database relations to be implemented in your application**

_

## Requirement 10<a name="req10"></a>
**Describe the way tasks are allocated and tracked in your project**

Through the use of a task management system called Trello, the project is tracked.

[Link to Project Tracking (Trello)](https://trello.com/invite/b/06cHHz3x/ATTI6045b9cf1328ade946408c89e0871c76D3A87865/api-web-server-project)

Split out into two Phases.

**Phase 1**

Is for Designing the API Web Server. Documenting requirements from 1 to 10. This is part of planning the project before Development can commence.

**Phase 2**

Is for Development of the API Web Server. With the foundations of the design clearly identified, the development can begin.

Tracking of the project includes:

Columns in Trello:

* High Level Project Requirements: All the other columns would need to be completed before these high level project requirements are marked as done. This would be considered the epics of the project.
* Phase 1 - Design Backlog: Initial steps of understanding what needs to be built and why. By working through these initial requirements, the project is understood and designed, database identified, documented and any additional requirements considered.
* Phase 2 - Development Backlog: With a focus on the OOP programming paradigm, this column is for development cards.
* In Progress: Actively working on the card in this column, to complete the acceptance criteria.
* Testing: During development, Test Driven Development is considered. The development cards include the testing so that it is a continuous process. Including unit testing and end to end testing manually as a sanity check/ regression testing.
* Completed/Done: All acceptance criteria in the card is marked as completed, then the card can be moved to this column and progress tracked.

_ 


# Development

## Phase 2: Software Development Plan<a name="phase2"></a>

