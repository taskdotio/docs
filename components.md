## Task Processing Components

Task Processing Components are the building blocks to allow you to get information back from users when they process your tasks.

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
       {"id": 1, "label": "Tag 1"},
       {"id": 2, "label": "Tag 2"},
       {"id": 3, "label": "Tag 3"},
       {"id": 4, "label": "Tag 4"},
       {"id": 5, "label": "Tag 5"}
       ]
}
```


