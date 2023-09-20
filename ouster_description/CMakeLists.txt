cmake_minimum_required(VERSION 3.5.0)
project(ouster_description)

find_package(ament_cmake REQUIRED)

install(DIRECTORY launch meshes rviz urdf worlds
        DESTINATION share/${PROJECT_NAME}
)

if (BUILD_TESTING)
  find_package(ament_lint_auto REQUIRED)
  ament_lint_auto_find_test_dependencies()
  
  # find_package(ament_cmake_gtest REQUIRED)
  # ament_add_gtest(tests/os1_gazebo.test)
endif()

ament_package()