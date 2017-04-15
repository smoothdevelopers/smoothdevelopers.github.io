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
## /api/token

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
## This will logout the user.

> Example request:

```bash
curl -X POST "http://localhost//api/logout" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/logout",
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
`POST /api/logout`


<!-- END_39798dab89951f0e0c3fc59a53f859e5 -->

<!-- START_0f8ecc008bbceb798251c0de85808ef8 -->
## This will register a new user with an email and password.

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

<!-- START_d5417ec5d425f04b71e9a4e9987c8295 -->
## Will authenticate the user given the email and password
and will return the new user token.

> Example request:

```bash
curl -X POST "http://localhost//api/authenticate" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://localhost//api/authenticate",
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
`POST /api/authenticate`


<!-- END_d5417ec5d425f04b71e9a4e9987c8295 -->

<!-- START_a5d7bfde9c5e33e7c8fd6f07a11939b5 -->
## /api/authenticated_user

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

