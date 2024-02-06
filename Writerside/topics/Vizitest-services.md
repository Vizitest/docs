# Vizitest Services and Service Monitor 

## Vizitest Home Folder
Vizitest installs its services into the ```.vizitest``` home folder that is located at...

- Mac ```/Users/username/.vizitest```
- Windows ```C:/User/username/.vizitest```
- Linux ```/home/username/.vizitest```

## Vizitest Service Monitor
The Vizitest Service Monitor is a simple application that can be found in the Vizitest home folder. A version can be found for Windows (.exe), Mac (.dmg) and Linux (.AppImage). Start it to

- show the current status of the Vizitest services,
- start and stop the Vizitest services,
- get a shortcut button for opening Vizitest in your browser.
- change ports and service startup behaviour.

<img src="vizitest-monitor.png" width="600" alt="vizitest monitor"/>

## Starting and stopping from the command line
Once you have installed Vizitest, the services will be started automatically and will also auto-start when you restart your computer.

You can start and stop the Vizitest services from the command line. Please go to the ```.vizitest``` home folder, where you'll find the ```start``` and ```stop``` scripts.
