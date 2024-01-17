# The Test Server

We provide a simple test server application that you can download from Github. 

It is a Python application that allows you to simulate a development and production environment (and any other environments for that matter).

## Installation of the Test Server
1. Clone the [GitHub repository](https://github.com/Vizitest/play-server) onto your machine.
2. Follow the instructions in README.md to get it up and running. If you have installed the Vizitest Learn project then an API Configuration will already be present in the project.
3. Confirm the server is running at ```http://localhost:33291/api```.

## Installation of the Vizitest Learn project
This is a simple repos
1. Clone the [Vizitest Learn repository](https://github.com/Vizitest/vizitest-learn).
2. Follow the installation instructions in the README.md file to install into Vizitest.

## Creating a new project
If you have not installed the Vizitest Learn project and want to set up your own project and tests from scratch, then please follow these steps.

### Create a new project
Instructions for adding a new project can be found [here](Add-new-project.md). 

### Create a Vizitest API

You should then [create a Vizitest](API-Configurations.md) API in the left sidebar. Configure it by adding the following servers.

- **development** : ```http://localhost:33291/server/development```
- **production** : ```http://localhost:33291/server/production```

### Selecting the active server
In the sidebar, select one of the environments from the dropdown. This will now be your default server for any tests you build.

<img src="change-active-server.png" width="400" alt="select active server"/>

You can switch servers at any time and all tests will then use that server. You will probably just use **development**.