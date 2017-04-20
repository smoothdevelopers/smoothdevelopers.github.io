---
title: API Reference

language_tabs:
- bash
- javascript

includes:

search: true

toc_footers:
- <a href='http://github.com/mpociot/documentarian'>Documentation Powered by Documentarian</a>
---
<!-- START_INFO -->
# Info

Welcome to the generated API reference.
[Get Postman Collection](http://localhost/docs/collection.json)
<!-- END_INFO -->

#User

This module will handle all the user manipulation including:
1. Registration  - with Facebook or email and password.
2. Authentication - with Facebook ID or email and password.
3. User details - access to logged in user&#039;s details.
4. Assigning tokens - will assign new API access tokens for
    an already logged in user.

Note: for all the those routes marked with Auth Required,
       the following headers must be passed:
 + &#039;Accept&#039; =&gt; &#039;application/json&#039;
 + &#039;Authorization&#039; =&gt; &#039;Bearer &#039; + { logged in user&#039;s token }

Please ensure you have the space after the &#039;Bearer &#039; value of the &#039;Authorization&#039;
header e.g. &#039;Bearer eyJ0eXAiOiJKV1QiL...&#039;
<!-- START_9b706bcb7d78cfacbf8e5e3e7d8afe2b -->
## Register with email and password.

Will register the user with an email and password.

> Example request:

```bash
curl -X POST "http://localhost//api/user/register" \
-H "Accept: application/json" \
    -d "name"="ab" \
    -d "email"="ward.faye@example.com" \
    -d "password_confirm"="ab" \
    -d "password"="ab" \
    -d "profile_pic"="ab" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/user/register",
    "method": "POST",
    "data": {
        "name": "ab",
        "email": "ward.faye@example.com",
        "password_confirm": "ab",
        "password": "ab",
        "profile_pic": "ab"
},
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```


### HTTP Request
`POST /api/user/register`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    name | string |  required  | Maximum: `255`
    email | email |  optional  | Maximum: `255`
    password_confirm | string |  required  | Minimum: `6`
    password | string |  required  | Minimum: `6`
    profile_pic | image |  optional  | Must be an image (jpeg, png, bmp, gif, or svg)

<!-- END_9b706bcb7d78cfacbf8e5e3e7d8afe2b -->

<!-- START_5aa3d01db2b9d4c6a5d0d1ee7c426bd8 -->
## Register with Facebook

Will register a user using their Facebook ID.

> Example request:

```bash
curl -X POST "http://localhost//api/user/register_fb" \
-H "Accept: application/json" \
    -d "name"="id" \
    -d "fb_id"="id" \
    -d "profile_pic"="id" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/user/register_fb",
    "method": "POST",
    "data": {
        "name": "id",
        "fb_id": "id",
        "profile_pic": "id"
},
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```


### HTTP Request
`POST /api/user/register_fb`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    name | string |  required  | Maximum: `255`
    fb_id | string |  required  | 
    profile_pic | image |  optional  | Must be an image (jpeg, png, bmp, gif, or svg)

<!-- END_5aa3d01db2b9d4c6a5d0d1ee7c426bd8 -->

<!-- START_96e41001d85ca072dc79e94397b6f2e3 -->
## Login with email and password.

Will login a user with their email and password.

> Example request:

```bash
curl -X POST "http://localhost//api/user/login" \
-H "Accept: application/json" \
    -d "email"="joanne.muller@example.com" \
    -d "password"="ut" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/user/login",
    "method": "POST",
    "data": {
        "email": "joanne.muller@example.com",
        "password": "ut"
},
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```


### HTTP Request
`POST /api/user/login`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    email | email |  required  | 
    password | string |  required  | 

<!-- END_96e41001d85ca072dc79e94397b6f2e3 -->

<!-- START_5185b1c08ff9fc05d72653d65ed7ed67 -->
## Login with Facebook ID.

Will login a user with their Facebook ID.

> Example request:

```bash
curl -X POST "http://localhost//api/user/login_fb" \
-H "Accept: application/json" \
    -d "fb_id"="sed" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/user/login_fb",
    "method": "POST",
    "data": {
        "fb_id": "sed"
},
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```


### HTTP Request
`POST /api/user/login_fb`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    fb_id | string |  required  | 

<!-- END_5185b1c08ff9fc05d72653d65ed7ed67 -->

<!-- START_9c9260bd1ad91eb9aa21477f56d5ad8b -->
## User details.

Note: Auth Required

Returns all the details of the currently logged in user.

> Example request:

```bash
curl -X GET "http://localhost//api/user/get" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/user/get",
    "method": "GET",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```

> Example response:

```json
null
```

### HTTP Request
`GET /api/user/get`

`HEAD /api/user/get`


<!-- END_9c9260bd1ad91eb9aa21477f56d5ad8b -->

<!-- START_25677b2fefca9a1f80499c00e4c4acf7 -->
## Refresh token

Note: Auth Required

This will refresh current logged in users token

> Example request:

```bash
curl -X GET "http://localhost//api/user/refresh_token" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/user/refresh_token",
    "method": "GET",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```

> Example response:

```json
null
```

### HTTP Request
`GET /api/user/refresh_token`

`HEAD /api/user/refresh_token`


<!-- END_25677b2fefca9a1f80499c00e4c4acf7 -->

<!-- START_99dabfc22a317a2385dee642272a537e -->
## Update user details.

Note: Auth Required.

This will update the details of an already logged in user.

> Example request:

```bash
curl -X POST "http://localhost//api/user/update" \
-H "Accept: application/json" \
    -d "token"="culpa" \
    -d "name"="culpa" \
    -d "profile_pic"="culpa" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/user/update",
    "method": "POST",
    "data": {
        "token": "culpa",
        "name": "culpa",
        "profile_pic": "culpa"
},
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```


### HTTP Request
`POST /api/user/update`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    token | string |  required  | 
    name | string |  required  | Maximum: `255`
    profile_pic | image |  optional  | Must be an image (jpeg, png, bmp, gif, or svg)

<!-- END_99dabfc22a317a2385dee642272a537e -->

<!-- START_a93d6745597660d48aea8c2249b67600 -->
## Update user password

Note: Auth Required.

This will update the password of an already logged in user. This user
must have been registered using an email and password.

> Example request:

```bash
curl -X POST "http://localhost//api/user/update_password" \
-H "Accept: application/json" \
    -d "token"="dicta" \
    -d "old_password"="dicta" \
    -d "password_confirm"="dicta" \
    -d "password"="dicta" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/user/update_password",
    "method": "POST",
    "data": {
        "token": "dicta",
        "old_password": "dicta",
        "password_confirm": "dicta",
        "password": "dicta"
},
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```


### HTTP Request
`POST /api/user/update_password`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    token | string |  required  | 
    old_password | string |  required  | Minimum: `6`
    password_confirm | string |  required  | Minimum: `6`
    password | string |  required  | Minimum: `6`

<!-- END_a93d6745597660d48aea8c2249b67600 -->

<!-- START_8e2bcf97ca2b0da97a00d74ce5c0dddc -->
## Logout the user.

Note: Auth Required.

Will logout the logged in user and close the session.
The token is required.

> Example request:

```bash
curl -X POST "http://localhost//api/user/logout" \
-H "Accept: application/json" \
    -d "token"="quia" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/user/logout",
    "method": "POST",
    "data": {
        "token": "quia"
},
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```


### HTTP Request
`POST /api/user/logout`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    token | string |  required  | 

<!-- END_8e2bcf97ca2b0da97a00d74ce5c0dddc -->

<!-- START_901f22c468bb4f7946c10670b088ad93 -->
## Close user account.

Note: Auth Required.

This will close the logged in user's account by soft deleting it.

> Example request:

```bash
curl -X POST "http://localhost//api/user/close_account" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/user/close_account",
    "method": "POST",
    "headers": {
        "accept": "application/json"
    }
}

$.ajax(settings).done(function (response) {
    console.log(response);
});
```


### HTTP Request
`POST /api/user/close_account`


<!-- END_901f22c468bb4f7946c10670b088ad93 -->

