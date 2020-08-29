cmake_minimum_required(VERSION 3.0.2)
project(erc_jetson_bringup)

find_package(catkin REQUIRED)

catkin_package()

install(DIRECTORY launch/
    DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch)

install(DIRECTORY config/
    DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/config)

catkin_install_python(PROGRAMS 
    scripts/zed2_imu_transform_broadcaster
    DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)