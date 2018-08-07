## Projects

Technical definitions and information around the Taskio projects.

### Technical structure

Taskio project consist of:
```javascript
{
  "title": "Name of the project",
  "start_date": 0, // Unix format (team can access the project but cannot work on tasks until date passes, 0 means no start date)
  "end_date": 0, // Unix format (team can access the project but cannot work on tasks once date passes, 0 means project never ends)
  "short_description": "A short description of the project limited to 200 characters maximum",
  "long_description": "A long description of the project - provides an overview of the project and the tasks to expect. Can contain videos and other media, plus links to external sites",
  "url": "project", // Allows for an easy to share url slug in format account/project
  "tags": {  // User tagged categorisation of projects
    "tags 1": "tags 1",
    "tags 2": "tags 2"
  },
  "publishing": private, // Display project on public task.io/account page - options "public", "private"
  "join_policy": invite // How to join the channel, options "open" (anyone can join and process tasks) or "invite" (invite only)
}
```
