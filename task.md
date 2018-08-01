## Breakdown of a Task

You can add tasks via the mobile application or website - but in all cases a task follow the rules laid out when you add tasks via the API using our standard JSON:

`
{
      "task": {
        "name": "This is the main title of the task",
        "details": "Additional details area, inserts images files, plus limitedhtml layout of content.",
        "region_based": false, //allocate to users in a geo-location
        "lat": 0,
        "lng": 0,
        "radius": 300,
        "ttl": 0, // How long the task lives before being removed, 0 means never
        "answers_count": 0, // sets number of answers per task, 0 means unlimited
        "multi_answer": true, // If true user can complete task multiple times
        "components_attributes": [
          {
          "component_type": "audio_file",
          "label": "Record an interview now",
          "name": "interview",
          "extra": {
            "max_length": 120 // Max audio file length in seconds
          },
          {
          "component_type": "tags_collection",
          "label": "Select tags",
          "name": "tags",
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
          "extra": {
            "character_limit": 140
          },
         }
        ]
      }
}
`
