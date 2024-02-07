# Vizitest Services and Service Monitor 

## Vizitest Home Folder
Vizitest installs its services into the ```.vizitest``` home folder that is located at...

- Mac ```/Users/username/.vizitest```
- Windows ```C:/User/username/.vizitest```
- Linux ```/home/username/.vizitest```

## Vizitest Service Monitor
The Service Monitor is not installed automatically. Follow these steps to install it.

- Locate the ```vizitest_monitor``` app (.exe, .dmg, .appimage) in the Vizitest home folder as explain above.
- Run the ```vizitest_monitor``` to install it.

The monitor performs the following tasks.

- Shows the current status of the Vizitest services.
- Start and stop the Vizitest services,
- Shortcut button for opening Vizitest in your browser (we recommend bookmarking this in your browser for future use)
- Change ports and service startup behaviour.

<img src="vizitest-monitor.png" width="600" alt="vizitest monitor"/>

## Starting and stopping from the command line
Once you have installed Vizitest, the services will be started automatically and will also auto-start when you restart your computer.

The easiest way to start and stop the Vizitest services is from the monitor. However, you can also install it from the command line. 

Go to the ```.vizitest``` home folder, where you'll find the ```start``` and ```stop``` scripts.
