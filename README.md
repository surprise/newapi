**NAME STATUS**
GET https://api.minecraftservices.com/minecraft/profile/name/asd/available
bearer in headers
200 ok
if taken/blocked:
```
{
  "status" : "DUPLICATE"
}```
if available:
```
{
  "status" : "AVAILABLE"
}```
if innappropriate:
```
{
  "status" : "NOT_ALLOWED"
}```
