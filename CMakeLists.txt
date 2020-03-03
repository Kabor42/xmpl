cmake_minimum_required(VERSION 2.8)

set( OpenGL_GL_PREFERENCE GLVND)

project(xmpl)
add_executable(xmpl greentriangle.cpp)
find_package(OpenGL REQUIRED)
find_package(GLEW REQUIRED)
find_package(GLUT REQUIRED)
include_directories( ${OPENGL_INCLUDE_DIRS} ${GLUT_INCLUDE_DIRS} ${GLEW_INCLUDE_DIRS})

target_link_libraries(xmpl ${OPENGL_LIBRARIES} ${GLUT_LIBRARIES} ${GLEW_LIBRARIES})
