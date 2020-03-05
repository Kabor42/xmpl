cmake_minimum_required(VERSION 3.15)

set( OpenGL_GL_PREFERENCE GLVND)

project(SkeletonTest)
add_executable(SkeletonTest framework.cpp Skeleton.cpp)
find_package(OpenGL REQUIRED)
find_package(GLEW REQUIRED)
find_package(GLUT REQUIRED)
include_directories( ${OPENGL_INCLUDE_DIRS} ${GLUT_INCLUDE_DIRS} ${GLEW_INCLUDE_DIRS})

target_link_libraries(SkeletonTest ${OPENGL_LIBRARIES} ${GLUT_LIBRARIES} ${GLEW_LIBRARIES})
