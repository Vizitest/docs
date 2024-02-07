# Sample Projects and Test Server

We provide a simple test server application that you can download from Github. 

It is a Python application that allows you to simulate a development and production environment (and any other environments for that matter).

## Installation of the Test Server
1. Clone the [GitHub repository](https://github.com/Vizitest/play-server) onto your machine.
2. Follow the instructions in README.md to get it up and running. If you have installed the Vizitest Learn project then an API Configuration will already be present in the project.
3. Confirm the server is running at ```http://localhost:33291/api```.

## Sample Projects
Our sample projects can be found on Github. To install these into Vizitest...

- Clone the repository to your computer.
- In the Vizitest Test Manager, press the + button in the Projects section of the left sidebar.
- Select the **Existing** tab in the new project dialog.
- Enter a project name (Vizitest Learn/Credit Check).
- Enter the path of the folder you cloned the repository into.
- The project should now open and you should see some groups with test configurations.

### Learn project

Clone the [Learn repository](https://github.com/Vizitest/vizitest-learn).

### Credit Check

Clone the [Credit Check repository](https://github.com/Vizitest/vizitest-learn).

### Create an API

You should then [create an Api](API-Configurations.md) in the left sidebar. Configure it by adding the following servers.

- **development** : ```http://localhost:33291/server/development```
- **production** : ```http://localhost:33291/server/production```

The both access the same server but use a development/production namespace for illustrative purposes.

### Selecting the active server
In the sidebar, select one of the environments from the dropdown. This will now be your default server for any tests you build.

<img src="change-active-server.png" width="400" alt="select active server"/>
