add_subdirectory(can)
add_executable(subsystem subsystem.cpp drive_controller.hpp drive_controller.cpp)

find_package(Boost COMPONENTS system REQUIRED)
target_include_directories(subsystem PUBLIC ${Boost_INCLUDE_DIR} rover_can rover_system_messages)
target_link_libraries(subsystem PUBLIC network rover_can rover_system_messages Boost::system)

target_compile_features(subsystem PRIVATE cxx_std_17)