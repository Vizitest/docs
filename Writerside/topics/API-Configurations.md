# API Configurations

API testing means you will connect to local or remote APIs that you want to test.

## Adding the API
Ensure that you have selected a project, then click on the **+ API** button in the sidebar.

<img src="add-api.png" width="300" alt="add api"/>

Next, enter a friendly name for the server. You can edit this name later if required.

<img src="newly-added-api.png" width="300" alt="newly added api"/>

## Configuring the API

You edit the base API configuration by hovering on the server and then pressing the pencil icon. You will see the following dialog.

All configuration data you provide here should be thought of as defaults that can be overridden as required in actual test configurations.

### Servers
We provide a test server for you to play with. [Click here](The-Test-Server.md) for details on installing and using it. All examples in this user guide use this server.

<img src="configure-api.png" width="500" alt="configure api"/>

You can see we've added two servers called **production** and **development** and provided corresponding host names. 

If you are learning, we suggest you configure these two servers.

- **production** : ```http://localhost:33291/server/development```
- **development** : ```http://localhost:33291/server/production```

Urls should not end with a / character. If one is detected, it will be removed.

You can add additional servers if you require.

The servers you provide can then be selected in the left sidebar. This allows you to switch between servers to test against from a central location rather than having to modify any actual test configurations.

<img src="api-active-select.png" width="300" alt="select api server"/>

Select the ```development``` server for use later on.

## Headers and Cookies
You can also add any standard headers and cookies as required. You do not have to provide any but the benefit is you can add commonly used headers and cookies. These will then automatically be available within a test configuration for you to select from. This saves time so you don't have to specify them repeatedly for endpoint tests.

## Security
Coming soon, this is where you can centrally configure various security configurations.
