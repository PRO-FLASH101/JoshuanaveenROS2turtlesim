cmake_minimum_required(VERSION 3.8)
project(turtle_controller)

find_package(ament_cmake REQUIRED)
find_package(proto2ros REQUIRED)

proto2ros_generate(turtle_commands
  PACKAGE_NAME turtle_controller
  PROTOS
    ${CMAKE_CURRENT_SOURCE_DIR}/proto/movement.proto
)

ament_package()
