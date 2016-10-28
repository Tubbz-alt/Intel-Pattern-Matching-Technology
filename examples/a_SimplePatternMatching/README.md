# Neural Network Simple Pattern Matching Example

This example is for a simple pattern matching function implemented using the 
Intel Pattern Matching Technology Engine which is a hardware neural-network.



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
When the sample runs and the Pattern Matching is initialized, training begins 
using the built in training set that trains the Pattern Matcher to recogrnize 
Six Categories of Patterns.

Once this is complete, the terminal asks for an input vector of Three Numbers
that are comma separated and between 0 to 255. The Pattern is analyzed when
a Newline character is recognized.

**Note:** Any entry that is greater than 255 will be constrained to 255

```
   Neurons committed before learning = 0
   Category 1 trained with: 11, 24, 29
 
   Category 2 trained with: 18, 75, 38
 
   Category 3 trained with: 2, 56, 35
 
   Category 4 trained with: 111, 224, 229
 
   Category 5 trained with: 128, 200, 255
 
   Category 6 trained with: 99, 180, 201
 
   Neurons committed after learning = 6
   Now enter 3 numbers, between 0 and 255, separated by a comma. 
   Like 11, 24, 29 
```

### Output 

If you enter an Input Vector that is similar or closely matching one 
of the learned Patterns, then it is recognized as such. For Example:

```
   You entered: 10,25,30
   The closest match to the trained data 
   is category: 1
```







