cmake_minimum_required(VERSION 3.5)
project(mobileye_msgs)

# Encontrar dependencias de ROS 2
find_package(ament_cmake REQUIRED)
find_package(std_msgs REQUIRED)

# Generar mensajes
find_package(rosidl_default_generators REQUIRED)
rosidl_generate_interfaces(${PROJECT_NAME}
  "msg/LKAlane.msg"
  "msg/ReferencePoints.msg"
  "msg/LKA.msg"
  "msg/Lane.msg"
  "msg/ObstacleStatus.msg"
  "msg/ObstacleData.msg"
  "msg/CarInfo.msg"
  "msg/Gyro.msg"
  "msg/SystemWarnings.msg"
  "msg/TSR.msg"
  "msg/TSRVisionOnlySign.msg"
  "msg/ExtLogData.msg"
  "msg/SmartADAS.msg"
  "msg/SeeQ.msg"
  "msg/StandardCAN.msg"
  "msg/MobileyeInfo.msg"
  DEPENDENCIES std_msgs
)

# Exportar dependencias
ament_export_dependencies(rosidl_default_runtime)
ament_package()
