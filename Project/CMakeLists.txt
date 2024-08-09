# Project 目录下的 CMakeLists.txt，用于管理 Factory 文件夹中的源代码

# 添加 Factory 文件夹中的源文件
add_executable(Project 
  Factory/Factory.cpp 
  Factory/main.cpp
)

# 包含 Factory 文件夹中的头文件
target_include_directories(Project PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/Factory)

if (CMAKE_VERSION VERSION_GREATER 3.12)
  set_property(TARGET Project PROPERTY CXX_STANDARD 20)
endif
