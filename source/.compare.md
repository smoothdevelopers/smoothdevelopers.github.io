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
    -d "gender"="male" \
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
        "gender": "male",
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
    gender | string |  required  | `male` or `female`
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
    -d "gender"="female" \
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
        "gender": "female",
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
    gender | string |  required  | `male` or `female`
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

This will refresh current logged in users token and return the new token

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
    -d "gender"="female" \
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
        "gender": "female",
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
    gender | string |  required  | `male` or `female`
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

#Wedding

This module will handle creation, access, update and desctruction of
weddings :)

Note: for a wedding to be created, we only require to have a couple and
      these two have to have created an account with us.
<!-- START_215c692433fd2245de4a7294ed03897c -->
## Get one public wedding.

Returns a public wedding given its id as a parameter.

> Example request:

```bash
curl -X GET "http://localhost//api/wedding/get_other/{wedding}" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/wedding/get_other/{wedding}",
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
`GET /api/wedding/get_other/{wedding}`

`HEAD /api/wedding/get_other/{wedding}`


<!-- END_215c692433fd2245de4a7294ed03897c -->

<!-- START_cd40717ee2c509069af7ed5b3b270140 -->
## Get public weddings by page.

Return all public weddings in pages with every page having 15 weddings.

> Example request:

```bash
curl -X POST "http://localhost//api/wedding/get_pages" \
-H "Accept: application/json" \
    -d "page"="817450" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/wedding/get_pages",
    "method": "POST",
    "data": {
        "page": 817450
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
`POST /api/wedding/get_pages`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    page | integer |  required  | 

<!-- END_cd40717ee2c509069af7ed5b3b270140 -->

<!-- START_c1656cf4b0c0abf54a59393b6903898d -->
## Create wedding.

Note: Auth Required.

This will create a wedding between two app users and returns the wedding
id on success.

> Example request:

```bash
curl -X POST "http://localhost//api/wedding/create" \
-H "Accept: application/json" \
    -d "groom_id"="46398" \
    -d "bride_id"="46398" \
    -d "description"="rerum" \
    -d "venue"="rerum" \
    -d "reception"="rerum" \
    -d "venue_lat"="46398" \
    -d "venue_lng"="46398" \
    -d "reception_lat"="46398" \
    -d "reception_lng"="46398" \
    -d "when"="46398" \
    -d "is_public"="1" \
    -d "image"="rerum" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/wedding/create",
    "method": "POST",
    "data": {
        "groom_id": 46398,
        "bride_id": 46398,
        "description": "rerum",
        "venue": "rerum",
        "reception": "rerum",
        "venue_lat": 46398,
        "venue_lng": 46398,
        "reception_lat": 46398,
        "reception_lng": 46398,
        "when": 46398,
        "is_public": true,
        "image": "rerum"
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
`POST /api/wedding/create`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    groom_id | integer |  required  | 
    bride_id | integer |  required  | 
    description | string |  optional  | 
    venue | string |  optional  | 
    reception | string |  optional  | 
    venue_lat | numeric |  optional  | Required if the parameters `venue_lng` are present.
    venue_lng | numeric |  optional  | Required if the parameters `venue_lat` are present.
    reception_lat | numeric |  optional  | Required if the parameters `reception_lng` are present.
    reception_lng | numeric |  optional  | Required if the parameters `reception_lat` are present.
    when | numeric |  optional  | 
    is_public | boolean |  optional  | 
    image | image |  optional  | Must be an image (jpeg, png, bmp, gif, or svg)

<!-- END_c1656cf4b0c0abf54a59393b6903898d -->

<!-- START_a980dbfae34220591a9b41d427ea08c8 -->
## Update wedding.

Note: Auth Required.

Updates this users wedding.

> Example request:

```bash
curl -X POST "http://localhost//api/wedding/update" \
-H "Accept: application/json" \
    -d "groom_id"="480" \
    -d "bride_id"="480" \
    -d "description"="modi" \
    -d "venue"="modi" \
    -d "reception"="modi" \
    -d "venue_lat"="480" \
    -d "venue_lng"="480" \
    -d "reception_lat"="480" \
    -d "reception_lng"="480" \
    -d "when"="480" \
    -d "is_public"="1" \
    -d "image"="modi" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/wedding/update",
    "method": "POST",
    "data": {
        "groom_id": 480,
        "bride_id": 480,
        "description": "modi",
        "venue": "modi",
        "reception": "modi",
        "venue_lat": 480,
        "venue_lng": 480,
        "reception_lat": 480,
        "reception_lng": 480,
        "when": 480,
        "is_public": true,
        "image": "modi"
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
`POST /api/wedding/update`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    groom_id | integer |  required  | 
    bride_id | integer |  required  | 
    description | string |  optional  | 
    venue | string |  optional  | 
    reception | string |  optional  | 
    venue_lat | numeric |  optional  | Required if the parameters `venue_lng` are present.
    venue_lng | numeric |  optional  | Required if the parameters `venue_lat` are present.
    reception_lat | numeric |  optional  | Required if the parameters `reception_lng` are present.
    reception_lng | numeric |  optional  | Required if the parameters `reception_lat` are present.
    when | numeric |  optional  | 
    is_public | boolean |  optional  | 
    image | image |  optional  | Must be an image (jpeg, png, bmp, gif, or svg)

<!-- END_a980dbfae34220591a9b41d427ea08c8 -->

<!-- START_b50b634738779e258b4b191f0a2ef21b -->
## Get this user&#039;s wedding.

Note: Auth Required.

Returns the authenticated user's wedding if found.

> Example request:

```bash
curl -X POST "http://localhost//api/wedding/get" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/wedding/get",
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
`POST /api/wedding/get`


<!-- END_b50b634738779e258b4b191f0a2ef21b -->

<!-- START_89972e9a15d708f3105bbc247f1eca02 -->
## Close user wedding.

Note: Auth Required.

Closes the authenticated user's wedding.

> Example request:

```bash
curl -X POST "http://localhost//api/wedding/close" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/wedding/close",
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
`POST /api/wedding/close`


<!-- END_89972e9a15d708f3105bbc247f1eca02 -->

