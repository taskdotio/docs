# Task formats

This provides you with a breakdown of the ways you'd typically setup tasks.

## Show title, text details (header)
A very plain text only task. Looks like this:

![t1](https://raw.githubusercontent.com/taskdotio/docs/master/images/t1.jpg)

### JSON to create this task
```
{
      "task": {
        "name": "Show title, text details (header)",
        "show_name": true,
        "details": "<h2>We start the details with a header 2</h2>Then finish off here with some normal paragragh text",
        "task_ttl": 0,
        "user_ttl": 0,
        "process_count": 0,
        "user_multi_process": true,
        "payment_unit": 1
      }
}
```


