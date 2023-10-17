# Building-CRUD-API

# Todo App CRUD API

This is a simple RESTful CRUD (Create, Read, Update, Delete) API for managing a list of todos. The API is built using the Spring framework in Java.

## Endpoints

- **Add a Todo**
  - **URL:** POST `/todo`
  - **Description:** Add a new todo item to the list.
  - **Request Body:** JSON representation of a Todo object.
  - **Response:** "todo added"

- **Get All Todos**
  - **URL:** GET `/todos`
  - **Description:** Retrieve a list of all existing todo items.
  - **Response:** A JSON array containing all the todos.

- **Set Todo Status by ID**
  - **URL:** PUT `/todo/id/{id}/status`
  - **Description:** Update the status (completed or not) of a specific todo item by its ID.
  - **Parameters:**
    - `{id}`: The ID of the todo to be updated.
    - `status`: A query parameter to set the status (boolean).
  - **Response:** "todo : {id} updated to {status}" if successful, or "Invalid id" if the provided ID doesn't match any todos.

- **Delete Todo by ID**
  - **URL:** DELETE `/todo/id/{id}`
  - **Description:** Delete a todo item by its ID.
  - **Parameters:**
    - `{id}`: The ID of the todo to be deleted.
  - **Response:** "todo: {id} removed" if successful, or "Invalid id" if the provided ID doesn't match any todos.

- **Add a List of Todos**
  - **URL:** POST `/todos`
  - **Description:** Add a list of todo items to the existing list.
  - **Request Body:** JSON array containing multiple Todo objects.
  - **Response:** "{number of todos} todos were added"

- **Get All Undone Todos**
  - **URL:** GET `/todos/undone`
  - **Description:** Retrieve a list of todos that are not marked as completed.
  - **Response:** A JSON array containing all the undone todos.

- **Delete Todos by IDs**
  - **URL:** DELETE `/todos/ids`
  - **Description:** Delete multiple todos by their IDs.
  - **Request Body:** JSON array containing IDs of todos to be deleted.
  - **Response:** A JSON array containing the updated list of todos after removal.

## Example Usage

You can use this API to manage your todo list with basic CRUD operations. Here are some sample requests:

- **Adding a Todo:**
  - `POST` to `/todo` with a JSON body containing the new todo item.
  
- **Updating Todo Status:**
  - `PUT` to `/todo/id/{id}/status?status=true` to mark a todo as completed.

- **Deleting a Todo:**
  - `DELETE` to `/todo/id/{id}` to remove a todo by its ID.

- **Adding Multiple Todos:**
  - `POST` to `/todos` with a JSON array containing multiple todo items.

- **Getting Undone Todos:**
  - `GET` to `/todos/undone` to retrieve all todos that are not marked as completed.

- **Deleting Multiple Todos by IDs:**
  - `DELETE` to `/todos/ids` with a JSON array of IDs to delete multiple todos at once.

Please note that this API is a basic implementation and doesn't include features like authentication or advanced error handling. It's intended as a simple example for understanding CRUD operations in a Spring-based application.
