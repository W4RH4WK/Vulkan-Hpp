# Copyright(c) 2018-2019, NVIDIA CORPORATION. All rights reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

cmake_minimum_required(VERSION 3.2)

project(06_InitDepthBuffer)

set(HEADERS
  ../utils/utils.hpp
)

set(SOURCES
  06_InitDepthBuffer.cpp
  ../utils/utils.cpp
)

source_group(headers FILES ${HEADERS})
source_group(sources FILES ${SOURCES})

add_executable(06_InitDepthBuffer
  ${HEADERS}
  ${SOURCES}
)

set_target_properties(06_InitDepthBuffer PROPERTIES FOLDER "Samples")
target_compile_definitions(06_InitDepthBuffer PUBLIC VULKAN_HPP_DISPATCH_LOADER_DYNAMIC=1)
