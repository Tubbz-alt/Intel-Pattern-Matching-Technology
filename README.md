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

## About the Library
The Intel® Pattern Matching Technology library provides the API's necessary to implement a supervised machine-learning pattern matching or classification algorithm which is accelerated by the hardware pattern matching engine.

  + Basic Functions Supported:
     * Learning Patterns
     * Recognizing Patterns
     * Storing Pattern Memory (Knowledge) [Requires SerialFlash Library]
     * Retrieving Pattern Memory (Knowledge) [Requires SerialFlash Library]

## About the Intel® Curie™ Pattern Matching Engine

The Pattern Matching Engine (PME) is a parralel data recognition engine with the following features:
  + 128 parallel arithmetic units (Processing Element or PE) with 8-bit features per PE.
  + Support for up to 128 Contexts
  + Support for up to 32,768 Categories
  + 128 byte input vector and model memory.
  + Two Transfer Functions:
  
     * k-nearest neighbors (KNN)
     * Radial Basis Function (RBF)
     
  + Two distance evaluation norms with 16-bit resolution:
     
     * L1 (Manhattan) Distance 
     * Lsup Distance
     
  + Classification states:
  
     * ID - identified, only one category matches
     * UNC - uncertain, more than one category matches
     * UNK- unknown, no match
    
     
