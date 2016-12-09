# Intel® Pattern Matching Technology

This repository contains the Intel Pattern Matching Library library (CuriePME) that provides access to the Pattern Matching Engine (PME) within the Intel® Curie™ Compute Module. 

Supported Curie™ hardware platforms:

* Arduino/Genuino 101 (Arduino)

* tinyTILE (Farnell)


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

2. In addition, storing and retreiving knowledge needs the following Curie libraries:
  * [SPI] (https://github.com/01org/corelibs-arduino101/tree/master/libraries/SPI)
  * [SerialFlash] (https://github.com/01org/corelibs-arduino101/tree/master/libraries/SerialFlash)

  In your project, edit your Makefile and add the following:

  ```
    LIBDIRS = $(ARDUINOSW_DIR)/libraries/Intel-Pattern-Matching-Technology/src \
	          $(ARDUINOSW_DIR)/corelibs/libraries/SPI/src \
	          $(ARDUINOSW_DIR)/corelibs/libraries/SerialFlash

  ```

## About the Library
The Intel® Pattern Matching Technology library provides the API's necessary to implement a machine-learning pattern matching or classification algorithms which are accelerated by the hardware pattern matching engine.

  + Basic Functions Supported:
     * Learning Patterns
     * Recognizing Patterns
     * Storing Pattern Memory (Knowledge) [Requires SerialFlash Library]
     * Retrieving Pattern Memory (Knowledge) [Requires SerialFlash Library]

## About the Intel® Curie™ Pattern Matching Engine

The Pattern Matching Engine (PME) is a parralel data recognition engine with the following features:
+ 128 parallel Processing Elements (PE) each with"
  
  	- 128 byte input vector 
	- 128 byte model memory.
	- 8-Bit Arithmetic Units
	- Two distance evaluation norms with 16-bit resolution:
        	
		* L1 norm (Manhattan Distance)
        * Lsup (Supremum) norm (Chebyshev Distance)
		
	- Support for up to 32,768 Categories
	- Classification states:
  
           * ID  - Identified
           * UNC - Uncertain
           * UNK - Unknown
		
+ Two Classification Functions:
  
     * k-nearest neighbors (KNN)
     * Radial Basis Function (RBF)
	
+ Support for up to 127 Contexts
  
     

    
     
