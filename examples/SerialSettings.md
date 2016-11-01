# Serial Terminal Emulator

The included examples interact with the user via a serial terminal. 
On Ubuntu, a serial terminal emulator such as CuteCOM or Putty or Screen 
needs to be installed before running the example. 
On the Arduino IDE, the Built-in Serial Monitor can be used.

## Serial Terminal Settings

   **Device      :** /dev/ttyACM0
   
   **Speed       :** 9600
   
   **Data Bits   :** 1
   
   **Stop Bits   :** 1
   
   **Parity      :** None
   
   **Flow Control:** None

**Note:** Ensure that you turn on Both Newline and Carriage Return 
in the emulation settings as the samples require the Newline character
in order to recognize an Input Pattern.
