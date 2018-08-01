## Breakdown of a Task

You can add tasks via the mobile application or website - but in all cases a task follow the rules laid out when you add tasks via the API using our standard JSON:

```javascript
{
      "task": {
        "name": "This is the main title of the task",
        "details": "Additional details of the task - inserts images, video's, audio plus limited html tags.",
        "region_based": false, //allocate the task to users in a geo-location
        "lat": 0,
        "lng": 0,
        "radius": 300,
        "task_ttl": 0, // How long the task lives before being removed, 0 means never
        "user_ttl": 0, // If the task has been allocated to a user, how long do they have to process it, 0 means never
        "process_count": 0, // Sets number of times a task can be processed, 0 means unlimited
        "user_multi_process": true, // If true a single user can complete the same task multiple times
        "payment_unit": 1, // The amount of points to assign to successful completion of this task
        "task_processing_components": [
          {
          "component_type": "audio_file",
          "label": "Record an interview now",
          "name": "interview",
          "required": "yes",
          "extra": {
            "max_length": 120 // Max audio file length in seconds
          },
          {
          "component_type": "tags_collection",
          "label": "Select tags",
          "name": "tags",
          "required": "yes",
          "extra": {
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
            "character_limit": 140
          },
         }
        ]
      }
}
```
