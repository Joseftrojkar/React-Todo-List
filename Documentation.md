# Project Documentation

## 1. Contents

This project documentation contains information on a Todo app built using React. It describes what the app does, the technologies used, how it works internally, instructions on how to use the project, and possible future development.

## 2. What the app does

The Todo app is a web-based application that allows users to create, update, and delete tasks. The app enables users to add a new task to a list of existing tasks, toggle the completion status of a task, edit the task, and delete a task.

## 3. Description of the technologies used

This project was built using React, a popular JavaScript library for building user interfaces. The app uses React Hooks, which are a set of functions that allow developers to use state and other React features without writing a class. The app also uses the uuidv4 library to generate unique IDs for the tasks.

## 4. A detailed description of how it works internally

The `TodoWrapper` component is the main component that renders the application. It contains the state for the list of todos and provides functions to add, delete, toggle complete and edit tasks.

When a user enters a new task in the `TodoForm` component, it triggers the `addTodo` function which creates a new todo object with a unique ID generated using `uuidv4` and the task description entered by the user. The `completed` and `isEditing` properties of the todo object are set to `false` by default. The new todo is added to the list of todos by setting the state using `setTodos` and passing in the new list of todos that includes the newly added todo.

When the user clicks on the checkbox beside a task, it triggers the `toggleComplete` function which maps over the list of todos and toggles the `completed` property of the todo object with the given ID. The new list of todos is set as the state using `setTodos`.

When the user clicks on the delete button beside a task, it triggers the `deleteTodo` function which filters the list of todos to exclude the todo object with the given ID. The new list of todos is set as the state using `setTodos`.

When the user clicks on the edit button beside a task, it triggers the `editTodo` function which maps over the list of todos and toggles the `isEditing` property of the todo object with the given ID. This switches the view from the `Todo` component to the `EditTodoForm` component, which allows the user to edit the task description. Once the user submits the updated task description, the `editTask` function is called, which maps over the list of todos and updates the task property of the todo object with the given ID. The new list of todos is set as the state using `setTodos`.

The `TodoWrapperLocalStorage` component works similarly to the `TodoWrapper` component, but it also includes `localStorage` functionality to store the list of todos in the user's browser. When the component mounts, it retrieves the list of todos from `localStorage` and sets it as the initial state. Whenever the list of todos is updated, it is also saved to `localStorage` using `JSON.stringify`.

## 5. Instructions on how to use the project

To use the Todo app, follow these steps:

1. Clone the project repository from GitHub.
2. Open a terminal and navigate to the project directory.
3. Run `npm install` to install the project dependencies.
4. Run `npm start` to start the app.
5. Open a web browser and navigate to `http://localhost:3000/`.
6. Enter a task in the input field and click the "Add Task" button to add a new task.
7. Click the task to toggle its completion status.
8. Click the pencil icon to edit a task. Edit the task and click the "Add Task" button to update the task.
9. Click the trash icon to delete a task.

## 6. Possible future development/description of the actual use of the project

Possible future development of the Todo app includes adding features such as authentication, task prioritization, due dates, and reminders. The app can also be extended to allow users to share tasks with others and collaborate on tasks. Additionally, the app can be optimized to improve performance and user experience. The app can also be deployed to a cloud service provider to make it accessible to a wider audience. The actual use of the project can vary, depending on the user's needs. For example, the app can be used for personal task management or for team task management in a work setting.
