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

#Engagement

This module handles the creation, updating and deletion of
engagements.

Note: for an engagement to be created, we only require to have a couple and
      these two have to have created an account with us.
<!-- START_bcdb7863c3831e46bb710baf7dadb297 -->
## Get one public engagement by id.

Returns a public engagement given its id as a parameter.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/engagement/get_one" \
-H "Accept: application/json" \
    -d "engagement_id"="772121753" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/engagement/get_one",
    "method": "POST",
    "data": {
        "engagement_id": 772121753
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
`POST /api/engagement/get_one`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    engagement_id | integer |  required  | 

<!-- END_bcdb7863c3831e46bb710baf7dadb297 -->

<!-- START_a222e3482c977b9c139bfcd3208c1d8b -->
## Get public engagements by page.

Return all public engagements in pages with every page having 15 engagements.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/engagement/get_paged" \
-H "Accept: application/json" \
    -d "page"="519" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/engagement/get_paged",
    "method": "POST",
    "data": {
        "page": 519
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
`POST /api/engagement/get_paged`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    page | integer |  required  | 

<!-- END_a222e3482c977b9c139bfcd3208c1d8b -->

<!-- START_f1aabb6491c18132728616b8bb11355e -->
## Create engagement.

Note: Auth Required.

This will create an engagement between two app users and return the engagement
id on success. The user creating the engagement must either be the bride or
the groom in the engagement.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/engagement/create" \
-H "Accept: application/json" \
    -d "groom_id"="58" \
    -d "bride_id"="58" \
    -d "proposal_date"="58" \
    -d "culture"="58" \
    -d "proposal_lat"="58" \
    -d "proposal_lng"="58" \
    -d "image"="magnam" \
    -d "phrase"="magnam" \
    -d "type"="58" \
    -d "privacy"="58" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/engagement/create",
    "method": "POST",
    "data": {
        "groom_id": 58,
        "bride_id": 58,
        "proposal_date": 58,
        "culture": 58,
        "proposal_lat": 58,
        "proposal_lng": 58,
        "image": "magnam",
        "phrase": "magnam",
        "type": 58,
        "privacy": 58
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
`POST /api/engagement/create`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    groom_id | integer |  required  | 
    bride_id | integer |  required  | 
    proposal_date | numeric |  optional  | 
    culture | integer |  optional  | 
    proposal_lat | numeric |  optional  | Required if the parameters `proposal_lng` are present.
    proposal_lng | numeric |  optional  | Required if the parameters `proposal_lng` are present.
    image | image |  optional  | Must be an image (jpeg, png, bmp, gif, or svg)
    phrase | string |  optional  | 
    type | integer |  optional  | 
    privacy | integer |  optional  | 

<!-- END_f1aabb6491c18132728616b8bb11355e -->

<!-- START_6144b66ae57541e27c78677d69c9d4bc -->
## Update engagement.

Note: Auth Required.

Updates this users engagement.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/engagement/update" \
-H "Accept: application/json" \
    -d "groom_id"="6" \
    -d "bride_id"="6" \
    -d "proposal_date"="6" \
    -d "culture"="6" \
    -d "proposal_lat"="6" \
    -d "proposal_lng"="6" \
    -d "image"="perferendis" \
    -d "phrase"="perferendis" \
    -d "type"="6" \
    -d "privacy"="6" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/engagement/update",
    "method": "POST",
    "data": {
        "groom_id": 6,
        "bride_id": 6,
        "proposal_date": 6,
        "culture": 6,
        "proposal_lat": 6,
        "proposal_lng": 6,
        "image": "perferendis",
        "phrase": "perferendis",
        "type": 6,
        "privacy": 6
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
`POST /api/engagement/update`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    groom_id | integer |  required  | 
    bride_id | integer |  required  | 
    proposal_date | numeric |  optional  | 
    culture | integer |  optional  | 
    proposal_lat | numeric |  optional  | Required if the parameters `proposal_lng` are present.
    proposal_lng | numeric |  optional  | Required if the parameters `proposal_lng` are present.
    image | image |  optional  | Must be an image (jpeg, png, bmp, gif, or svg)
    phrase | string |  optional  | 
    type | integer |  optional  | 
    privacy | integer |  optional  | 

<!-- END_6144b66ae57541e27c78677d69c9d4bc -->

<!-- START_9dc7a9e7b43007917a52791a03478092 -->
## Get this user&#039;s engagement.

Note: Auth Required.

Returns the authenticated user's engagement if found.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/engagement/get" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/engagement/get",
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
`POST /api/engagement/get`


<!-- END_9dc7a9e7b43007917a52791a03478092 -->

<!-- START_50683e5d68ff9e630d6319761da83694 -->
## Close user&#039;s engagement.

Note: Auth Required.

Closes the authenticated user's engagement.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/engagement/close" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/engagement/close",
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
`POST /api/engagement/close`


<!-- END_50683e5d68ff9e630d6319761da83694 -->

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

On success:
{ 'error': false, 'error-code': success-code, 'error-description': ... }

On error: null.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/user/register" \
-H "Accept: application/json" \
    -d "name"="ab" \
    -d "email"="ward.faye@example.com" \
    -d "password_confirmation"="ab" \
    -d "password"="ab" \
    -d "gender"="male" \
    -d "profile_pic"="ab" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/user/register",
    "method": "POST",
    "data": {
        "name": "ab",
        "email": "ward.faye@example.com",
        "password_confirmation": "ab",
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
    email | email |  required  | Maximum: `255`
    password_confirmation | string |  required  | Minimum: `6`
    password | string |  required  | Minimum: `6`
    gender | string |  required  | `male` or `female`
    profile_pic | image |  optional  | Must be an image (jpeg, png, bmp, gif, or svg)

<!-- END_9b706bcb7d78cfacbf8e5e3e7d8afe2b -->

<!-- START_5aa3d01db2b9d4c6a5d0d1ee7c426bd8 -->
## Register with Facebook

Will register a user using their Facebook ID.

On success:
{ 'error': false, 'error-code': success-code, 'error-description': ... }

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/user/register_fb" \
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
    "url": "http://i-doapp.com//api/user/register_fb",
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

Will login a user with their email and password and return a token.

On success:
{ 'error': false, 'error-code': success-code, 'error-description': ..., 'token': ... }

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/user/login" \
-H "Accept: application/json" \
    -d "email"="joanne.muller@example.com" \
    -d "password"="ut" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/user/login",
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

Will login a user with their Facebook ID and return a token.

On success:
{ 'error': false, 'error-code': success-code, 'error-description': ..., 'token': ... }

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/user/login_fb" \
-H "Accept: application/json" \
    -d "fb_id"="sed" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/user/login_fb",
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

<!-- START_5b028048ded09ef8d7b75cbb829d70c3 -->
## Search users by name or email.

This will search and return a list of users in pages.

On success:
{ 'error': false, 'error-code': success-code, 'error-description': ..., 'users': # users # }

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/user/search_paged" \
-H "Accept: application/json" \
    -d "page"="94608" \
    -d "search_term"="dolorum" \
    -d "gender"="female" \
    -d "search_by"="email" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/user/search_paged",
    "method": "POST",
    "data": {
        "page": 94608,
        "search_term": "dolorum",
        "gender": "female",
        "search_by": "email"
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
`POST /api/user/search_paged`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    page | integer |  required  | 
    search_term | string |  required  | 
    gender | string |  required  | `male`, `female` or `both`
    search_by | string |  required  | `name`, `email` or `both`

<!-- END_5b028048ded09ef8d7b75cbb829d70c3 -->

<!-- START_1cff6a9e89def167de9d09a13dd2555d -->
## Refresh token

Note: Auth Required

This will refresh current logged in users token and return the new token

On success:
{ 'error': false, 'error-code': success-code, 'error-description': ... }

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/user/refresh_token" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/user/refresh_token",
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
`POST /api/user/refresh_token`


<!-- END_1cff6a9e89def167de9d09a13dd2555d -->

<!-- START_9c9260bd1ad91eb9aa21477f56d5ad8b -->
## User details.

Note: Auth Required

Returns all the details of the currently logged in user.

On success:
{ 'error': false, 'error-code': success-code, 'error-description': ..., 'user': { # user data # } }

> Example request:

```bash
curl -X GET "http://i-doapp.com//api/user/get" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/user/get",
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

<!-- START_99dabfc22a317a2385dee642272a537e -->
## Update user details.

Note: Auth Required.

This will update the details of an already logged in user.

On success:
{ 'error': false, 'error-code': success-code, 'error-description': ... }

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/user/update" \
-H "Accept: application/json" \
    -d "name"="culpa" \
    -d "gender"="female" \
    -d "profile_pic"="culpa" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/user/update",
    "method": "POST",
    "data": {
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
    name | string |  required  | Maximum: `255`
    gender | string |  required  | `male` or `female`
    profile_pic | image |  optional  | Must be an image (jpeg, png, bmp, gif, or svg)

<!-- END_99dabfc22a317a2385dee642272a537e -->

<!-- START_a93d6745597660d48aea8c2249b67600 -->
## Update user password

Note: Auth Required.

This will update the password of an already logged in user. This user
must have been registered using an email and password.

On success:
{ 'error': false, 'error-code': success-code, 'error-description': ... }

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/user/update_password" \
-H "Accept: application/json" \
    -d "old_password"="dicta" \
    -d "password_confirmation"="dicta" \
    -d "password"="dicta" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/user/update_password",
    "method": "POST",
    "data": {
        "old_password": "dicta",
        "password_confirmation": "dicta",
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
    old_password | string |  required  | Minimum: `6`
    password_confirmation | string |  required  | Minimum: `6`
    password | string |  required  | Minimum: `6`

<!-- END_a93d6745597660d48aea8c2249b67600 -->

<!-- START_8e2bcf97ca2b0da97a00d74ce5c0dddc -->
## Logout the user.

Note: Auth Required.

Will logout the logged in user and close the session.
The token is required.

On success:
{ 'error': false, 'error-code': success-code, 'error-description': ... }

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/user/logout" \
-H "Accept: application/json" \
    -d "token"="quia" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/user/logout",
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

On success:
{ 'error': false, 'error-code': success-code, 'error-description': ... }

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/user/close_account" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/user/close_account",
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
<!-- START_8994c494dcee876111b0a139e4365c99 -->
## Get one public wedding by id.

Returns a public wedding given its id as a parameter.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/wedding/get_one" \
-H "Accept: application/json" \
    -d "wedding_id"="630827" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/wedding/get_one",
    "method": "POST",
    "data": {
        "wedding_id": 630827
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
`POST /api/wedding/get_one`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    wedding_id | integer |  required  | 

<!-- END_8994c494dcee876111b0a139e4365c99 -->

<!-- START_9e56c96e75d01fc6354a8dfaf228a5e0 -->
## Get public weddings by page.

Return all public weddings in pages with every page having 15 weddings.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/wedding/get_paged" \
-H "Accept: application/json" \
    -d "page"="51782023" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/wedding/get_paged",
    "method": "POST",
    "data": {
        "page": 51782023
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
`POST /api/wedding/get_paged`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    page | integer |  required  | 

<!-- END_9e56c96e75d01fc6354a8dfaf228a5e0 -->

<!-- START_c1656cf4b0c0abf54a59393b6903898d -->
## Create wedding.

Note: Auth Required.

This will create a wedding between two app users and return the wedding
id on success. The user creating the wedding must either be the bride or
the groom in the wedding.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/wedding/create" \
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
    -d "privacy"="46398" \
    -d "image"="rerum" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/wedding/create",
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
        "privacy": 46398,
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
    privacy | numeric |  optional  | 
    image | image |  optional  | Must be an image (jpeg, png, bmp, gif, or svg)

<!-- END_c1656cf4b0c0abf54a59393b6903898d -->

<!-- START_a980dbfae34220591a9b41d427ea08c8 -->
## Update wedding.

Note: Auth Required.

Updates this users wedding.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/wedding/update" \
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
    -d "privacy"="480" \
    -d "image"="modi" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/wedding/update",
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
        "privacy": 480,
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
    privacy | integer |  optional  | 
    image | image |  optional  | Must be an image (jpeg, png, bmp, gif, or svg)

<!-- END_a980dbfae34220591a9b41d427ea08c8 -->

<!-- START_b50b634738779e258b4b191f0a2ef21b -->
## Get this user&#039;s wedding.

Note: Auth Required.

Returns the authenticated user's wedding if found.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/wedding/get" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/wedding/get",
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
curl -X POST "http://i-doapp.com//api/wedding/close" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/wedding/close",
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

