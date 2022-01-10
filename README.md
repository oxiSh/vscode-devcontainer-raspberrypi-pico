# VSCode DevConrainer RaspberryPi PICO C-SDK (WSL2)

## 3rd Party Utils
* [VS-Code](https://code.visualstudio.com/)
* [WSL update (x64)](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)
* [Docker Desktop](https://www.docker.com/products/docker-desktop)
* [usbipd](https://github.com/dorssel/usbipd-win/releases)
* [git](https://git-scm.com/download/win)
* [zadig (optional)](https://zadig.akeo.ie/)  

## VS-Code Extensions (only install them inside DevContainer)
* [Cortex Debug](https://marketplace.visualstudio.com/items?itemName=marus25.cortex-debug)
* [Remote Container](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
* [Remote WSL](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl)
* [Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)
* [CMake Tools](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cmake-tools)
* [Script Buttons](https://marketplace.visualstudio.com/items?itemName=JackWaterfall.script-buttons)

## ToDo
Enable SubSystem for Linux:
```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```
Enable ``SVM`` (AMD) or ``VT-x`` (Intel) in BIOS to ensure WSL-2 can run.


## This container includes
* [pico-sdk]()
* [openocd]()
* [picotool](https://github.com/raspberrypi/picotool)
* [bootterm](https://github.com/wtarreau/bootterm) (for serial monitoring) 
* [tio](https://github.com/tio/tio) (for serial monitoring)  


# Credits 
@mwinters-stuff 👍 awsome Template ❤️ <br>
@dorssel 👍 nice job on usbipd ❤️<br>
to all other, the name i dont know, yet!<br>




-----

Original ReadME

# vscode-devcontainer-raspberrypi-pico [![Create docker image](https://github.com/mwinters-stuff/vscode-devcontainer-raspberrypi-pico/actions/workflows/build-image.yml/badge.svg)](https://github.com/mwinters-stuff/vscode-devcontainer-raspberrypi-pico/actions/workflows/build-image.yml)
VSCode Dev Container for the Raspberry PI Pico C SDK

## Usage

Clone or download repository, copy the contents of .devcontainer into your project
Remove any existing "build" directory.

Open the folder, and allow the container to build.

# To know
* SDK is installed in /pico-sdk
* All USB devices are exported to container - so the picoprobe can be found and used.
* USB Device /dev/ttyACM0 is exported to container for monitoring

## This container includes
* pico-sdk
* openocd - compiled for picoprobe
* picotool
* bootterm (for serial monitoring) - see https://github.com/wtarreau/bootterm

##Test
