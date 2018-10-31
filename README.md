## Requirements

- Build desktop native app with Meteor Javascript as the main framework
- Use Angular as part of Meteor Integration
- Need to use dynamic JSON Schema form to render the application layout.
- All data can use static values, we will running another challenge that will able to process some client standard configuration files

## Description

A PDU (Power Distribution Unit) is a device fitted with multiple outputs designed to distribute electric power, especially to racks of computers and networking equipment located within a data center.  The PDU Mass Commissioning tool that we are designing will allow users to create configuration files and networking capabilities for PDUs in a system.  The app will allow for the necessary configuration parameters needed for operation within the system.  Once all of the configuration parameters have been set within the app, users will be able to "export" the files to a USB drive, which will be plugged into the PDUs to be commissioned.

The PDU Mass Commissioning tool will be a simple user interface that allows customers to create all of the necessary configuration files to configure all of their PDUs. The app will have a variable number of input fields for all the configuration parameters in which users will enter their desired configurations. Once they have entered all of the configuration parameters they will click "export" and the application will build the configuration file hierarchy into a chosen USB drive.

## Standard User Flow

1. User creates a CSV file from a provided template offline, and from outside of the application.
2. User opens Mass Commissioning app and goes to the general settings page
3. User clicks "upload configuration" button and selects the CSV file that was created outside of the app.
4. User goes to general settings configuration.  
5. User goes to Network Infrastructure settings and inputs necessary configurations.  See the provided spreadsheet for the settings and configurations sample data.  The items highlighted in Blue are the  configurations for Basic mode and are always present. The other items in White are expert features and depending on the PDU type, some of these will be shown on the app.  So just pick a few when designing for Expert mode.
6. User goes to Asset Management. A table displays all of the devices which were loaded from the CSV file in step 3. If no template has been loaded, the user will start from an empty wizard and add devices manually. The user configures each device’s specific settings by clicking the device and configuring the settings on the additional section which comes up for that device.  See the spreadsheet for the sample data.  The items highlighted in Blue are the  configurations for Basic mode and are always present. The other items in White are expert features and dependant on the PDU type.  So just pick a few when designing for Expert mode.
7. User goes to Export screen and confirms there are no validation issues.
8. User clicks the "Export" button and selects the USB drive they are exporting to
9. Application saves all configuration elements to a CSV file in a local application folder
10. Application converts the saved CSV file into the proper folder and file structure on the user's selected drive/folder
11. Application prompts user when export is complete
12. User unplugs the USB drive they exported to and plugs it into each of the PDUs that need to be configured
