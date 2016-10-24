#How to Run the Examples

This procedure assumes that the user has already installed the Intel Pattern Matching Library
as described in the library README.

## Procedure to run examples on CODK-M

All of the examples are available at the following path:

        $(ARDUINOSW_DIR)/libraries/Intel-Pattern-Matching-Technology/examples 

1. In the CODK-M directory, create a working directory for your experiments

        $<UserName>/CODK/CODK-M/>mkdir -p ipm_test 
        
2. Change to the working directory

        $<UserName>/CODK/CODK-M/>cd ipm_test 
        
3. Next, create a new project with the same name as the example you want to run.
For Example:

        make project PROJ_DIR=a_SimplePatternMatching 
        
4. Change directory to your project directory
For Example:

        cd a_SimplePatternMatching 
        
5. Now you need to source the environment settings. Remember to do this for every new terminal instance.

        $<UserName>/CODK/CODK-M/ipm_test/a_SimplePatternMatching/>source env.sh 
        
6. Copy the example sketch file ending in .ino from the example directory into your project directory.
For Example: (Do not forget the trailing period)

        cp $(ARDUINOSW_DIR)/libraries/Intel-Pattern-Matching-Technology/examples/a_SimplePatternMatching/a_SimplePatternMatching.ino . 
        
7. Convert the sketch into C++ by running `make convert-sketch`
For Example:

        make convert-sketch SKETCH=a_SimplePatternMatching.ino 
        
8. Now you can  Build and Flash your sample project:

        $>make compile
        $>make upload SERIAL_PORT=/dev/ttyACM0
        
        
Follow the instructions in the README file for each example to run the sample application.

## Procedure to run examples on the Arduino IDE

All the examples in the Intel Pattern Matching Technology Library can be opened and run directly from the Arduino IDE just like any other examples from a custom Arduino Library. Using the Arduino Menu select an example sketch using the following 

        File -> Examples -> (Under the grouping "Examples from Custom Libraries") Intel_PatternMatching ->  (Select one of the example Sketches)


[Examples from Libraries](https://www.arduino.cc/en/Tutorial/LibraryExamples)
