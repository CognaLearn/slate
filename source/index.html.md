---
title: API 3.1 InteDashboard

language_tabs: # must be one of https://git.io/vQNgJ
  - json: PHP
<!-- - json--wb: Winterbreak -->

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - authentication
  
search: true
---


# Introduction

The *API Service* for **InteDashboard™** is available on [GitHub](https://github.com/orgs/CognaLearn/dashboard). The repository named **api3-dev.intedashboard.com**. 

## Principles
To support the objective of this documentation, here are the following priniciples that will serve as guidance while using this documentation.

* **Base URL**

    `uat.intedashboard.com/v2`

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

* **Standard Request Headers** - These values are standard for **authenticated** resources.

Key | Value | Description
--------- | ------- | -----------
`Content-Type` | **application/json** | Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean vel nibh vel nisl iaculis tristique.
`Authorization` | **Bearer $token** | Lorem ipsum dolor sit amet, consectetur adipiscing elit.

<aside>
Generated token will be included in the value of <b>Authorization</b> key of <i>Request Headers</i>.
<br/>
<code>Authorization: Bearer $token</code>
</aside>


* **UUID** property will be used as a reference id in URI

    `your-local/roles/7a066d34-abb9-4874-8264-353e3bc451fd`







## Standard Roles
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam sed nibh nec tellus vestibulum commodo. Mauris tincidunt arcu id congue dapibus. Cras in odio nec elit viverra gravida. Phasellus placerat sed nulla eu gravida. Pellentesque ligula elit, dictum quis dictum quis, consequat sit amet justo.

ID | Name | Description
------- | ------- | -----------
`1` | **Superuser** | A user with special privileges needed to administer and maintain the system.
`2` | **Account Admin** | Responsible for reviewing and reconciling courses data in a certain organisation, processing setups and maintaining updated records of Teachers within the organisation.
`3` | **Teacher** | A user that manages course, module, activity and student data.
`4` | **Student** |




# HTTP Status Codes

API 3.1 InteDashboard use conventional HTTP response codes to indicate the success or failure of an API request. In general, codes in the 2xx range indicate success, codes in the 4xx range indicate an error caused by the information provided (i.e., a required parameter was omitted, a method was not found, etc.), and codes in the 5xx range indicate an error with servers.

Status Code | Status Text | Description
------- | ------- | -----------
`200` | **OK** | The request has succeeded. The meaning of a success varies depending on the HTTP method: <br/><br/>GET: The resource has been fetched and is transmitted in the message body. <br/><br/> POST: The resource describing the result of the action is transmitted in the message body
`201` | **Created** |	The request has succeeded and a new resource has been created as a result of it. This is typically the response sent after a PUT request.
`202` | **Accepted** | The request has succeeded and has been added to the queue, but the resource has not yet been created. This is typically the response sent after PUT and POST requests.
`204` | **No Content** | There is no content to send for this request. This is common for DELETE requests.
`307` | **Temporary Redirect** | The target resource resides temporarily under a different URI and the user agent MUST NOT change the request method if it performs an automatic redirection to that URI.
`400` | **Bad Request** | This response means that server could not understand the request due to invalid syntax.
`401` | **Unauthorized** | Authentication is needed to get requested response. This is similar to 403, but in this case, authentication is possible.
`403` | **Forbidden** | Client does not have access rights to the content so server is refusing to give proper response.
`404` | **Not Found** | Server cannot find the requested resource.
`405` | **Method Not Found** | The request method is known by the server but has been disabled and cannot be used. Double check your method type (i.e. GET, POST, PUT, DELETE)
`409` | **Conflict** | This response would be sent when a request conflicts with the current state of the server.
`429` | **Too Many Requests** | The user has sent too many requests in a given amount of time (“rate limiting”).
`499` | **Internal Server Error** | The server has encountered an internal error.
`500` | **Internal Server Error** | The server has encountered a situation it doesn’t know how to handle.
`502` | **Bad Gateway** | The server, while acting as a gateway or proxy, received an invalid response from an inbound server it accessed while attempting to fulfill the request.
`503` | **Service Unavailable** | The server is not ready to handle the request. Common causes are a server that is down for maintenance or that is overloaded.
`504` | **Gateway Timeout** | This error response is given when the server is acting as a gateway and cannot get a response in time.
