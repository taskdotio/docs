## Breakdown of a Task

You can add tasks via the mobile application or website - but in all cases a task is defined best using our standard JSON format. This is how you would add a task via our API.

The building blocks of the Task JSON are:

- The main task details such as name, time outs, regional information, how it gets processed and by who
- The way in which a task will get processed using our component library
-- Within the "processing_components" property one or more components may be defined 

Here is an example:

```javascript
{
      "task": {
        "name": "This is the main title of the task",
        "details": "Additional details of the task - inserts images, video's, audio plus limited html tags.",
        "region_based": false, //allocate the task to users in a geo-location
        "lat": 0,
        "lng": 0,
        "radius": 300,
        "task_ttl": 0, // How long before this task expires and is removed, 0 means never
        "user_ttl": 0, // If the task has been allocated to a user, how long do they have to process it, 0 means never
        "process_count": 0, // Sets number of times a task can be processed, 0 means unlimited
        "user_multi_process": true, // If true a single user can complete the same task multiple times
        "payment_unit": 1, // The amount of points to assign to successful completion of this task
        "components_attributes": [
          {
            "component_type": "audio_file",
            "label": "Record an interview now",
            "name": "interview",
            "required": "yes",
            "extra": {
              "instructions": "",
              "max_length": 120 // Max audio file length in seconds
              }
          },
          {
            "component_type": "tags_collection",
            "label": "Select tags",
            "name": "tags",
            "required": "yes",
            "extra": {
              "instructions": "",
              "values": [
                {"value": 1, "text": "Wow"},
                {"value": 2, "text": "Glitch"},
                {"value": 3, "text": "Exec report"},
                {"value": 4, "text": "Compliance issue"},
                {"value": 5, "text": "Call back"}
              ]
            }
          },
          {
            "component_type": "text_area",
            "label": "Tell us how you are feeling?",
            "name": "my_feelings",
            "required": "no",
            "extra": {
              "instructions": "",
              "character_limit": 140
            }
           }
          ]
        }
}
```

This examples has three components defined in the processing_components property, namely:
- audio_file - task worker can record audio
- tags_collection - task worker can choose from a set list of tags
- text_area - task worker can type written text in a text field

This is just a simple example of how a Task is constructed in Taskio. 

You can read about [Task Processing Components here](/components.md).
