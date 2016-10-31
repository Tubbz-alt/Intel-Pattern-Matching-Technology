# Neural Network k-Nearest-Neighbor Classification Example

This example is for a simple pattern classification function implemented using the Intel Pattern Matching Technology Engine which is a hardware neural-network.

The k-Nearest-Neighbor classification, also known in short-form as k-NN, is one of the basic and simplest machine learning algorithms. It is a form of instance-based learning also called memory-based learning because a hypothesis is constructed based on trained knowledge stored in memory which is based on the instances in the training set.

Since the function is only approximated locally based on the training set and all computation or analysis is deferred until after classification, the algorithm is also termed as a lazy-learning algorithm. 

Because of this simplicity and localization of knowledge, the algorithm can be used to simutaneously solve multiple problems and adapts very well to changes in the problem space.

It also suffers from some down-sides such as needing a large amount of memory for storing the entire training data set as well as vulnerability to noisy training data having many outliers.

## Hardware Requirements

   Arduino/Genuino 101 or Farnell tinyTile board based on Intel Curie Compute Module.
   
   Appropriate USB Cable for Curie based board.

   No additonal hardware is needed for this example.

### Hardware Connections
   
   Connect the USB cable between the host machine and the Arduino/Genuino 101
   USB port or the tinyTile USB port

## Serial Terminal Emulator

This example interacts with the user via a serial terminal. 
On Ubuntu, a serial terminal emulator such as CuteCOM or Putty or Screen needs to 
be installed before running the example. 
On the Arduino IDE, the Built-in Serial Monitor can be used.

### Serial Terminal Settings

   **Device      :** /dev/ttyACM0
   
   **Speed       :** 9600
   
   **Data Bits   :** 1
   
   **Stop Bits   :** 1
   
   **Parity      :** None
   
   **Flow Control:** None

**Note:** Ensure that you turn on Both Newline and Carriage Return 
in the emulation settings as this sample requires the Newline character
in order to recognize an Input Pattern.

## Running the Sample
