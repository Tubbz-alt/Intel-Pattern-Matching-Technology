# Restoring Knowledge Example

In the first example (a_SimplePatternMatching), we trained the neural-network to recognize a training set of input patterns. However, the learned knowledge was volatile and initializing the neural-network caused the neurons to forget all that was learned and they had to be retrained before use.

The second example (b_SavingKnowledge) showed how the learned knowledge could be saved into a file on the on-board flash memory so that once the neural-network was trained, it could potentially recall it's knowledge from the file without having to retrain and learn the knowledge all over again.

The current example (c_RestoringKnowledge) shows how to restore the previously learned knowledge stored on file back to the neural-network. In this example, an un-trained neural-network retrieves previously learned knowledge from file and can immediately begin performing pattern matching without needing to be retrained.

Knowledge learned by one neural-network can be transfered to another previously un-trained neural-network using this method thus eliminating the learning/training phase for subsequent neural-networks for the same task.

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

When the sample runs, it attempts to load the file NeurData.dat from the on-board flash. As before, the program asks for an input vector of Three Numbers that are comma separated and between 0 to 255. The Pattern is analyzed when a Newline character is recognized.

**Note:** Any entry that is greater than 255 will be constrained to 255

```
   Reading Neuron: 1
   1	47	2	1	11	24	29
   Reading Neuron: 2
   1	38	2	2	18	75	38
   Reading Neuron: 3
   1	38	2	3	2	56	35
   Reading Neuron: 4
   1	67	2	4	111	224	229
   Reading Neuron: 5
   1	67	2	5	128	200	255
   Reading Neuron: 6
   1	84	2	6	99	180	201
   Reading Neuron: Knowledge Set Restored. 

   Now enter 3 numbers, between 0 and 255, separated by a comma. 
   Like 11, 24, 29

 ```

### Output 

If the knowledge file exists and is properly restored, then the neural network regains it's knowledge from file and behaves as if it is trained.

If you enter an Input Vector that is similar or closely matching one 
of the learned Patterns, then it is recognized as such. 

**For Example:**

```
   You entered: 111,200,240
   The closest match to the trained data 
   is category: 4
```

If you enter an Input Vector that is not similar or that doesn't match
a learned Pattern, then the Pattern Matcher returns an appropriate
response that it does not match trained categories. 

**For Example:**

```
   You entered: 111,111,111
   Which didn't match any of the trained categories.
```

**Warning:** The file NeurData.dat is created the first time you run the previous sample, b_SavingKnowledge. Hence you should run that sample before running this sample c_RestoringKnowledge. The current sample does not check whether the NeurData.dat file exists and will remain untrained and unable to perform any pattern matching if the file is missing.

**For Example:**

```
   Knowledge Set Restored. 

    Now enter 3 numbers, between 0 and 255, separated by a comma. 
   Like 11, 24, 29 
   You entered: 11,24,29
   Which didn't match any of the trained categories.

```
