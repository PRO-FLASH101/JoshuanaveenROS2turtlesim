# JoshuanaveenROS2turtlesim

Goal:
- Make the W/S keys control up and down respectively
- Make the A/D keys control the degree of the turn
- Essentially like any controller

______________________________________________________________________________________________________________________________________________________
Design: 

1.  Keyboard (W/A/S/D)
2. Keyboard Node  ← tracks which keys are currently "active" (via watchdog timing)
3. MovementCommand (protobuf-generated ROS2 message)
4. Translator/bridge node  ← not yet made
5. geometry_msgs/Twist    
6. /turtle1/cmd_vel  
7. TurtleSim moves


Keyboard --> Python controller --> MovementCommand --> ROS 2 --> TurtleSim
______________________________________________________________________________________________________________________________________________________
