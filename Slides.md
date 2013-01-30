# Slides

Slides are individual images/videos to be displayed at a location. A single slide can be in a one to many relationship with Locations.

There are different slide types and priorities.

The different types include:
- image
  - Minimum Dimensions: 1920px by 1080px
  - Format: JPG, PNG
- video
  - Minimum Resolution: 720p
  - Minimum Bitrate: 2000 bps
  - Format: FLV, MP4
- text
  - 300 characters
- webpage
  - Responsive
  - Viewable area within resolution dimensions of 1920px by 1080px

## Get Slide
Retrieve information on a individual slide

```
GET /slides/:id
```

### Response
```
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8
```
```
{
  "_id": "50efe203eb86e1dcfb000001"
  "title": "Startup Weekend Event",
  "description": "Startup event for Engineers!",
  "remarks": "Recurring event every year",
  "type": "image",
  "url": "http://ten.jit.su/slides/50efe203eb86e1dcfb000001",
  "asset_data": "https://s3.amazonaws.com/tenproject/test/emerald-pantone-17-5641.jpg"
}
```

- `_id`: Hash identifier of slide
- `title`: Title of slide
- `description`: Description describle purpose of slide
- `remarks`: Remarks for moderator
- `type`:
  - `image`: Image should follow guidelines specified above
  - `video`:  Video should follow guidelines specified above
  - `text`: Plain text are
- `url`: Public URL location of slide or custom URL specified by owner of slide
- `asset_data": URL for type *image* or *video*. Plain text for type *text*
