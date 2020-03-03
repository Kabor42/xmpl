cmake_minimum_required(VERSION 2.8)

set( OpenGL_GL_PREFERENCE GLVND)

project(xmpl)
add_executable(xmpl glut_try.c)
find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
include_directories( ${OPENGL_INCLUDE_DIRS} ${GLUT_INCLUDE_DIRS} )

target_link_libraries(xmpl ${OPENGL_LIBRARIES} ${GLUT_LIBRARIES} )
