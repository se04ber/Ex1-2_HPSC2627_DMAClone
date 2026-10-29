find_package(Boost COMPONENTS unit_test_framework REQUIRED)

include(CTest)
enable_testing()

add_executable(test_vector test_vec.cpp)
target_link_libraries(test_vector PRIVATE Boost::unit_test_framework MDlib)
add_test (NAME TestVector COMMAND test_vector)

#add_executable(test_particle test_particle.cpp)
#target_link_libraries(test_particle PRIVATE Boost::unit_test_framework MDlib)
#add_test (NAME TestParticle COMMAND test_particle)

