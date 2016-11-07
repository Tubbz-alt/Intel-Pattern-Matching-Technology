#How to Run the Examples

This procedure assumes that the user has already installed the Intel Pattern Matching Library
as described in the library README.

## Procedure to run examples on CODK-M

All of the examples are available at the following path:

        $(ARDUINOSW_DIR)/libraries/Intel-Pattern-Matching-Technology/examples 

1. In the CODK-M directory, create a new project with the same name as the example you want to run.
For Example:

        make project PROJ_DIR=a_SimplePatternMatching ARC_PROJ=arc/corelibs/libraries/Intel-Pattern-Matching-Technology/examples/a_SimplePatternMatching
        
2. Change directory to your project directory
For Example:

        cd a_SimplePatternMatching 
        
3. Now you need to source the environment settings. Remember to do this for every new terminal instance.

        $<UserName>/CODK/CODK-M/a_SimplePatternMatching/>source env.sh 
        
4. Copy the example sketch file ending in .ino from the example directory into your project directory.
For Example: (Do not forget the trailing period)

    cp ../arc/corelibs/libraries/Intel-Pattern-Matching-Technology/examples/a_SimplePatternMatching/a_SimplePatternMatching.ino . 
        
7. Convert the sketch into C++ by running `make convert-sketch`
For Example:

        make convert-sketch SKETCH=a_SimplePatternMatching.ino 
        
8. Now you can  Build and Flash your sample project:

        $>make compile
        $>make upload SERIAL_PORT=/dev/ttyACM0
        
        
Follow the instructions in the README file for each example to run the sample application.


