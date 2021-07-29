# Simple MD File

This version was created using spotlight.io with the source YAML spec kept in GitHub (twilb1/spotlight). It looks like there is bidirectional syncing, that is, you can make changes in spotlight.io and they are reflected in Github or you can make changes to a Github file and the canges are reflected in spotlight.io. 

Technically Write IT (TWi) Ltd. provides an example service to demonstrate a real-world REST API in action. Clients can send HTTP requests to service endpoints and receive responses. This document describes the Application Programming Interface (API) that enables client-side application developers to communicate with the service.

Using the API, developers can perform Create, Read, Update, and Delete (CRUD) operations on database objects using the following REST API requests:

  - GET requests - to read information from the database tables

  - POST requests - to create records in database tables

  - PUT requests - to update records in database tables

  - DELETE requests - to delete records from the database tables

This document describes the details of the requests that can be issued including:

  - The type of the request

  - Required and optional parameters

  - Limitation of parameters, such as the length of a parameter string

  - Status codes that indicate if the request was successful or resulted in an error

  -   Error messages

## Application Database

To demonstrate REST API capabilities we are using the sample database that comes with SQLite. SQLite is a software library that provides a relational database management system and is popular for developing small-scale applications.

![SQLite Tutorial Database Entity-Relationship (ER) Diagram](https://twiapi.herokuapp.com/images/SQLite_Tutorial_DB.jpg)

Leanne was here! Testing editing

## Getting Started

Getting started could not be simpler! To get information about all the customers registerd in the database enter the following command in your favorite browser: 

  https://twiapi.herokuapp.com/api/customers

You get a response in JavaScript Object Notation (JSON) format showing the details of each customer in the database.

Similarly, to get information about all the employees in the database, enter the following command in your favorite browser:

  https://twiapi.herokuapp.com/api/employees

You get a response in JSON format showing the details of each employee in the database.

In a browser URL, it is only possible to issue GET requests. To issue more complicated REST requests, you can use a tool called `Postman`.

## Using Postman

Postman is an online platform that allows API developers to collaborate on the development of REST API applications. The part we are most interested in is the [Postman API Client](https://www.postman.com/product/api-client).

We can use this client to send all types of requests to our REST API (or any REST API) and view the responses, status codes, and error messages. It is the ideal tool for REST API testing.

The Postman API Client is freely available from the [download](https://www.postman.com/downloads/) page.

The Postman API Client user interface is quite intuitive, but to help you get started, check out Postman's own [documentation](https://learning.postman.com/docs/postman/launching-postman/introduction/).

## Managing Information in the Database

You can use the TWi REST API for:

  - [Customer Management](#section/Customer-Management)

  - [Employee Management](#section/Employee-Management)

## Customer Management

You can view and edit the information retained in the database for customers. This information includes:

  - Customer ID

  - First Name (required)

  - Last Name (required)

  - Company

  - Address

  - City

  - State

  - Country

  - Postal Code

  - Phone

  - Fax

  - Email (required)

  - Support Representative ID

The Customer ID is generated automatically by the database, and it cannot be changed. Attempting to do so results in an error.

The First Name, Last Name, and Email are required fields, so you must specify them when adding a new customer. If you do not specify these fields when adding a customer, you receive an error.

The Support Representative ID is the ID of an employee that is assigned to the customer.

Using the TWi REST API, you can:

  - [View details of all customers](https://twi.stoplight.io/docs/twi-rest-api-reference/b3A6MTY3OTg2NTQ-view-details-of-all-customers)

  - [View details of a single customer](#operation/post-customer) 

  - [Add a new customer](#operation/post-customer)

  - [Edit customer details](#operation/put-customer-info)

  - [Delete a customer](#operation/del-customer)

## Employee Management

You can view and edit the information retained in the database for employees. This information includes:

  - Employee ID

  - Last Name (required)

  - First Name (required)

  - Title

  - Reports To

  - Birth Date

  - Hire Date

  - Address

  - City

  - State

  - Country

  - Postal Code

  - Phone

  - Fax

  - Email (required)

The Employee ID is generated automatically by the database, and it cannot be changed. Attempting to do so results in an error.

The First Name, Last Name, and Email are required fields, so you must specify them when adding a new employee. If you do not specify these fields when adding an employee, you receive an error.

The Reports To parameter is the ID of an employee that the employee reports to.

Using the TWi REST API, you can:

  - [View details of all empoloyees](#operation/get-api-employee)

  - [View details of a single employee](#operation/get-api-employees-Id)

  - [Add a new employee](#operation/post-api-employees)

  - [Edit empoloyee details](#operation/put-api-employees-EmployeeId)

  - [Delete an employee](#operation/del-api-employees-EmployeeId)
