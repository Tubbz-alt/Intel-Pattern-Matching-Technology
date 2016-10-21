# Intel® Pattern Matching Technology

This repository contains the Intel Pattern Matching Library code that can run on the Pattern Matching Engine in the Intel® Curie™ Compute Module, which is used on the Arduino/Genuino 101 from Arduino and the tinyTile from Farnell.

## Development Environments

This library can be used in the following development environments:

* On Windows, Mac-OS or Linux, using Arduino IDE version 1.6.12 or greater and Corelibs 1.0.7 or greater.
* On Ubuntu 14.04 LTS, using the latest version of the Curie Open Development Kit - Mixed Tree (CODK-M)

## Library Contents
```
Intel-Pattern-Matching-Technology
                                 |- src
                                        |- CuriePME.cpp
                                        |- CuriePME.h
                                 |- examples
                                        |- a_SimplePatternMatching
                                        |- b_SavingKnowledge
                                        |- c_RestoringKnowledge
                                        |- d_k-nearest-neighbor
                                        |- DrawingInTheAir 
```

## Library Usage CODK-M

1. From the GitHub repository, download the library Zip file and copy it into the user library folder in your CODK-M directory. Rename the library directory "Intel-Pattern-Matching-Technology".

        `$(ARDUINOSW_DIR)/libraries/ `

2. In the CODK-M directory, create a new project

        `make project PROJ_DIR=my_ipmt_sample `

3. Edit the Makefile and add the following:

        `LIBDIR = $(ARDUINOSW_DIR)/libraries/Intel-Pattern-Matching-Technology/src `

4. Copy an example sketch from the library into your project and use
        `make convert-sketch ` 
   or create your own C++ application file.

5. Build and Flash your project:

        ```
        $>make compile
        $>make upload SERIAL_PORT=/dev/ttyACM0
        ```

## Library Usage Arduino IDE

The Intel Pattern Matching Technology Library can be installed in the Arduino IDE just like any other Arduino Library using the Library Manager.

[Installing Additional Arduino Libraries](https://www.arduino.cc/en/Guide/Libraries)







