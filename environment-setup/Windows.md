# Install ESP-IDF on Windows
- Please refer to ESP-IDF's official documentation [Standard Toolchain Setup for Windows](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/windows-setup.html#esp-idf-tools-installer)

- Please also refer to [Mair's video tutorial for installation on Windows](https://learnesp32.com/videos/1/1_%5Bwindows%5D%20installing%20the%20esp-idf)

## Get ESP-IDF Tools Installer
 Download one of ESP-IDF Tools Installer
 [ESP-IDF Tools Installer](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/windows-setup.html)

>:bulb: It is recommended to install ESP-IDF directly under your local drive, for example:
```c
// Will install ESP-IDF master into:
      C:\esp\esp-idf
// IDF tools directory (IDF_TOOLS_PATH): 
      C:\esp\tools\.espressif
```
At the end of the installation process, choose the prompt you would like to use to launch ESP-IDF environment, for example:

<img src = "./image/cmd.png" width = "300"> <img src = "./image/cmd-shortcut.png" width = "300">

Note that when launching the ESP-IDF Command Prompt, it automatically runs `export.bat` script to set up the environment variables (`PATH`, `IDF_PATH` and others)

<img src = "./image/esp-idf-installer-powershell.png" width = "600"> 

## Start an example project
ESP-IDF provides a sample project called `hello_world`, navigate to the folder where `hello_world` locates

```sh
cd \Users\<UserName>\esp\esp-idf\examples\get-started\hello_world
```
## Connect Your Device
Connect your ESP32 board to the computer and check under which serial port the board is visible


## Build your project
To build the example project, run
```sh 
idf.py build
```
If succeed, you should see the following output

<img src = "./image/idf-build-windows.png" width = "500">


# Install ESP-IDF on Windows via WSL2 
Please refer to Hwan's documentation [doc-tinyml](https://github.com/MACSO-AI/doc-tinyml/blob/main/main.pdf)
