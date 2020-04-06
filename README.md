# ReDBox 1.8 Sample Institutional Build

This is a sample institutional build to aid developers in porting their existing institutional builds across to the new format. By utilising the new format in conjunction with the [redbox-build-distro distribution of ReDBox](https://github.com/redbox-mint/redbox-build-distro), the new format removes the dependency on Maven.

## Porting an existing institutional build

### 1. Clone this project

Clone this project to get the basic structure.

### 2. Copy template and configuration changes to their new location

Delete the existing sample files from the Copy the files and directories that were previously in the [src/main/config](https://github.com/redbox-mint/redbox-build-distro/tree/master/src/main/config) directory to the root of your project.

### 3. Restructure the system-config.json

To allow new configuration items to be added to future releases without causing issues with local customisations, the system-config.json has been split up into a many smaller configuration files (named by their category) in the [home/config-include](https://github.com/redbox-mint/redbox-build-distro/tree/master/src/main/config/home/config-include) directory. These files are merged at runtime to form a structure exactly the same as the original system-config.json format.

Copy your local changes in your existing system-config.json into the corresponding configuration file in config-include. For best results, only include files in your institutional build that contain local changes.

## Deploying your 1.8 institutional build

The 1.8 institutional build structure mimics the application structure and simply is overlaid over the deployed redbox-build-distro distribution to have your customisations applied.

Please follow the links on our old documentation website for:
* [installation](http://docs.redboxresearchdata.com.au/documentation/installguide), and
* [customisation](http://docs.redboxresearchdata.com.au/documentation/how-to/institutional-builds).

*(For later builds against 1.x: see: https://www.redboxresearchdata.com.au/download/)*

*(For Redbox 2.x preview, please explore our demo site at: https://demo.redboxresearchdata.com.au/)*
