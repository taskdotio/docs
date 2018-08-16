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
    "media_types": "photo", // Options "photo, video, library, scan - can list multiple such as "photo, video" if you will allow both the mobile camera to capture both photos and videos. Library means user can add media from their local library. Scan lets us set a scan icon in the widget.
    "media_limit": 1 // How many media items can be added
}
```

### LogIt

The LogIt componenent allows you to record specific values when a task is completed. Sometimes the action of completing a task is enough (if the task is to record logging a filled bag of rubbish for example).

The LogIt component can be hidden or shown in the Task canvas area (Currently we only support hidden, shown is coming soon).

Example:
```javascript
{
  "component_type": "logit",
  "label": "Text label to display", // If visibity=hidden, then this will not display
  "name": "internal_name",
  "required": "yes",
  "extra": {
    "instructions": "", // Optional instructions to provide in addition to the label - if visibity=hidden, then this will not display
    "visibility": "hidden", // Options "hidden, shown"
    "value": 1, // Value to provide against your choswn unit
    "unit": "" // Examples: kg, bag, m, mm, ...
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


