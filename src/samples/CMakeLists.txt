project(SolarEngine-Samples)

include_directories("${SolarEngine_SOURCE_DIR}/src")

file(GLOB_RECURSE DIRS RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} CMakeLists.txt)
list(SORT DIRS)
foreach (DIR ${DIRS})
    get_filename_component (DIR ${DIR} PATH)
    if (DIR)
        add_subdirectory(${DIR})
    endif ()
endforeach ()