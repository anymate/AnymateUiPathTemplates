# Anymate Enterprise Framework

Anymate provides Enterprise ready templates, based on the UiPath Robotic Enterprise Framework. 

## Flow Control 

The basic flow is set up for the get-go in Main.xaml, and everything is hooked up following Anymate Good Practice. 
Key steps are split up in seperate workflows, making it easy to extend as needed.


## Configuration

Keeping configuration values seperate from the code is pretty much a universal standard by now. 
In order to keep things familiar, the Anymate Enterprise Framework follows the style chosen by the UiPath Robotic Enterprise Framework and have included a configuration file, named Config.xlsx and located in the folder Data, which can be used to define project configuration parameters. 

From the REF-documentation:
```
These parameters are then read into the Config dictionary variable of the Main.xaml
file. This dictionary is also passed as arguments to other files of the framework.
For easier manipulation, this configuration file is an Excel workbook which has three
sheets:

* Settings: Configuration values to be used throughout the project and that
usually depend on the environment being used. For example, names of queues,
folder paths or URLs for web systems.
* Constants: Values that are supposed to be the same across all deployments of
the workflow. For example, department name or bank name to be input in a
certain screen.
* Assets: Values defined as assets in Orchestrator.
Rows in the Settings and the Constants sheets indicate keys and values that are read
into the Config dictionary during the initialization phase of the framework. The Name
column specifies a key in Config and the Value column defines the value associated
with that key. The Description column offers an explanation about the row, but it is not
included in the dictionary. 
``` 

We recommend always storing settings in the Orchestrator, making it easy to make adjustments without requiring a redeploy.

## Logging

Logging is baked in to the Framework, doing in proper logging at key steps in the Process.
