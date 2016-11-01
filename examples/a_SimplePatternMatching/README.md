# Neural Network Simple Pattern Matching Example

This example is for a simple pattern matching function implemented using the Intel Pattern Matching Technology Engine which is a hardware neural-network.

In a neural-network, unlike a programmed pattern matching algorithm, there is a learning phase when the neural-network is trained to recognize a training set of input patterns. Once this is done, the neural-network is able to recognize exactly matching or similar patterns and also identify patterns that are not part of the training set.

## Hardware Requirements

   Arduino/Genuino 101 or Farnell tinyTile board based on Intel Curie Compute Module.
   
   Appropriate USB Cable for Curie based board.

   No additonal hardware is needed for this example.

### Hardware Connections
   
   Connect the USB cable between the host machine and the Arduino/Genuino 101
   USB port or the tinyTile USB port

[Serial Terminal Emulator Settings](../blob/master/examples/SerialSettings.md)

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
of the learned Patterns, then it is recognized as such. 

**For Example:**

```
   You entered: 10,25,30
   The closest match to the trained data 
   is category: 1
```

If you enter an Input Vector that is not similar or that doesn't match
a learned Pattern, then the Pattern Matcher returns an appropriate
response that it does not match trained categories. 

**For Example:**

```
   You entered: 255,255,255
   Which didn't match any of the trained categories.
```





