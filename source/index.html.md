---
title: API 3.1 InteDashboard

language_tabs: # must be one of https://git.io/vQNgJ
  - php: PHP

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - authentication
  - roles
  - users
  - accounts
  - courses
  - modules
  - questions
  - errors

search: true
---

# Introduction

The *API Service* for **InteDashboard™** is available on [GitHub](https://github.com/orgs/CognaLearn/dashboard). The repository named **api3-dev.intedashboard.com**. 

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique. Vestibulum tincidunt rhoncus sapien ut rutrum. Mauris vel nibh id elit dictum gravida. Maecenas tincidunt et lacus vel vestibulum.  

## Objective
Listed below are the following objectives that will be accomplished through out this documentation.

* To setup project environment.
* To familiarized on the resources and data structure.
* Others...


## Project Setup
These setups are required to successfully utilised the API InteDashboard in local environment.

* Pull latest repo and install composer **(composer install)**
* Run migration and seeder command **(php artisan migrate:refresh --seed)**
* Setup .env file

## Principles
To support the objective of this documentation, here are the following priniciples that will serve as guidance while using this documentation.

* **Base URL**

    `https://api3-dev.intedashboard.com/api/v1`

* **Standard HTTP Get Parameters** - These parameters are standard for all **list** resources.

Parameter | Type | Description
--------- | ------- | -----------
`page` | **int** | Pagination page number.
`per_page` | **int** | Constrains the number of rows returned.
`sort` | **string** | Column name to be sorted.
`order` | **string** | `ASC` or `DESC`
`q` | **string** | Value to be searched.

* **Archived and Trashed Records** 

<aside class="notice">
By default, <b>archived</b> and <b>trashed</b> records are not included in returned list. To manage the data to be returned by <b>LIST</b> resource, following parameters can be used to show and hide archived and trashed records:
<br/> <br/>

<code>isArchived=*</code> <br/>
Returns all records whether archived or not.<br/><br/>

<code>isArchived=true</code> or <code>isArchived=1</code> <br/>
Returns archived records only.<br/><br/>

<code>isArchived=false</code> or <code>isArchived=0</code> <br/>
Returns unarchived records only.<br/><br/>

<code>isTrashed=*</code> <br/>
Returns all records whether trashed or not.<br/><br/>

<code>isTrashed=true</code> or <code>isTrashed=1</code> <br/>
Returns trashed records only.<br/><br/>

<code>isTrashed=false</code> or <code>isTrashed=0</code> <br/>
Returns untrashed records only.<br/><br/>
</aside>

* **Default roles** - Super Admin, Account Admin, Teacher, and Student

* **Super Admin User** - A permanent default user.
    * *identity* - bodwyer
    * *email* - brian@cognalearn.com
    * *password* - brian@cognalearn.com
    * *firstname* - Brian
    * *lastname* - O’Dwyer
    * *uuid* - [varies in every migration]
    
* Generated token as one of the request headers

    `Authorization: Bearer $token`

* Complete list of routers can be found at [Router](#routers). This routes will be used for permission setup per role

* Permission/route setup per role (as parameter)

    `"routers": [ "App\Http\Controllers\RoleController@index" ]`

* **UUID** property will be used as a reference id in URI

    `your-local/roles/7a066d34-abb9-4874-8264-353e3bc451fd`





## Unit Test
Automated testing objective is to segregate each part of the program and test that the individual parts are working correctly. **InteDashboard™** provides unit tests to help users/developers better manage and control the following modules: 

* **Account** - `AccountTest`
* **Course** - `CourseTest`
* **Module** - `ModuleTest`
    

<aside class="notice">
To run tests, run the following scripts in your terminal:

<br/>
<code>phpunit</code> - To run the entire tests.
 
<br/>
<code>phpunit --filter {TestMethodName}</code> - To run specific test. 
</aside>




## Standard Roles
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam sed nibh nec tellus vestibulum commodo. Mauris tincidunt arcu id congue dapibus. Cras in odio nec elit viverra gravida. Phasellus placerat sed nulla eu gravida. Pellentesque ligula elit, dictum quis dictum quis, consequat sit amet justo.

ID | Name | Description
------- | ------- | -----------
`1` | **Superuser** | People who work at CognaLearn.
`2` | **Account Admin** | Every Account has an Admin Teacher who has full access to the Account.
`3` | **Teacher** | Lorem ipsum dolor sit amet.
`4` | **Student** | Lorem ipsum dolor sit amet.

<aside class="notice">
Each role has several permissions. To update the certain role with certain permissions, proceed to Roles.
</aside>