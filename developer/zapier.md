# Zapier

TASKIO has a fully integrated Zapier app that allows you to add tasks from, and send processed task information to 1000+ other applications.

Our integration is currently invite only via this link: [https://zapier.com/developer/invite/96028/95cb9261d387cd079bdf5f0f41d8236b/](https://zapier.com/developer/invite/96028/95cb9261d387cd079bdf5f0f41d8236b/)

## Configuring Tasker Actions

What actions do you want Taskers to take? How should users process your tasks? What information do you want returned?

This is where you configure your "Tasker Actions" in the Zapier integration.

The Zapier app uses our standard [Task Processing Components](/developer/components.md) to allow you to request all sorts of data back from your Taskers. Remember to wrap your componenent JSON inside suqre brackets!

### Example Tasker Action JSON to test with

```javascript
[
          {
            "component_type": "tags_collection",
            "label": "Does this make sense?",
            "name": "tags",
            "required": "yes",
            "extra": {
              "instructions": "Let us know how easy to understand the typography demonstration is - did it give you insight into how to form useful tasks?",
              "values": [
                {"value": 1, "text": "100% clear"},
                {"value": 2, "text": "Easy"},
                {"value": 3, "text": "Could be better"},
                {"value": 4, "text": "Foggy!"},
                {"value": 5, "text": "Help!"}
              ]
            }
          },
          {
            "component_type": "text_area",
            "label": "Optional personal feedback",
            "name": "my_feelings",
            "required": "no",
            "extra": {
              "instructions": "",
              "character_limit": 140
            }
           }
        ]
```
