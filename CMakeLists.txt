cmake_minimum_required(VERSION 3.5)

project(project LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(${PROJECT_NAME}
    main.cpp
)
list(APPEND 3RDPARTY_DEFINATIONS
    UNIT_LIB_DISABLE_IOSTREAM
    DISABLE_PREDEFINED_UNITS
    ENABLE_PREDEFINED_DATA_UNITS
    ENABLE_PREDEFINED_ANGLE_UNITS
    ENABLE_PREDEFINED_TIME_UNITS
    ENABLE_PREDEFINED_ANGULAR_VELOCITY_UNITS
    ENABLE_PREDEFINED_FREQUECY_UNITS
    ENABLE_PREDEFINED_VOLTAGE_UNITS
    ENABLE_PREDEFINED_POWER_UNITS
    ENABLE_PREDEFINED_TEMPERATURE_UNITS
    ENABLE_PREDEFINED_CONVERT_UNITS
    ENABLE_PREDEFINED_CONCENTRATION_UNITS
    ELPP_NO_LOG_FILE
    ELPP_NO_DEFAULT_LOG_FILE
    ELPP_FORCE_USE_STD_THREAD
)

