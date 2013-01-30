# Locations

Each location represents a single digital signage client instance.

## List Locations
List the locations the authentication user has access to.

```
GET /locations
```

### Response
```
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8
```
```json
[
  {
    "id": "eus/trottier",
    "name": "Trottier",
    "organization": "EUS",
    "access_mode": "organization",
    "status": "online"
  },
  {
    "id": "eus/mcconnell",
    "name": "McConnell",
    "organization": "EUS",
    "access_mode": "invite",
    "status": "warning"
  }
]
```

- `id`: Location resource ID
- `name`: Name of location
- `organization`: Name of organization the location belongs to
- `access_mode`: Access permissions for location
  - `organization`: Any user belonging to the location's organization has access to this flow
  - `invite`: This location can only be accessed via invite
- `status`: Current status of location
  - `online`: Client at location is connected and running without problem
  - `warning`: Client at location is connected but has encountered problem(s)
  - `offline`: Client at location is not connected to ten server


## Get Location
Get information for a specific location. Returned object includes slides for the location.

Slides will contain relevant information for displaying on client.

```
GET /locations/:organization/:location
```

### Response
```
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8
```
```json
{
  "id": "eus/trottier",
  "name": "Trottier",
  "organization": "EUS",
  "access_mode": "organization",
  "status": "online",
  "slides": [
    {
      "_id": ""
      "url": ""
    },
    {
      "_id": ""
      "url": ""
    },
    // ...
  ]
}
```


## Create a Location

```
POST /locations/:organization
```


## Update a Location

```
PUT /locations/:organization/:location
```