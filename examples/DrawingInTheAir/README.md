# Neural Network with Accelerometer Input Example
This sample is an application example for Intel Pattern Matching Technology. The sample sketch uses the built-in Accelerometer sensor inside the Curie module to detect motion. This data is used as an input to the PME to learn, recognize and classify the writing of alphabets in the air using the board as a stylus.

The Curie PME is initially trained using 4 training data sets for each letter of the first 6 alphabets A through F. To start and stop data aquisition in both the learning and recognition phases, a push-button is used.


## Hardware Requirements

#### Using Breadboard
   * Breadboard - 1 No.
   * SPST Pushbutton (Normally Off) - 1 No.
   * Resistor 10 kOhm, 0.25 Watt - 1 No.
   * Connecting wire - Assorted colors and lengths - As required

**OR**

#### Using Grove Starter Kit Plus - Intel Edition
   * 1 x Grove Base Shield V2
   * 1 x Grove- Button
   
### Hardware Connections
   
   Connect the USB cable between the host machine and the Arduino/Genuino 101
   USB port or the tinyTile USB port
   
   Connect 

[Serial Terminal Emulator Settings](../SerialSettings.md)

## Software Dependencies
  * Intel-Pattern-Matching Library
  * CurieIMU

## Running the Sample

1. Start the Serial Console
2. When prompted, hold down the button and use the Curie Board to draw an alphabet in the air and release the button.
3. Repeat three more times as prompted.
4. Repeat Steps 2 and 3 for all the alphabets from A through F.
5. Once this step is completed, hold down the button and draw an alphabet in the air. The Curie PME should be able to classify this action into one of the 6 alphabet categories.

**Note:** For best results, draw big letters, at least 1-2 feet tall.




### Output 
TBD


**For Example:**
TBD
