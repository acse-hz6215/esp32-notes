 
Mair’s ESP32 course: https://learnesp32.com/

Here's is a summary of Mair's course notes 
  

# Table of Contents
- [Table of Contents](#table-of-contents)
- [Environment Setup](#environment-setup)
  - [Flash commands](#flash-commands)
  - [Starter template](#starter-template)
- [Introduction](#introduction)
  - [Logging](#logging)


# Environment Setup 
  
## Flash commands
```sh
#check serial ports
ls /dev/cu.*   

# set environment variables
. $HOME/esp/esp-idf/export.sh 

idf.py set-target TARGET

idf.py -p PORT

idf.py build

#this will actually flash and build the same time
idf.py flash 

# this will flash while monitoring flashing process
# to stop use 'ctrl + ]'
idf.py flash monitor 

idf.py fullclean
  ```
## Starter template
- main
  - `component.mk` - useless
  - `main.c`- source code
  - `CMakeList.txt` - all the files used for configuration, including source files and imported header files. Note that there's also a `CmakeList` outside the main folder, which is responsible for importing files outside the project, and this one is responsible for files inside the project.

- project root path
  - `CMakeList.txt` - all files from the outside of the project that are used configuration 
  - `MakeFile` - useless
  - `sdkconfig` - configuration file, changing the configuration can also be done by using `idf.py menuconfig`

 ESP32 starter template on Github: https://github.com/Mair/esp32-course/tree/master/_2_template/esp32_starter_template

# Introduction 
## Logging