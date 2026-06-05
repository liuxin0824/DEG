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

### handle-press (5 videos)
A video clip of the handle-press task: A red robotic arm is positioned on a table, along with a device featuring a red handle (the device position is randomly initialized and then fixed). The robotic arm lifts up, moves above the handle, then descends and uses its gripper to press the handle downward onto the table. 

Keep the table static and the device position unchanged throughout. Preserve detailed ground shadows. Ensure that the motion of the robotic arm follows logical physics, and maintain consistent colors and shapes of the objects and scene from start to finish. Note that the handle does not move until the robotic arm makes contact with it.

### button-press (3 videos)
A video clip of the button-press task: A red robotic arm is positioned on a table, along with a box featuring a red button. The robotic arm moves toward the box, accurately aligns with the red button, and presses it down. 

Keep the table static and the box position unchanged throughout. Preserve detailed ground shadows. Ensure that the motion of the robotic arm follows logical physics, and maintain consistent colors and shapes of the objects and scene from start to finish.

### coffee-button (5 videos)
A video clip of the coffee-button task: A red robotic arm is positioned on a table, along with a coffee machine with a button (machine position randomly initialized and then fixed), and a coffee mug. The robotic arm reasonably adjusts its orientation until aligned with the coffee machine, then moves toward the button and presses it. 

Keep the table static and the coffee machine position unchanged throughout. Preserve detailed ground shadows. Ensure that the motion of the robotic arm follows logical physics, and maintain consistent colors and shapes of the objects and scene from start to finish. Note that the button does not move until the robotic arm makes contact with it.

### drawer-open (3 videos)
A video clip of the drawer-open task: A red robotic arm is positioned on a table, along with a closed green drawer featuring a white handle. The robotic arm lifts up and moves above the white handle, then descends and uses its gripper to precisely hook the handle (with the blue inner jaw positioned inside and the white outer jaw positioned outside), and pulls the drawer open. 

Keep the table static. Preserve detailed ground shadows. Ensure that the motion of the robotic arm and the target object follows logical physics, and maintain consistent colors and shapes of the objects and scene from start to finish. Note that the drawer does not move until the robotic arm makes contact with it or its handle.

### button-press-wall (3 videos)
A video clip of the button-press-wall task: A red robotic arm is positioned on a table, along with a box featuring a red button and a fixed wall. The robotic arm lifts up and closes its gripper, moves toward the box and passes over the wall, then descends to align the outer side of its gripper precisely with the red button, opens the gripper, and presses the button down. 

Keep the table static and the box position unchanged throughout. Preserve detailed ground shadows. Ensure that the motion of the robotic arm follows logical physics, and maintain consistent colors and shapes of the objects and scene from start to finish. Note that the red button does not move until the robotic arm makes contact with it, and the robotic arm cannot pass directly through the wall.

### drawer-close (3 videos)
A video clip of the drawer-close task: A red robotic arm is positioned on a table, along with an open green drawer featuring a white handle. The robotic arm first lifts upward, then descends and uses its gripper to precisely press against the white handle from the outside, pushing the green drawer closed. 

Keep the table static. Preserve detailed ground shadows. Ensure that the motion of the robotic arm and the target object follows logical physics, and maintain consistent colors and shapes of the objects and scene from start to finish. Note that the drawer does not move until the robotic arm makes contact with it or its handle.

### plate-slide (3 videos)
A video clip of the plate-slide task: A red robotic arm is positioned on a table, alongside a black plate initialized at a random position, and a soccer goal. The robotic arm moves downward, accurately presses on the plate, and slides it into the goal toward a red target point. 

Keep the table and goal static with unchanged positions. Preserve detailed shadows on the ground. Ensure the motion of the robotic arm is logical and that the colors and shapes of the objects and scene remain consistent. Note that the plate does not move until the robotic arm makes contact with it.

### button-press-topdown (3 videos)
A video clip of the button-press-topdown task: A red robotic arm is positioned on a table, along with a box featuring a red button on its top surface. The robotic arm lifts upward, then moves over the box, aligns with the red button, and descends to press it down precisely. 

Keep the table static and the box position unchanged throughout. Preserve detailed ground shadows. Ensure that the motion of the robotic arm follows logical physics, and maintain consistent colors and shapes of the objects and scene from start to finish. Note that the red button does not move until the robotic arm makes contact with it.

### hammer (3 videos)








