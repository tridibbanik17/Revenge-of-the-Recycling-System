## Revenge of the Recycling System

### Authors: Tridib Banik & Benji Switzman, McMaster University, Engineering I.

_This Python program controls a Q-Arm to sort various containers differentiated by their masses, build materials and container's destination. 
_
_The Q-arm only accepts the containers of one category in a signle cycle.
__
_The Q-bot's hopper can carry a maximum of 3 containers.
__
_If the max number of containers is reached, or a different type of container is served in the table, the Q-Arm stops and the Q-bot starts moving.
__
_The program also controls the Q-bot to follow a specific yellow line detected by IR sensors mounted on the Q-bot 
_and dump the previously picked containers into one of four recycling bins differentiated by the bin colours (red, green, blue, and white). 
_
_The colour sensors mounted on the Q-bot detect the correct bin. 
__
__After dumping is completed, the Q-bot returns to the home position and a new cycle of sorting and recycling begins.
__
__An infinite number of cycles will run unless the user terminates the program. 
__
__Quanser Interactive Labs software powers the simulated virtual environment.
__
_[Watch the video on how Q-Arm transfers a container from the servo table to Q-bot's hopper.](./ServoTable_to_Hopper.mp4)
_
_[Watch the video on the deposit process of containers after the target bin color is detected by the color sensor.](./DepositContainers_to_TargetBin.mp4)
_
_[Watch the video on the Q-bot following a yellow line using Infrared sensors.](./Q-Bot_Movements_using_IR_sensors.mp4)
_
