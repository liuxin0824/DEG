# Dual-Granularity Contrastive Reward via Generated Episodic Guidance for Efficient Embodied RL

## Code
Implementation will be released after acceptance.

## Video Foundation Model Finetuning Details: Framework, Data, and Prompts.
In DEG, we employ LoRA to finetune Wan2.1-I2V-14B as our RL guide. We use DiffSynth-Studio (https://github.com/modelscope/DiffSynth-Studio) as our finetuning framework, following its default settings on Wan2.1-I2V-14B. The number of videos and task prompts employed in each task is provided here. 

### real-world: pick banana (3 videos)
A video clip of the robotic arm successfully grasping and placing a banana into a plate. On a table, there are a plate, a banana initialized at a random position, and a robotic arm equipped with a gripper. The robotic arm moves horizontally above the banana, then opens its gripper, descends to precisely grasp the banana with the gripper, lifts it, moves horizontally above the plate, opens the gripper, and places the banana into the plate.

### real-world: stack cube (3 videos)
A video clip of the robotic arm stacking a cube. On a table, there are a plate, a red cube initialized at a random position, and a wooden block. The robotic arm moves horizontally above the red cube, then opens its gripper, descends to precisely grasp the red cube with the gripper, lifts it, moves horizontally above the wooden block, opens the gripper, and places the red cube onto the wooden block.


### door-close (3 videos)
A video clip of the door-close task: A red robotic arm is positioned on a table, along with a dark cabinet whose door is initially open (with its position randomly initialized and then fixed), and a light green target marker. The robotic arm moves toward the cabinet door, presses against it from the outside, and closes it. 

Keep the table static and the cabinet position unchanged throughout. Preserve detailed shadows on the ground. Ensure that the motion of the robotic arm and the cabinet door follows logical physics. Maintain consistent colors and appearance of objects and the scene from start to finish. After initialization, the cabinet door exhibits a slight automatic rebound, then remains stationary until contacted by the robotic arm.

### window-close (3 videos)
A video clip of the window-close task: A red robotic arm is positioned on a table alongside an open window. The robotic arm moves toward the window, presses against its white handle from the left side, and slides it to the right to close the window. 

Keep the table static and the window position unchanged throughout. Preserve detailed ground shadows. Ensure that the motion of the robotic arm and the window follows logical physics. Maintain consistent colors and appearance of the scene and objects from start to finish.

