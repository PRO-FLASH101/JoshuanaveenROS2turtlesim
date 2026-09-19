cmake_minimum_required(VERSION 3.8)
project(turtle_controller)

find_package(ament_cmake REQUIRED)
find_package(proto2ros REQUIRED)
find_package(rosidl_default_generators REQUIRED)

proto2ros_generate(turtle_commands
  PACKAGE_NAME turtle_controller
  PROTOS
    ${CMAKE_CURRENT_SOURCE_DIR}/proto/movement.proto
  INTERFACES_OUT_VAR ros_messages
)

rosidl_generate_interfaces(${PROJECT_NAME}
  ${ros_messages}
  DEPENDENCIES builtin_interfaces proto2ros
)

ament_package()
