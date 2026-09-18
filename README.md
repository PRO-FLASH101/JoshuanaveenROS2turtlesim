# JoshuanaveenROS2turtlesim

Goal:
- Make the W/S keys control up and down respectively
- Make the A/D keys control the degree of the turn
- Essentially like any controller

______________________________________________________________________________________________________________________________________________________
Design: 

Keyboard (W/A/S/D)
      │
      ▼
Keyboard Node  ← tracks which keys are currently "active" (via watchdog timing)
      │
      ▼
MovementCommand (protobuf-generated ROS2 message)
      │
      ▼
Translator/bridge node  ← not yet made
      │
      ▼
geometry_msgs/Twist  →  /turtle1/cmd_vel  →  TurtleSim moves

______________________________________________________________________________________________________________________________________________________
