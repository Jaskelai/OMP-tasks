# cmake_minimum_required(VERSION <specify CMake version here>)

# !!SET YOUR PROJECT NAME HERE (instead of OMP-tasks)!!
project(OMP-tasks)

set(CMAKE_CXX_STANDARD 17)
cmake_minimum_required(VERSION 3.4)

find_package(OpenMP)
if (OPENMP_FOUND)
    set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} ${OpenMP_C_FLAGS}")
    set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${OpenMP_CXX_FLAGS}")
    set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} ${OpenMP_EXE_LINKER_FLAGS}")
endif ()

# !!SET YOUR PROJECT NAME HERE (instead of OMP-tasks)!!
add_executable(OMP-tasks omp/launcher.cpp omp/task1.cpp omp/task1.h omp/task2.cpp omp/task2.h omp/task3.cpp omp/task3.h omp/task4.cpp omp/task4.h omp/task5.cpp omp/task5.h omp/task6.cpp omp/task6.h omp/task7.cpp omp/task7.h omp/task8.cpp omp/task8.h omp/task9.cpp omp/task9.h omp/task10.cpp omp/task10.h omp/task11.cpp omp/task11.h omp/task12.cpp omp/task12.h omp/task13.cpp omp/task13.h)