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
  "id" : "98540df05a854bddbc21199991e4ac60",
  "name" : "ecksessdee",
  "skins" : [ {
    "id" : "4732e446-365a-4fde-b1a2-d69b36a93115",
    "state" : "ACTIVE",
    "url" : "http://textures.minecraft.net/texture/ac4355918bd10032817f71066eb62acd452368aba32df9bff9968c0063656709",
    "variant" : "CLASSIC"
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
  "capes" : [ ]
}
```
