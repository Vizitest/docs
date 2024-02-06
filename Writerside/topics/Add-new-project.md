# Add new project

A project stores API and Test configurations organized into groups.

## Project folder
Before you create your new project, prepare a folder where the Vizitest project data should be stored. This can be anywhere on your machine.

## Git
You may want to initialise this folder as a git repository. This will allow you to collaborate with others. 

All Vizitest data is stored as text files, so it works well with Git.

## New vs. Existing project
A Vizitest project is simply a folder somewhere on your machine. For brand new projects, you can create an empty folder on your machine. Once you have added the project to Vizitest, you will see a ```.vizitest``` sub folder that contains your groups and test configurations.

When adding a project, you will either be 

- creating a brand new, empty project
- or adding a project that already contains Vizitest test configurations (collaborating on Git, you've been sent the project folder, you've removed it and are adding it back in).

## Create the project
To add a new project, click the + button next to **Projects**.

<img src="add-new-project.png" width="400" alt="add new project"/>

For a brand new project, select the **New** tab. If you already have a Vizitest project folder, select **Existing**.

1. Enter a project name, such as **Vizitest Learn**. This can only contain valid file name characters.
2. Provide the name of a folder where your project can be found. This can be anywhere on your machine but it must be a valid, absolute path and must already exist.

For new projects, you can optionally add...

3. A description.
4. A color. The color only servers as a visual aid to easily differentiate projects from one another.

When you click **Confirm**, and if your are creating a new project, a ```.vizitest``` folder will be created inside your root folder that contains all project related information. 

You will now see your newly created project in the left sidebar. It should be automatically selected and ready to work with.

<img src="project-added.png" width="600" alt="add new project"/>

You can also see that a group has been created. More about groups shortly.

## Editing the project
You can change the project name, description and color later by pressing the pencil icon in the bottom right corner of the Project name box (see above image).

You cannot change the project path once created.
 