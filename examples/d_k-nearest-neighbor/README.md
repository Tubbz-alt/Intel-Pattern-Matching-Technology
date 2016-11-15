# Neural Network k-Nearest-Neighbor Classification Example

This example is for a simple pattern classification function implemented using the Intel Pattern Matching Technology Engine which is a hardware neural-network.

The k-Nearest-Neighbor classification, also known in short-form as k-NN, is one of the basic and simplest machine learning algorithms. It is a form of instance-based learning also called memory-based learning because a hypothesis is constructed based on trained knowledge stored in memory which is based on the instances in the training set.

Since the function is only approximated locally based on the training set and all computation or analysis is deferred until after classification, the algorithm is also termed as a lazy-learning algorithm. Classification is performed by comparing the unknown vector with it's nearest neighbors in terms of distance calculated by each committed neuron and assigning the category of the majority of the neighbors to the unknown vector.

Because of this simplicity and localization of knowledge, the algorithm can be used to simutaneously solve multiple problems and adapts very well to changes in the problem space.

It also suffers from some down-sides such as needing a large amount of memory for storing the entire training data set as well as vulnerability to noisy training data having many outliers.

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

When the sample runs and the Pattern Matching is initialized and knowledge is restored from the file created using the second example that showed how to save knowledge (b_SavingKnowledge). The program then asks for the input vector as before.

When an input is provided, the neural networks calculates the distance to the nearest neighbor for each category.


```
   Restoring Neuron: 1
   11 24 29
   Restoring Neuron: 2
   18 75 38
   Restoring Neuron: 3
   2  56 35
   Restoring Neuron: 4
   111   224   229
   Restoring Neuron: 5
   128   200   255
   Restoring Neuron: 6
   99 180   201
   Restoring Neuron: Knowledge Set Restored. 

    Now enter 3 numbers, between 0 and 255, separated by a comma. 
   Like 11, 24, 29 
```

### Output 

If you enter an Input Vector that is similar or closely matching one 
of the learned Pattern categories, then you will notice that the distance to that category is markedly smaller than that for other categories. This indicates that the pattern can be classified as part of that category until further analysis.

**For Example:**


```
   You entered: 12,25,30
   Now searching k-nearest neighbor
   Distance = 3  Category = 1
   Distance = 46  Category = 3
   Distance = 64  Category = 2
   Distance = 413  Category = 6
   Distance = 497  Category = 4
   Distance = 516  Category = 5
```

When the Input Vector is markedly different from the training set, the distances to each category is large.

**For Example:**

```
   You entered: 255,255,255
   Now searching k-nearest neighbor
   Distance = 182  Category = 5
   Distance = 201  Category = 4
   Distance = 285  Category = 6
   Distance = 634  Category = 2
   Distance = 672  Category = 3
   Distance = 701  Category = 1
```

**Note:** This Input Vector was classified as unknown and not part of the training set in our previous samples and looking at the distances from each category we can tell that this is indeed so.

**Warning:** The file NeurData.dat is created the first time you run the previous sample, b_SavingKnowledge. Hence you should run that sample before running this sample d_k-nearest-neighbor. The current sample does not check whether the NeurData.dat file exists and will remain untrained and unable to perform any pattern matching if the file is missing. No output will be generated in this case.

**For Example:**

```
   Knowledge Set Restored. 

    Now enter 3 numbers, between 0 and 255, separated by a comma. 
   Like 11, 24, 29 
   You entered: 1,2,3
   Now searching k-nearest neighbor
```
