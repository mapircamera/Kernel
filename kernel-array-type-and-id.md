#Kernel Array Type and ID

####To provide a modular configuration each Kernel module provides two values in the captured image metadata to determine what type of an array configuration is being used, as well as where the module is in the array.

##Array ID: 

This value ranges from 0 to n-1, where n is the number of modules in the array, up to a value of 255. The Array ID tells you where the module is located in the array, with 0 being the master camera on the master link board and iterating up from there.

##Array Type:

This value ranges from 0 to 255 and tells you which type of array is being used. See the below table for more information.

##Array Orientation

This corresponds to how the top row of sensor pixels are orientated within the array. It also relates to any rotation to the images our software does during processing.


| Array Type Value &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Common Name | Rotation Orientation| Array ID 0 | Array ID 1 | Array ID 2 |Array ID 3 |Array ID 4 |Array ID 5 |
|-------------------|-------------------------|----------------|--------------------|--------------------|--------------|--------------------|--------------|--------------|
| ArrayType 0d| 1 Kernel| A | Yaw: 0, Pitch: 0, Roll: 0         |   |  |  |  |  |
| ArrayType 1| 1 Kernel| B | Yaw: 90, Pitch: (-Roll)  Roll: (Pitch)         |   |  |  |  |  |
| ArrayType 2| 1 Kernel| C | Yaw: 180, Pitch: (-Pitch), Roll: (-Roll), [Rotate Image]         |   |  |  |  |  |
| ArrayType 3| 1 Kernel| D | Yaw: 270, Pitch: (Roll), Roll: (-Pitch) |   |  |  |  |  |


