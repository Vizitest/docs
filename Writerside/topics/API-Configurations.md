# API Configurations

API testing means you will connect to local or remote APIs that you want to test.

## Adding the API
Ensure that you have selected a project, then click on the + API button in the sidebar.

<img src="add-api.png" width="300" alt="add api"/>

Next, enter a friendly name for the server. You can edit this name later.

<img src="newly-added-api.png" width="300" alt="newly added api"/>

## Configuring the API

### Servers
You edit the base API configuration by hovering on the server and then pressing the pencil icon. You will see the following dialog.

All configuration data you provide here should be thought of as defaults that can be overridden as required in actual test configurations.

<img src="configure-api.png" width="500" alt="configure api"/>

You can see we've added a server called production and provided a host name. This url should not end with a / character. If one is detected, it will be removed.

You can add as many servers as you require, such as **development**, **staging** etc.

The servers you provide can then be selected in the left sidebar. This allows you to switch between servers to test against from a central location rather than having to modify any actual test configurations.

## Headers and Cookies
You can also add any standard headers and cookies as required. You do not have to provide any. The purpose is that you can add as many commonly used headers and cookies. These are then optionally available within a test configuration and save you time having to specify them for each endpoint test.

## Security
Coming soon, this is where you can centrally configure various security configurations.
