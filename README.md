Found by danktrain#0001 and Duff#8240 for the community and 3NAME Development and MCSniperPY

**NAME STATUS:**

Method:GET

URL: https://api.minecraftservices.com/minecraft/profile/name/asd/available

You only have to send the bearer token aswell as the typical headers

if taken/blocked:
```
{
  "status" : "DUPLICATE"
}
```

if available:
200 Ok
```
{
  "status" : "AVAILABLE"
}
```

if innappropriate:
```
{
  "status" : "NOT_ALLOWED"
}
```

**ACCOUNT NAMECHANGE ELIGIBILITY:**

Method:GET

URL: https://api.minecraftservices.com/minecraft/profile/namechange

You only have to send the bearer token aswell as the typical headers

Response Body when successful:
200 ok
```
{
  "changedAt" : "2020-07-17T16:01:26Z",
  "createdAt" : "2011-06-19T14:20:35Z",
  "nameChangeAllowed" : true
}
```

**ACCOUNT DATA:**

Method: GET

URL: https://api.minecraftservices.com/minecraft/profile

You only have to send the bearer token aswell as the typical headers

Response Body: 
200 OK

```
{
  "id" : uuid,
  "name" : currentname,
  "skins" : [ {
    "id" : skinid,
    "state" : skinstate,
    "url" : skinurl,
    "variant" : bodytype
  } ],
  "capes" : [ ]
}
```

**CHANGE NAME:**

Method: PUT
URL: https://api.minecraftservices.com/minecraft/profile/name/<name>

You only have to send the bearer token aswell as the typical headers

Response Body if the request is successful:
200 OK
```
{
  "id" : uuid,
  "name" : new name,
  "skins" : [ {
    "id" : skinid?,
    "state" : someshit,
    "url" : skinurl,
    "variant" : bodyshape
  } ],
  "capes" : [ ] //if someone with a cape account could do this and tell me it would be much appreciated
}
```

Response Body if name was changed before 30 days:
401 UNAUTHORIZED
```
{
    "path": "/minecraft/profile/name/<NAME>",
    "errorType": "UnauthorizedOperationException",
    "error": "UnauthorizedOperationException",
    "errorMessage": "Unauthorized",
    "developerMessage": "Unauthorized"
}
```

**CHANGE SKIN**

POST https://api.minecraftservices.com/minecraft/profile/skins/active

200 OK

bearer in headers

payload: skin file

resp body:
```
{
  "id" : uuid,
  "name" : new name,
  "skins" : [ {
    "id" : skinid?,
    "state" : someshit,
    "url" : skinurl,
    "variant" : bodyshape
  } ],
  "capes" : [ ] //if someone with a cape account could do this and tell me it would be much appreciated
}
```

**RESET SKIN**

DELETE https://api.minecraftservices.com/minecraft/profile/skins/active



You only have to send the bearer token aswell as the typical headers

resp body:
200 OK
```
{
  "id" : uuid,
  "name" : new name,
  "skins" : [ {
    "id" : skinid,
    "state" : skinstate,
    "url" : skinurl,
    "variant" : bodytype,
    "alias" : officialnameofskin
  } ],
  "capes" : [ ] //if someone with a cape account could do this and tell me it would be much appreciated
}
```
