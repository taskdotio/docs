# TASKIO technical docs

This area provides technical information to interact and develop on the Taskio platform.

## API documentation

The latest version of our [API documentation can be found here](https://api.task.io/docs).

## Projects

Projects have a simple structure which is [defined here](/developer/project.md).

## Tasks

At the heart of the Taskio platform is the ability to process all types of tasks. 

### Task construction

A Task has two key building blocks:

1. [The Task Breakdown](/developer/task.md)
2. [Task Processing Components](/developer/components.md)

The [Task breakdown is represented by JSON](/developer/task.md) and provides all parameters you can utilise to add Tasks to your projects. But for any task, you will want some form of processing to be performed on your tasks - and the [Task Processing Components](/developer/components.md) are the building blocks that allow you to do this.

A Task can just have one processing component, or it can have multiple ones.

### Adding Tasks

1. Use our API to inject tasks (documentation will be linked to here soon)
2. Use our [Zapier integration](/developer/zapier.md) as an easy method to [add tasks from over 1000 applications](https://zapier.com/)

