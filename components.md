## Task Processing Components

Task Processing Components are the building blocks to allow you to get information back from users when they process your tasks.

### Media

Example:
```javascript
{
  "component_type": "media",
  "label": "Text label to display",
  "name": "internal_name",
  "required": "yes",
  "extra": {
    "instructions": "", // Optional instructions to provide in addition to the label
    "media_types": "photo", // Options "photo, video, library - can list multiple such as "photo, video" if you will allow both the mobile camera to capture both photos and videos. Library means user can add media from their local library
    "media_limit": 1 // How many media items can be added
}
```

### Text Area

Example:
```javascript
{
  "component_type": "text_area",
  "label": "Text label to display",
  "name": "internal_name",
  "required": "yes",
  "extra": {
    "instructions": "", // Optional instructions to provide in addition to the label
    "character_limit": 140 // Maximum characters to enter in the field
}
```

### Tag selector

Example:
```javascript
{
  "component_type": "tags_collection",
  "label": "Text label to display",
  "name": "internal_name",
  "required": "yes",
   "extra": {
     "instructions": "", // Optional instructions to provide in addition to the label
     "values": [
       {"value": 1, "text": "Tag 1"},
       {"value": 2, "text": "Tag 2"},
       {"value": 3, "text": "Tag 3"},
       {"value": 4, "text": "Tag 4"},
       {"value": 5, "text": "Tag 5"}
       ]
}
```


