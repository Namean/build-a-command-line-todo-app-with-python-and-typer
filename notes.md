# Notes


## Table of Contents

- Demo
- Project Overview
-



## Demo

In this step-by-step project you'll build a command-line interface (CLI) application to manage a to-do list.
You application will provide a CLI based on Typer, a modern versatile library for creating CLI applications.



## Project Overview

The name of the application is called `rptodo`.

You want your application to have a user-friendly command-line interface that allows your users to interact
with the app and manage their to-do lists.

To start off, you want your CLI to provide the following global options:

-v or --version shows the current version and exits the application
--help shows the global help message for the entire application


You'll see these same options in many other CLI applications out there. It's a nice idea to provide them because most
users who work with command line expect to find them in every app.


_____________________________________________________________________________
| Command          | Description                                            |
| --------------   | -------------------------------------------------------|
| init             | Initialize the application's to-do database            |
| add DESCRIPTION  | Adds a new to-do to the database with a description    |
| list             | Lists all the to-dos in the database                   |
| complete TODO_ID | Completes a to-do by setting it as done using its ID   |
| remove TODO_ID   | Removes a to-do from the database using its ID         |
| clear            | Removes all the to-dos by clearing the database        |
----------------------------------------------------------------------------|


These commands provide all the functionality you need to turn your to-do application
into a minimum viable product (MVP) so that you can publish it to PyPI or the platform
of your choice and start getting feedback from your users.

To provide all these features in your to-do application, you'll need a few tasks:

1. Build a command-line interface capable of taking and processing commands, options, and arguments
2. Select an appropriate data type to represent your to-dos
3. Implement a way to persistenly store your to-do list
4. Define a way to connect that user interface with the to-do data


These tasks relate well to what is known as the Model-View-Controller design,
which is an architectureal pattern. In this pattern, the model takes care of the data
the view deals with the user interface, and the controller connects both ends to make the application
work.


The main reason for using this patter in your application and projects is to provide `separation of concerns (SoC)`
making differnt parts of your code deal with specific concepts independently.

The next decision you need to make is about the tools and libraries you'll use to tackle each of the tasks you defined
further up. In other words, you need to decide your `software stack`. In this tutorial, you'll use the following stack:


- `Typer` to build the to-do application's CLI
- Named tuples and dictionaries to handle the to-do data
- Python's json modle to mange persistent data store

You'll also use the config parser module from the PYthon standard library to handle the application's inital settings
in a configuration file. Within the configuration file, you'll store the path to the to-do database in your file system.
Finally, you'll use pytest as a tool for testing your CLI application.


## Prerequisites

To complete this tutorial and get the most out of it, you should be comfortable with the following topics:


- The Model-View-Controller pattern
- Command-line interfaces (CLI)
- Python type hints, also known as type annotations


