find_package(MPI REQUIRED)

add_library(MDlib SHARED)

target_sources(MDlib PUBLIC vector3d.cpp)
# target_link_libraries(MDlib PUBLIC MPI::MPI_CXX)
target_compile_options(MDlib PUBLIC -Werror -O3 -march=native -fopenmp)
target_link_options(MDlib PUBLIC -fopenmp)
# target_compile_definitions(MDlib PUBLIC -DNDEBUG)
