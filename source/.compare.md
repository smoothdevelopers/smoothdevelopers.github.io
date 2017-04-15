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

#Authentication

This module will handle all the user authentication  including registration with
email or Facebook, login  email or Facebook and logout.

It is also responsible of assigning new API access tokens  the credentials of
the already authenticated user.
<!-- START_fde36329ab58ad5d6ab50b7704de548b -->
## User details.

This will return the currently logged in user's details.

> Example request:

```bash
curl -X GET "http://localhost//api/token" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/token",
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
`GET /api/token`

`HEAD /api/token`


<!-- END_fde36329ab58ad5d6ab50b7704de548b -->

<!-- START_39798dab89951f0e0c3fc59a53f859e5 -->
## Logout the user.

Will logout the logged in user and close the session.

> Example request:

```bash
curl -X POST "http://localhost//api/logout" \
-H "Accept: application/json" \
    -d "token"="distinctio" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/logout",
    "method": "POST",
    "data": {
        "token": "distinctio"
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
`POST /api/logout`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    token | string |  required  | 

<!-- END_39798dab89951f0e0c3fc59a53f859e5 -->

<!-- START_0f8ecc008bbceb798251c0de85808ef8 -->
## Register with email and password.

Will register the user with an email and password.

> Example request:

```bash
curl -X POST "http://localhost//api/register" \
-H "Accept: application/json" \
    -d "name"="voluptatem" \
    -d "email"="damore.nestor@example.org" \
    -d "password"="voluptatem" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/register",
    "method": "POST",
    "data": {
        "name": "voluptatem",
        "email": "damore.nestor@example.org",
        "password": "voluptatem"
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
`POST /api/register`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    name | string |  required  | Maximum: `255`
    email | email |  optional  | Maximum: `255`
    password | string |  required  | Minimum: `6`

<!-- END_0f8ecc008bbceb798251c0de85808ef8 -->

<!-- START_7a55f4d36791d87bfc8b6c280f210886 -->
## Register with Facebook

Will register a user using their Facebook ID.

> Example request:

```bash
curl -X POST "http://localhost//api/register_fb" \
-H "Accept: application/json" \
    -d "name"="vero" \
    -d "fb_id"="vero" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/register_fb",
    "method": "POST",
    "data": {
        "name": "vero",
        "fb_id": "vero"
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
`POST /api/register_fb`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    name | string |  required  | Maximum: `255`
    fb_id | string |  required  | 

<!-- END_7a55f4d36791d87bfc8b6c280f210886 -->

<!-- START_d5417ec5d425f04b71e9a4e9987c8295 -->
## Login with email and password.

Will login a user with their email and password.

> Example request:

```bash
curl -X POST "http://localhost//api/authenticate" \
-H "Accept: application/json" \
    -d "email"="rossie62@example.org" \
    -d "password"="cupiditate" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/authenticate",
    "method": "POST",
    "data": {
        "email": "rossie62@example.org",
        "password": "cupiditate"
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
`POST /api/authenticate`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    email | email |  required  | 
    password | string |  required  | 

<!-- END_d5417ec5d425f04b71e9a4e9987c8295 -->

<!-- START_20b8511ea671420c2e7a7220a7a5ecdc -->
## Login with Facebook ID.

Will login a user with their Facebook ID.

> Example request:

```bash
curl -X POST "http://localhost//api/authenticate_fb" \
-H "Accept: application/json" \
    -d "email"="runolfsson.ima@example.org" \
    -d "password"="et" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/authenticate_fb",
    "method": "POST",
    "data": {
        "email": "runolfsson.ima@example.org",
        "password": "et"
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
`POST /api/authenticate_fb`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    email | email |  required  | 
    password | string |  required  | 

<!-- END_20b8511ea671420c2e7a7220a7a5ecdc -->

<!-- START_a5d7bfde9c5e33e7c8fd6f07a11939b5 -->
## Get authenticated user

Returns the details of the currently logged in user.

> Example request:

```bash
curl -X GET "http://localhost//api/authenticated_user" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/authenticated_user",
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
`GET /api/authenticated_user`

`HEAD /api/authenticated_user`


<!-- END_a5d7bfde9c5e33e7c8fd6f07a11939b5 -->

