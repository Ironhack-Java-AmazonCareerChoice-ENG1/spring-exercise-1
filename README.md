# Task Manager Application using Spring Boot

This exercise aims to create a simple command-line Task Manager Application using Spring Boot. The tasks will be stored in an in-memory database.
Task 1: Create Spring Boot Application

Start a new Spring Boot project
Task 2: Define Task Model

## Create a Task model with the following fields:

    id (Long)
    title (String)
    description (String)
    status (Enum: PENDING, COMPLETED)

## Task 3: Create Task Repository

Create a TaskRepository class. This repository will act as an in-memory database. The repository should provide the following methods:

    save(Task task) - to save a task
    findAll() - to return a list of all tasks
    findById(Long id) - to return a task with a specific id
    deleteById(Long id) - to delete a task by id
    update(Task task) - to update a task

## Task 4: Task Service Layer

Develop a TaskService that will utilize the TaskRepository. Implement the following methods:

    addTask(Task task) - to add a task to the repository
    getAllTasks() - to fetch all tasks from the repository
    getTaskById(Long id) - to fetch a specific task by id from the repository
    deleteTask(Long id) - to remove a task from the repository by id
    updateTask(Task task) - to update the details of a task in the repository
    updateStatus(Long id, Status status) - to update the status of a task (PENDING/COMPLETED) in the repository

## Task 5: Command Line Interface

Implement CommandLineRunner to provide a command-line interface to interact with the Task Manager application. It should use TaskService and allow the following operations:

    Add a new task
    View all tasks
    View a task by ID
    Delete a task by ID
    Update a task's details
    Update a task's status
    Exit the application

Use the Scanner class to take input from the console for these operations. Provide a menu for the user to select from these options.

Ensure that your application is interactive and provides appropriate prompts and feedback to the user. The user should be able to navigate through the options smoothly.
