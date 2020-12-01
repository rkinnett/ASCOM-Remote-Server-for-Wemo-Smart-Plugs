# ASCOM-Remote Server for Wemo Smart Plugs
This appliation is designed to run alongside your astronomy software, relaying commands and status to and from a single Wemo smart plug.
  
## Requirements:
A Wemo smart plug connected to your local network.

ASCOM platform:  https://ascom-standards.org/Downloads/Index.htm

ASCOM Alpaca, aka ASCOM Remote:  https://github.com/ASCOMInitiative/ASCOMRemote/releases
  
Java runtime environment, if running the jar file (not needed if running the exe):  https://www.java.com/en/download/
  
  
## Installation
This application does not require installation.  Just download the jar, zip, or exe file from the latest Release and save it anywhere on your filesystem.

The exe should work on most modern Windows platforms, but your antivirus may flag it as malicious, in which case you can either configure an exception for the exe file, or use the jar file instead.

The jar file requires Java Runtime Environment which you can get here:  https://www.java.com/en/download/

## Running the server
Start the exe or jar file by double-clicking in windows, or via command line.
  
The application provides instructions in the log area.
  
Step 0) Find out the local IP address of your Wemo switch.  You can use the scan feature of this application to look for available devices on your local network.  The scan feature displays information about any switches it finds, and takes no further action.  It's up to you to figure out which IP address represents the switch you want to control.
  
Step 1) Set the IP address of your Wemo switch, press enter or click the Set button.  If the application successfully connects to your switch, then information will be displayed in the log window and the application will enable the Start Server button.  You can try toggling the switch from the server application at this point to test, if desired.
  
Step 2) Enter a port number (or use default 8080) for the ASCOM server and click Start Server.
  
Step 3) In the equipment connection menu for your astronomy software, load the ASCOM Remote Client driver as a switch device, and opent the driver settings menu.  Select "http" service type, enter 127.0.0.1 as the Remote Device Server Name or IP Address, enter the port number you specified as the Server Port in the Wemo ASCOM Server application.  Confirm these settings and start the device.

That's it!  The name and state of your device should now be displayed in your astronomy software, and the switch should be controllable from both your astronomy software and the server application.

## Building this project
This project was built in Netbeans IDE 12.1 with Gradle Build Tool, with Java runtime 15.0.  Open the project in Netbeans and run Build.
