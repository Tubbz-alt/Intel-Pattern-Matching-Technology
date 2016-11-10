# Saving Knowledge Example

In the previous example, we trained the neural-network to recognize a training set of input patterns. This knowledge is volatile in that initializing the neural-network will cause the neurons to forget all that was learned.

The current example shows how the learned knowledge can be saved into a file on the on-board flash memory so that once the neural-network is trained, it can recall it's knowledge from the file without having to retrain and learn the knowledge all over again. This is useful when training sets are large or when you want to replicate the knowledge to multiple neural-networks.

## Hardware Requirements

   No additional hardware needed.
   
### Hardware Connections
   
   Connect the USB cable between the host machine and the Arduino/Genuino 101
   USB port or the tinyTile USB port

[Serial Terminal Emulator Settings](../SerialSettings.md)

## Software Dependencies
  * Intel-Pattern-Matching Library
  * Serial Flash Library
  * SPI Library

## Running the Sample
When the sample runs and the Pattern Matching is initialized, training begins using the built in training set that trains the Pattern Matcher to recogrnize Six Categories of Patterns.

Once this is complete, the program writes the data to a file on the flash and, as before, the program asks for an input vector of Three Numbers that are comma separated and between 0 to 255. The Pattern is analyzed when a Newline character is recognized.

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
   File Size to save is = 17408
   Creating file NeurData.dat
   Saving Neuron: 1
   Saving Neuron: 2
   Saving Neuron: 3
   Saving Neuron: 4
   Saving Neuron: 5
   Saving Neuron: 6
   Knowledge Set Saved. 

   Now enter 3 numbers, between 0 and 255, separated by a comma. 
   Like 11, 24, 29 
```

**Note:** The file NeurData.dat is created the first time this sample is run. Thereafter, the program checks if the file exists and erases it before writing the fresh training data to the file.

As such, the line "Creating file NeurData.dat" is replaced with the line "File NeurData.dat already exists".

### Output 

If you enter an Input Vector that is similar or closely matching one 
of the learned Patterns, then it is recognized as such. 

**For Example:**

```
   You entered: 18,76,40
   The closest match to the trained data 
   is category: 2
```

If you enter an Input Vector that is not similar or that doesn't match
a learned Pattern, then the Pattern Matcher returns an appropriate
response that it does not match trained categories. 

**For Example:**

```
   You entered: 0,0,0
   Which didn't match any of the trained categories.
```
