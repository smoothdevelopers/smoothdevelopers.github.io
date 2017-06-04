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

<!-- START_60cca79164b0762b36e6aea9f22597a2 -->
## Create a comment

Note: Auth Required.

Creates a comment on an engagement. The engagement has to be a public
engagement or the user has to be an invited user for them to be
able to comment on the engagement.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/engagement/comment/create" \
-H "Accept: application/json" \
    -d "engagement_id"="4550437" \
    -d "comment"="vero" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/engagement/comment/create",
    "method": "POST",
    "data": {
        "engagement_id": 4550437,
        "comment": "vero"
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
`POST /api/engagement/comment/create`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    engagement_id | integer |  required  | 
    comment | string |  required  | 

<!-- END_60cca79164b0762b36e6aea9f22597a2 -->

<!-- START_ee5128ae9623aaa63f4da31646328aa7 -->
## Update a comment

Note: Auth Required.

Updates a comment that was previously made by the authenticated user

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/engagement/comment/update" \
-H "Accept: application/json" \
    -d "comment_id"="3057061" \
    -d "comment"="facere" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/engagement/comment/update",
    "method": "POST",
    "data": {
        "comment_id": 3057061,
        "comment": "facere"
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
`POST /api/engagement/comment/update`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    comment_id | integer |  required  | 
    comment | string |  required  | 

<!-- END_ee5128ae9623aaa63f4da31646328aa7 -->

<!-- START_5d28f2487050be102e78e1f158702544 -->
## Get comments.

Note: Auth Required.

Returns comments for an engagement if the user is authorized to
view them or the engagement is a public one.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/engagement/comment/get_paged" \
-H "Accept: application/json" \
    -d "engagement_id"="2" \
    -d "page"="2" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/engagement/comment/get_paged",
    "method": "POST",
    "data": {
        "engagement_id": 2,
        "page": 2
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
`POST /api/engagement/comment/get_paged`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    engagement_id | integer |  required  | 
    page | integer |  required  | 

<!-- END_5d28f2487050be102e78e1f158702544 -->

<!-- START_96e2207feb246a08621888672700bf8b -->
## Delete a comment

Note: Auth Required.

Deletes a comment created by the user.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/engagement/comment/delete" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/engagement/comment/delete",
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
`POST /api/engagement/comment/delete`


<!-- END_96e2207feb246a08621888672700bf8b -->

<!-- START_8a60c9a600bd310476f401f2027881b0 -->
## Create a like

Note: Auth Required.

Creates a like for this engagement by the authenticated user

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/engagement/like/create" \
-H "Accept: application/json" \
    -d "engagement_id"="1" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/engagement/like/create",
    "method": "POST",
    "data": {
        "engagement_id": 1
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
`POST /api/engagement/like/create`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    engagement_id | integer |  required  | 

<!-- END_8a60c9a600bd310476f401f2027881b0 -->

<!-- START_5b7db36b764c12fa886e3bd875d60470 -->
## Remove a like

Note: Auth Required.

Removes a like on an engagement by the authenticated user.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/engagement/like/delete" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/engagement/like/delete",
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
`POST /api/engagement/like/delete`


<!-- END_5b7db36b764c12fa886e3bd875d60470 -->

<!-- START_4105f8b986cf597245ee52f8e6fdf101 -->
## Save Photo

Note: Auth Required.

Saves engagement photo for the given engagement by the given user. The
user saving the photo must either be the owner of engagement (in which
case the photo is saved authorized) or another user with the permission
to access this engagement's data (when it is public or when the user
is an invited user)

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/engagement/photo/save" \
-H "Accept: application/json" \
    -d "image"="ea" \
    -d "user_id"="4873" \
    -d "engagement_id"="4873" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/engagement/photo/save",
    "method": "POST",
    "data": {
        "image": "ea",
        "user_id": 4873,
        "engagement_id": 4873
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
`POST /api/engagement/photo/save`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    image | image |  required  | Must be an image (jpeg, png, bmp, gif, or svg)
    user_id | integer |  required  | 
    engagement_id | integer |  required  | 

<!-- END_4105f8b986cf597245ee52f8e6fdf101 -->

<!-- START_79eaffd5710a53db5e5245f25d06d215 -->
## Authorize a photo.

Note: Auth Required.

Authorize a specific photo that has been posted. The authenticated user
must be one of the couples in the engagement.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/engagement/photo/authorize" \
-H "Accept: application/json" \
    -d "photo_id"="98" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/engagement/photo/authorize",
    "method": "POST",
    "data": {
        "photo_id": 98
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
`POST /api/engagement/photo/authorize`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    photo_id | integer |  required  | 

<!-- END_79eaffd5710a53db5e5245f25d06d215 -->

<!-- START_b89840a0af8e245d6d83ebd63a2c8d9c -->
## Get authorized images paged.

Note: Auth Required.

Returns a list of authorized images of this engagement if the engagement
is public or if the user has permission (user_id holds the user of the user
accessing the images)

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/engagement/photo/authorized" \
-H "Accept: application/json" \
    -d "engagement_id"="3" \
    -d "user_id"="3" \
    -d "page"="3" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/engagement/photo/authorized",
    "method": "POST",
    "data": {
        "engagement_id": 3,
        "user_id": 3,
        "page": 3
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
`POST /api/engagement/photo/authorized`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    engagement_id | integer |  required  | 
    user_id | integer |  required  | 
    page | integer |  required  | 

<!-- END_b89840a0af8e245d6d83ebd63a2c8d9c -->

<!-- START_523ee91fa1727fd66d3a44493b32970a -->
## Get unauthorized photos paged.

Note: Auth Required.

Returns a list in pages of images that have not yet been
authorized by the couple, but have been posted already. The user
accessing them must be one of the couples

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/engagement/photo/unauthorized" \
-H "Accept: application/json" \
    -d "engagement_id"="1" \
    -d "user_id"="1" \
    -d "page"="1" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/engagement/photo/unauthorized",
    "method": "POST",
    "data": {
        "engagement_id": 1,
        "user_id": 1,
        "page": 1
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
`POST /api/engagement/photo/unauthorized`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    engagement_id | integer |  required  | 
    user_id | integer |  required  | 
    page | integer |  required  | 

<!-- END_523ee91fa1727fd66d3a44493b32970a -->

<!-- START_39b2d61e91b23ce1b5f8648b5699d339 -->
## Delete a photo

Note: Auth Required.

Deletes an photo that has already been posted. The user deleting it
is either the person who posted it or the couples.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/engagement/photo/delete" \
-H "Accept: application/json" \
    -d "photo_id"="97" \
    -d "user_id"="97" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/engagement/photo/delete",
    "method": "POST",
    "data": {
        "photo_id": 97,
        "user_id": 97
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
`POST /api/engagement/photo/delete`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    photo_id | integer |  required  | 
    user_id | integer |  required  | 

<!-- END_39b2d61e91b23ce1b5f8648b5699d339 -->

#Inspiration

This module handles the creation, updating and deletion of
inspiration media.

Note: an inspiration is created either by the admin or a
user with a wedding or engagement.
<!-- START_122c09397a11c53fd9af5ade76789fba -->
## Get one inspiration by id.

Returns an inspiration by given the id.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/inspiration/get_one" \
-H "Accept: application/json" \
    -d "inspiration_id"="42" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/inspiration/get_one",
    "method": "POST",
    "data": {
        "inspiration_id": 42
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
`POST /api/inspiration/get_one`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    inspiration_id | integer |  required  | 

<!-- END_122c09397a11c53fd9af5ade76789fba -->

<!-- START_c3397f6ee9ec3d7214414e59ec51e1a2 -->
## Get inspirations paginated.

Returns a list of inspirations paginated.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/inspiration/get_paged" \
-H "Accept: application/json" \
    -d "page"="731" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/inspiration/get_paged",
    "method": "POST",
    "data": {
        "page": 731
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
`POST /api/inspiration/get_paged`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    page | integer |  required  | 

<!-- END_c3397f6ee9ec3d7214414e59ec51e1a2 -->

<!-- START_6d556b51a026c07a3b287f7f512947a4 -->
## Create inspiration.

Note: Auth Required.

This will create an inspiration. The user must have a wedding or an
an engagement.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/inspiration/create" \
-H "Accept: application/json" \
    -d "file"="perspiciatis" \
    -d "description"="perspiciatis" \
    -d "media_type"="image" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/inspiration/create",
    "method": "POST",
    "data": {
        "file": "perspiciatis",
        "description": "perspiciatis",
        "media_type": "image"
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
`POST /api/inspiration/create`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    file | file |  required  | Must be a file upload
    description | string |  required  | 
    media_type | string |  required  | `video`, `image` or `audio`

<!-- END_6d556b51a026c07a3b287f7f512947a4 -->

<!-- START_324c9412c5c33c6f58204f981d99bc09 -->
## Update inspiration.

Note: Auth Required.

The user updating the inspiration must be the user that created it.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/inspiration/update" \
-H "Accept: application/json" \
    -d "description"="nobis" \
    -d "inspiration_id"="9879367" \
    -d "file"="nobis" \
    -d "media_type"="nobis" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/inspiration/update",
    "method": "POST",
    "data": {
        "description": "nobis",
        "inspiration_id": 9879367,
        "file": "nobis",
        "media_type": "nobis"
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
`POST /api/inspiration/update`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    description | string |  required  | 
    inspiration_id | integer |  required  | 
    file | file |  optional  | Must be a file upload
    media_type | string |  optional  | Required if the parameters `file` are present.

<!-- END_324c9412c5c33c6f58204f981d99bc09 -->

<!-- START_8323a8d624221d7afb3e7c32f0a9a485 -->
## Deletes inspiration.

Note: Auth Required.

Deletes an inspiration. The user deleting it must have created it.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/inspiration/delete" \
-H "Accept: application/json" \
    -d "inspiration_id"="1818" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/inspiration/delete",
    "method": "POST",
    "data": {
        "inspiration_id": 1818
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
`POST /api/inspiration/delete`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    inspiration_id | integer |  required  | 

<!-- END_8323a8d624221d7afb3e7c32f0a9a485 -->

<!-- START_bf805309722956e6410a24a48210c738 -->
## Create inspiration comment.

Note: Auth Required.

Creates a comment by a user on an inspiration.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/inspiration/comment/create" \
-H "Accept: application/json" \
    -d "comment"="corporis" \
    -d "inspiration_id"="291" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/inspiration/comment/create",
    "method": "POST",
    "data": {
        "comment": "corporis",
        "inspiration_id": 291
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
`POST /api/inspiration/comment/create`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    comment | string |  required  | 
    inspiration_id | integer |  required  | 

<!-- END_bf805309722956e6410a24a48210c738 -->

<!-- START_5fff72c993147fbbeb6c4a6720088096 -->
## Update inspiration comment.

Note: Auth Required.

Updates a comment made by user on inspiration. The user updating it
must be the one who made the comment.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/inspiration/comment/update" \
-H "Accept: application/json" \
    -d "comment_id"="1" \
    -d "comment"="inventore" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/inspiration/comment/update",
    "method": "POST",
    "data": {
        "comment_id": 1,
        "comment": "inventore"
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
`POST /api/inspiration/comment/update`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    comment_id | integer |  required  | 
    comment | string |  required  | 

<!-- END_5fff72c993147fbbeb6c4a6720088096 -->

<!-- START_9a5e3de803b1d246fe8a86f3721c1e89 -->
## Delete inspiration comment

Note: Auth Required.

Deletes a comment on an inspiration. The user deleting must be
the one who made the comment.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/inspiration/comment/delete" \
-H "Accept: application/json" \
    -d "comment_id"="579277" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/inspiration/comment/delete",
    "method": "POST",
    "data": {
        "comment_id": 579277
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
`POST /api/inspiration/comment/delete`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    comment_id | integer |  required  | 

<!-- END_9a5e3de803b1d246fe8a86f3721c1e89 -->

<!-- START_995772862dda647294e8f360b3feb77f -->
## Creates a like on an inspiration.

Note: Auth Required.

Creates a like on an inspiration by a user.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/inspiration/like/create" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/inspiration/like/create",
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
`POST /api/inspiration/like/create`


<!-- END_995772862dda647294e8f360b3feb77f -->

<!-- START_75e8264dad31ef42aabd392cb4cdbe22 -->
## Delete inspiration like

Note: Auth Required.

Removes a like on an inspiration by the authenticated user. The user removing
it must be the one who created it.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/inspiration/like/delete" \
-H "Accept: application/json" \
    -d "like_id"="95" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/inspiration/like/delete",
    "method": "POST",
    "data": {
        "like_id": 95
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
`POST /api/inspiration/like/delete`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    like_id | integer |  required  | 

<!-- END_75e8264dad31ef42aabd392cb4cdbe22 -->

#Invitation

This module will handle creation, deletion and securing of invitations
to users by the wedding couple.

Note: for an inviation to be created, the user has to have a wedding.
<!-- START_0c2551e1a8d7bfb7f5ac33ab0e613ff8 -->
## Create invitation.

Note: Auth Required.

This will create an invitation to another user for a given wedding.
The user creating the invitation must own the wedding for which the invitation
is created.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/invitation/create" \
-H "Accept: application/json" \
    -d "wedding_id"="115831629" \
    -d "slots"="115831629" \
    -d "message"="ut" \
    -d "type"="link" \
    -d "invitee_id"="ut" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/invitation/create",
    "method": "POST",
    "data": {
        "wedding_id": 115831629,
        "slots": 115831629,
        "message": "ut",
        "type": "link",
        "invitee_id": "ut"
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
`POST /api/invitation/create`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    wedding_id | integer |  required  | 
    slots | integer |  required  | 
    message | string |  optional  | 
    type | string |  required  | `app` or `link`
    invitee_id | string |  optional  | Required if 

<!-- END_0c2551e1a8d7bfb7f5ac33ab0e613ff8 -->

<!-- START_369ca599f3b0bb84237b996f6af6a86c -->
## Cancel invitation.

Note: Auth Required.

This will cancel an invitation that has already been created by the
wedding couple for a particular user. The user cancelling must own the
wedding.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/invitation/delete" \
-H "Accept: application/json" \
    -d "invitation_id"="792585501" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/invitation/delete",
    "method": "POST",
    "data": {
        "invitation_id": 792585501
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
`POST /api/invitation/delete`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    invitation_id | integer |  required  | 

<!-- END_369ca599f3b0bb84237b996f6af6a86c -->

<!-- START_257fb0fb5fd8512c6c62fe796cb718e2 -->
## Secure invitation.

Note: Auth Required.

This will secure an invitation for a wedding for an invited user. This marks
the invitation as accepted.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/invitation/secure" \
-H "Accept: application/json" \
    -d "token"="60954" \
    -d "secured_slots"="1010721972" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/invitation/secure",
    "method": "POST",
    "data": {
        "token": 60954,
        "secured_slots": 1010721972
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
`POST /api/invitation/secure`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    token | integer |  required  | 
    secured_slots | integer |  required  | Minimum: `1`

<!-- END_257fb0fb5fd8512c6c62fe796cb718e2 -->

<!-- START_77cdc7f3884d2bbfcb8d2693e37d5fe6 -->
## Get user invitations.

Note: Auth Required.

Retrieves all the invitations for a particular user.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/invitation/user_invitations" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/invitation/user_invitations",
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
`POST /api/invitation/user_invitations`


<!-- END_77cdc7f3884d2bbfcb8d2693e37d5fe6 -->

<!-- START_3d0e8dac772451b7e7130348651981b4 -->
## Get wedding invitations.

Note: Auth Required.

Retrieves all the invitations for a particular wedding. The user accesses
invitations of his/her wedding.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/invitation/wedding_invitations" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/invitation/wedding_invitations",
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
`POST /api/invitation/wedding_invitations`


<!-- END_3d0e8dac772451b7e7130348651981b4 -->

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

#Vendors

This module handles access to vendor details.
<!-- START_3192b85742c56adcd29f1b95bf579e72 -->
## Get one vendor.

Returns one vendor details, given their id.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/vendor/get_one" \
-H "Accept: application/json" \
    -d "vendor_id"="7097" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/vendor/get_one",
    "method": "POST",
    "data": {
        "vendor_id": 7097
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
`POST /api/vendor/get_one`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    vendor_id | integer |  required  | 

<!-- END_3192b85742c56adcd29f1b95bf579e72 -->

<!-- START_9a1a4da40c9b365d3faf4125528329b4 -->
## Get vendors under category.

This returns a list of vendors paginated for a given category.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/vendor/get_paged" \
-H "Accept: application/json" \
    -d "category_id"="24839150" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/vendor/get_paged",
    "method": "POST",
    "data": {
        "category_id": 24839150
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
`POST /api/vendor/get_paged`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    category_id | integer |  required  | 

<!-- END_9a1a4da40c9b365d3faf4125528329b4 -->

<!-- START_0ed1f72a32cbccb32c3151e8d3082b8f -->
## Get one vendor category

Returns one vendor category details.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/vendor_category/get_one" \
-H "Accept: application/json" \
    -d "category_id"="167" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/vendor_category/get_one",
    "method": "POST",
    "data": {
        "category_id": 167
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
`POST /api/vendor_category/get_one`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    category_id | integer |  required  | 

<!-- END_0ed1f72a32cbccb32c3151e8d3082b8f -->

<!-- START_18da6937b834c3cb08ae25dfcb07dcc8 -->
## Get vendor categories.

This returns the list of all vendors currently available.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/vendor_category/get_paged" \
-H "Accept: application/json" \
    -d "page"="5499885" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/vendor_category/get_paged",
    "method": "POST",
    "data": {
        "page": 5499885
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
`POST /api/vendor_category/get_paged`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    page | integer |  required  | 

<!-- END_18da6937b834c3cb08ae25dfcb07dcc8 -->

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

<!-- START_5bc8e2203528c526aa0e7c9b58d016c9 -->
## Create a comment

Note: Auth Required.

Creates a comment on a wedding. The wedding has to be a public
wedding or the user has to be an invited user for them to be
able to comment on the wedding.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/wedding/comment/create" \
-H "Accept: application/json" \
    -d "wedding_id"="11" \
    -d "comment"="voluptatem" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/wedding/comment/create",
    "method": "POST",
    "data": {
        "wedding_id": 11,
        "comment": "voluptatem"
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
`POST /api/wedding/comment/create`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    wedding_id | integer |  required  | 
    comment | string |  required  | 

<!-- END_5bc8e2203528c526aa0e7c9b58d016c9 -->

<!-- START_bee29ea6dfb1ef2584e4d80e91e749e4 -->
## Update a comment

Note: Auth Required.

Updates a comment that was previously made by the user

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/wedding/comment/update" \
-H "Accept: application/json" \
    -d "wedding_id"="111972470" \
    -d "page"="111972470" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/wedding/comment/update",
    "method": "POST",
    "data": {
        "wedding_id": 111972470,
        "page": 111972470
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
`POST /api/wedding/comment/update`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    wedding_id | integer |  required  | 
    page | integer |  required  | 

<!-- END_bee29ea6dfb1ef2584e4d80e91e749e4 -->

<!-- START_7b46dde2996767d3954e8e4c1c035692 -->
## Get comments.

Note: Auth Required.

Returns comments for a wedding if the user is authorized to
view them or the wedding is a public one.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/wedding/comment/get_paged" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/wedding/comment/get_paged",
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
`POST /api/wedding/comment/get_paged`


<!-- END_7b46dde2996767d3954e8e4c1c035692 -->

<!-- START_e23c9b719b0eef2aaf633f32111db007 -->
## Delete a comment

Note: Auth Required.

Deletes a comment created by the user.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/wedding/comment/delete" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/wedding/comment/delete",
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
`POST /api/wedding/comment/delete`


<!-- END_e23c9b719b0eef2aaf633f32111db007 -->

<!-- START_08de9c2b452a38104481e63d246eef13 -->
## Create a like

Note: Auth Required.

Creates a like for this wedding by the authenticated user

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/wedding/like/create" \
-H "Accept: application/json" \
    -d "wedding_id"="901" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/wedding/like/create",
    "method": "POST",
    "data": {
        "wedding_id": 901
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
`POST /api/wedding/like/create`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    wedding_id | integer |  required  | 

<!-- END_08de9c2b452a38104481e63d246eef13 -->

<!-- START_d820c2d86c043b56bd3de43318db84e8 -->
## Remove a like

Note: Auth Required.

Removes a like on an wedding by the authentcated user.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/wedding/like/delete" \
-H "Accept: application/json"
```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/wedding/like/delete",
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
`POST /api/wedding/like/delete`


<!-- END_d820c2d86c043b56bd3de43318db84e8 -->

<!-- START_8baef9a104db56caf46dd15cd9ecf470 -->
## Save Photo

Note: Auth Required.

Saves wedding photo for the given wedding by the given user. The
user saving the photo must either be the owner of wedding (in which
case the photo is saved authorized) or another user with the permission
to access this wedding's data (when it is public or when the user
is an invited user)

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/wedding/photo/save" \
-H "Accept: application/json" \
    -d "image"="rerum" \
    -d "user_id"="823006276" \
    -d "wedding_id"="823006276" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/wedding/photo/save",
    "method": "POST",
    "data": {
        "image": "rerum",
        "user_id": 823006276,
        "wedding_id": 823006276
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
`POST /api/wedding/photo/save`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    image | image |  required  | Must be an image (jpeg, png, bmp, gif, or svg)
    user_id | integer |  required  | 
    wedding_id | integer |  required  | 

<!-- END_8baef9a104db56caf46dd15cd9ecf470 -->

<!-- START_39b1c4a212a127f34d9e3548445e8a35 -->
## Authorize a photo.

Note: Auth Required.

Authorize a specific photo that has been posted. The authenticated user
must be one of the couples in the wedding.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/wedding/photo/authorize" \
-H "Accept: application/json" \
    -d "photo_id"="74099" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/wedding/photo/authorize",
    "method": "POST",
    "data": {
        "photo_id": 74099
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
`POST /api/wedding/photo/authorize`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    photo_id | integer |  required  | 

<!-- END_39b1c4a212a127f34d9e3548445e8a35 -->

<!-- START_b9f5ed09ae361f862dd7a1d486cba9bd -->
## Get authorized images paged.

Note: Auth Required.

Returns a list of authorized images of this wedding if the wedding
is public or if the user has permission.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/wedding/photo/authorized" \
-H "Accept: application/json" \
    -d "wedding_id"="422" \
    -d "user_id"="422" \
    -d "page"="422" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/wedding/photo/authorized",
    "method": "POST",
    "data": {
        "wedding_id": 422,
        "user_id": 422,
        "page": 422
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
`POST /api/wedding/photo/authorized`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    wedding_id | integer |  required  | 
    user_id | integer |  required  | 
    page | integer |  required  | 

<!-- END_b9f5ed09ae361f862dd7a1d486cba9bd -->

<!-- START_de94711a7845d1766bc9630ca4f6919c -->
## Get unauthorized photos paged.

Note: Auth Required.

Returns a list in pages of images that have not yet been
authorized by the couple, but have been posted already. The user
accessing them must be one of the couples

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/wedding/photo/unauthorized" \
-H "Accept: application/json" \
    -d "wedding_id"="8586956" \
    -d "user_id"="8586956" \
    -d "page"="8586956" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/wedding/photo/unauthorized",
    "method": "POST",
    "data": {
        "wedding_id": 8586956,
        "user_id": 8586956,
        "page": 8586956
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
`POST /api/wedding/photo/unauthorized`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    wedding_id | integer |  required  | 
    user_id | integer |  required  | 
    page | integer |  required  | 

<!-- END_de94711a7845d1766bc9630ca4f6919c -->

<!-- START_6e96668992cb30387a4a52e7b5f0842e -->
## Delete a photo

Note: Auth Required.

Deletes an photo that has already been posted. The user deleting it
is either the person who posted it or the couples.

> Example request:

```bash
curl -X POST "http://i-doapp.com//api/wedding/photo/delete" \
-H "Accept: application/json" \
    -d "photo_id"="92026811" \
    -d "user_id"="92026811" \

```

```javascript
var settings = {
    "async": true,
    "crossDomain": true,
    "url": "http://i-doapp.com//api/wedding/photo/delete",
    "method": "POST",
    "data": {
        "photo_id": 92026811,
        "user_id": 92026811
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
`POST /api/wedding/photo/delete`

#### Parameters

Parameter | Type | Status | Description
--------- | ------- | ------- | ------- | -----------
    photo_id | integer |  required  | 
    user_id | integer |  required  | 

<!-- END_6e96668992cb30387a4a52e7b5f0842e -->

