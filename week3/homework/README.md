# HackYourFuture Node.js Week 3 - Homework

### Assignment

### To-Do API

This week we wrote an Express application with request body in JSON
format.

There are 4 [CRUD](https://en.wikipedia.org/wiki/Create%2C_read%2C_update_and_delete)
actions:

#### `createTodo` (`POST /todos`)

  Creates a new to-do

#### `readTodos` (`GET /todos`)

  Reads and lists all to-dos

#### `updateTodo` (`PUT /todos/:id`)

  Updates the description of a to-do with ID `:id`

#### `deleteTodo` (`DELETE /todos/:id`)

  Deletes a to-do with ID `:id`

### Request Body Format

When calling the `create` or `update` actions, the request body must look like
this:

```json
{
  "todo": {
    "description": "(todo description)"
  }
}
```

Note that for these actions, the client must add the following header:

- `Content-Type`: `application/json`

In Postman, make sure to add this header, and set the Body type to _raw_ and
_JSON (application/json)_.


Read through the code from the lecture, make sure you understand the flow of the
program.

Add four more actions:

### `readTodo` (`GET /todos/:id`)

  Get a single to-do with ID `:id`

### `clearTodos` (`DELETE /todos`)

  Clears the list of to-dos

### `markAsDone` (`POST /todos/:id/done`)

  Sets the `done` flag of a single to-do to `true`

### `markAsNotDone` (`DELETE /todos/:id/done`)

  Sets the `done` flag of a single to-do to `false`

## Requirements

- All requests that need a body should be in JSON format, and follow the request
  structure of the other actions
- All responses should be in JSON format, and follow the response structure of
  the other actions
- Follow the anatomy of the project
- Make sure your code is [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)
- Follow the REST design principles: use the proper method, response status
  codes, and consistent URL paths
- Test your API using Postman
