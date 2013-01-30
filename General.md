# General

Basic application commands/information. No authentication required.

## Ping
Ping the API server to see if alive and well. 

```
GET /ping
```

### Response
```
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8
```
```
{
  "version": "0.0.1-9",
  "name": "ten"
}
```
