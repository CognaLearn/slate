---
title: API 3.1 InteDashboard

language_tabs: # must be one of https://git.io/vQNgJ
  - php: PHP

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
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
    
* Email stored in **lumen.log** once account admin has been created during account creation.

## Content [TO BE UPDATED]

Items that are included in this document are the following:

* Authentication and Token Generation
* Role and Permission Management
* Security Question Management
* Account and User (Account Admin) Management
* Profile Viewing





# Authentication

> To authorize, use this code:

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
```

> Make sure to replace `$token` with your personal token.

Kittn uses API keys to allow access to the API. You can register a new Kittn API key at our [developer portal](http://example.com/developers).

Kittn expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: Bearer $token`

<aside class="notice">
Replace <code>$token</code> with your personal token.
</aside>


