# Slides

Slides are individual images/videos to be displayed at a location. A single slide can be in a one to many relationship with Locations.

There are different slide types and priorities.


#### Slide types and respective submission guidelines:
- image
  - Minimum Dimensions: 1920px by 1080px
  - Format: JPG, PNG
- video
  - Minimum Resolution: 720p
  - Format: FLV, MP4
- text
  - 300 characters
- webpage
  - Responsive
  - Viewable area within resolution dimensions of 1920px by 1080px

#### Status of slides:
- `submitted` We have recieved your submission and will be reviewing it
- `rejected` Submission did not meet requirements. Please read slide comments
- `online` Slide is being displayed at designated locations
- `offline` Slide is not displayed on any monitors
- `expired` Slide approved online duration has expired
- `draft` Saved slides which have not yet been submitted for approval

## Get Slide
Retrieve information on a individual slide

```
GET /slides/:organization
```

### Response
```
HTTP/1.1 200 OK
Content-Type: application/json; charset=utf-8
```
```json
{
  "_id": "50efe203eb86e1dcfb000001",
  "location": "eus/trottier",
  "title": "Startup Weekend Event",
  "description": "Startup event for Engineers!",
  "remarks": "Recurring event every year",
  "type": "image",
  "url": "http://ten.jit.su/slides/50efe203eb86e1dcfb000001",
  "asset_data": "https://s3.amazonaws.com/tenproject/test/emerald-pantone-17-5641.jpg",
  "status": "draft"
}
```

- `_id`: Hash identifier of slide
- `location`: Location(s) which slide belongs to
- `title`: Title of slide
- `description`: Description describle purpose of slide
- `remarks`: Remarks for moderator
- `type`:
  - `image`: Image should follow guidelines specified above
  - `video`:  Video should follow guidelines specified above
  - `text`: Plain text should follow guidelines specified above
  - `webpage`: Page should follow guidelines specified above
- `url`: Public URL location of slide or custom URL specified by owner of slide
- `asset_data`: URL for type *image* or *video*. Plain text for type *text*
- `status`: Status of slide



## Create a Slide

```
POST /slides/:organization/slides
```


## Delete Slide

```
DELETE /slides/:organization/slides/:id
```