Found by danktrain#0001 for the community and 3NAME Development

**NAME STATUS**

GET https://api.minecraftservices.com/minecraft/profile/name/asd/available

bearer in headers

200 ok

if taken/blocked:
```
{
  "status" : "DUPLICATE"
}
```

if available:
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

**ACCOUNT NAMECHANGE ELIGIBILITY**

GET https://api.minecraftservices.com/minecraft/profile/namechange

bearer in headers

200 ok
```
{
  "changedAt" : "2020-07-17T16:01:26Z",
  "createdAt" : "2011-06-19T14:20:35Z",
  "nameChangeAllowed" : true
}
```

**ACCOUNT DATA**

GET https://api.minecraftservices.com/minecraft/profile

bearer of my alt "ecksessdee" in headers

resp: 200 ok

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

**CHANGE NAME**

PUT https://api.minecraftservices.com/minecraft/profile/name/wantedname

200 OK

bearer in headers

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

200 OK

bearer in headers

resp body:
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
