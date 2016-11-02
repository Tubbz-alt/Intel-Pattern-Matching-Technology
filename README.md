# Intel® Pattern Matching Technology

This repository contains the Intel Pattern Matching Library code that can run on the Pattern Matching Engine in the Intel® Curie™ Compute Module, which is used on the Arduino/Genuino 101 from Arduino and the tinyTile from Farnell.

## Development Environments

This library can be used in the following development environments:

* On Ubuntu 14.04 LTS or 16.04 LTS, using the latest version of the Curie Open Development Kit - Mixed Tree (CODK-M)

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

1. The Intel Pattern Matching Library is pre-installed as part of the Curie ODK in the Corelibs libraries directory:  `$(ARDUINOSW_DIR)/corelibs/libraries `

2. In your project, edit your Makefile and add the following:

        LIBDIR = $(ARDUINOSW_DIR)/corelibs/libraries/Intel-Pattern-Matching-Technology/src 
