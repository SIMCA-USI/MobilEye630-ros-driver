cmake_minimum_required(VERSION 3.5)
project(mobileye_node)

# Encontrar dependencias de ROS 2
find_package(ament_cmake REQUIRED)
find_package(rclpy REQUIRED)
find_package(std_msgs REQUIRED)
find_package(can_msgs REQUIRED)
find_package(mobileye_msgs REQUIRED)

# Instalar el script de Python
install(
  PROGRAMS
  scripts/mobileye_node.py
  DESTINATION lib/${PROJECT_NAME}
)

# Instalar archivos de lanzamiento
install(
  DIRECTORY scripts/
  DESTINATION share/${PROJECT_NAME}
)

# Exportar dependencias
ament_package()
