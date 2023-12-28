# The Test Server

We provide a simple test server application that you can download from Github. 

It is a Python application that allows you to simulate a development and production environment (and any other environments for that matter).

## Installation
1. Clone the [GitHub play-server repository](https://github.com/Vizitest/play-server).
2. Follow the installation instructions in the README.md file
3. Confirm the server us running at ```http://localhost:33291/api```.

## Create a Vizitest API
You should first [create a Vizitest](API-Configurations.md) API in the left sidebar. If you've not already done so, configure it by adding the following servers.

- development : ```http://localhost:33291/server/devlopment```
- production : ```http://localhost:33291/server/production```

## Selecting the active server
In the sidebar, select one of the environments from the dropdown. This will now be your default server for any tests you build.

<img src="change-active-server.png" width="400" alt="select active server"/>

You can switch servers at any time and all tests will then use that server.