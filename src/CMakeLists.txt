cmake_minimum_required(VERSION 3.9)
set(CMAKE_CXX_STANDARD 11)

find_package(Vulkan REQUIRED)
# find_package(glfw3 REQUIRED)
# find_package(glm REQUIRED)

include_directories(${Vulkan_INCLUDE_DIR})
add_executable(${PROJECT_NAME}
        main.cpp
        # VulkanEngine.cpp
        # VulkanEngine.h
      )
target_link_libraries(${PROJECT_NAME} Vulkan::Vulkan)
# thanks to
# https://www.reddit.com/r/vulkan/comments/5873ic/psa_as_of_version_37_cmake_supports_vulkan_out_of/
