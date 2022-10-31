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
*Through the use of Trello, the project is tracked in Phases*

[Phase 1: Project Planning](#phase1)

* [Requirement 1](#req1)
* [Requirement 2](#req2)
* [Requirement 3](#req3)
* [Requirement 4](#req4)


* Phase 2: Design of Database
* Phase 3: Development (Software Development Plan)
* Phase 4: Testing 

(*Phase 3, see Software Development Plan*)

### Software Development Plan
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


## Phase 1: Project Planning<a name="phase1"></a>

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

This is a problem to solve I want to solve as a future business owner that expects this business to grow successfully.

_

## Requirement 3<a name="req3"></a>
**Why have you chosen this database system. What are the drawbacks compared to others?**

The chosen database for this project is a **Relational Database Management System**.

Reason for this type of database is that it is characterized by its intuitive relationships of representing data in tables. Especially for a business where the importance of data integrity is integral.

However without reviewing other types of databases I wouldn’t have been able to come to this conclusion.

A comparison between a Relational Database Management System and a Non-Relational Database Management System, the only drawback I could find is the potentia complexity of a relational database. Especially when it comes to storing data in a tabular form, which can make it difficult to represent complex relationships between objects.

However there are more advantages in this case to use a Relational Database Management System than any other database management system due the nature of the data for this project.
_

## Requirement 4<a name="req4"></a>
**Identify and discuss the key functionalities and benefits of an ORM**

ORM, Object Relational Mapping refers to a library that implements the technique to write the query in your chosen programming language rather than relying on SQL to execute a query.

Even though there is still a need for a fundamental understanding of SQL and databases when using an ORM.

Benefits of an ORM is:

* That you can write in your chosen programming language
* Abstracts away from the database system so that there is no need to switch from MySQL to PostgreSQL
* There are a lot of advanced features that support transactions, connection pooling, migratations, and seeds as an example.
  
In this project, the ORM we will be using is **SQLAlchemy**.
