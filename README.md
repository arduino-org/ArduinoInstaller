# Arduino IDE Windows Installer
this repository contains the Nullsoft Scriptable Install System (NSIS) script used to create the Windows installer of Arduino IDE.

## Tools and Requirements
* NSIS 2.46 can be downloaded here: http://nsis.sourceforge.net/Download
* File Association plugin for NSIS (include in this repo) under Plugins
* License file: license.txt


## Instructions

### Working Directory Structure
your Working Directory should be similar to:

* `LOCAL_FILES_PATH`/
    * script.nsi
    * License.txt
    * `files`/

Where:

* `LOCAL_FILES_PATH` : Local path to your Working Directory e.g.: *C:\Users\Sergio\ArduinoInstaller*
* script.nsi: is the NSIS script file
* License.txt: is the license file that comes with this repo.
* `files`: is a directory which contains the Arduino IDE files

## First steps
Install NSIS into your Windows PC and then open the .nsi script file and change `LOCAL_FILES_PATH` variable as explained above.

Unzip the Arduino IDE .zip file (that comes from ant building in windows) into the `files` directory and be sure about the naming of the unzipped folder that must be :
`arduino-X.Y.Z` where `X.Y.Z` is the version number of the IDE that you are releasing.

Change with the same version number the variable `PRODUCT_VERSION` inside the script file.

Put the `FileAssociation.nsh` plugin into the `Include` folder of NSIS: `C:\Programs Files\NSIS\Include\`

## Start Building
Open NSIS, load the script file and click the compile button. The .exe final installer will be created inside the Working Directory
