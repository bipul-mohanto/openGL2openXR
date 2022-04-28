# CMakeList.txt : CMake project for openxrOptix, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.8)

project ("openxrOptix")



include_directories("C:/vcpkg/installed/x64-windows/include")
include_directories("C:/vcpkg/installed/x64-windows/include/glm")




# Add source to this project's executable.
add_executable (openxrOptix     openxrOptix.cpp 
							    openxrOptix.h
								GLSLShader.h
								GLSLShader.cpp
								shaders/simple.fs
								shaders/simple.vs
								)


target_link_libraries(openxrOptix   "C:/vcpkg/installed/x64-windows/lib/glew32.lib"
									"C:/vcpkg/installed/x64-windows/lib/OpenGL32.lib"
									"C:/vcpkg/installed/x64-windows/lib/GlU32.lib"
									"C:/vcpkg/installed/x64-windows/lib/glfw3dll.lib"
								  )



# TODO: Add tests and install targets if needed.
