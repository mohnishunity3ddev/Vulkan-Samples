# Copyright (c) 2019-2024, Sascha Willems
#
# SPDX-License-Identifier: Apache-2.0
#
# Licensed under the Apache License, Version 2.0 the "License";
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
#

get_filename_component(FOLDER_NAME ${CMAKE_CURRENT_LIST_DIR} NAME)
get_filename_component(PARENT_DIR ${CMAKE_CURRENT_LIST_DIR} PATH)
get_filename_component(CATEGORY_NAME ${PARENT_DIR} NAME)

add_sample_with_tags(
    ID ${FOLDER_NAME}
    CATEGORY ${CATEGORY_NAME}
    AUTHOR "Sascha Willems"
    NAME "Conservative rasterization"
    DESCRIPTION "Uses an offscreen buffer with lower resolution to demonstrate the effect of conservative rasterization (VK_EXT_conservative_rasterization)"
    SHADER_FILES_GLSL
        "conservative_rasterization/glsl/fullscreen.vert"
        "conservative_rasterization/glsl/fullscreen.frag"        
        "conservative_rasterization/glsl/triangle.vert"
        "conservative_rasterization/glsl/triangle.frag"
        "conservative_rasterization/glsl/triangleoverlay.frag"
    SHADER_FILES_HLSL
        "conservative_rasterization/hlsl/fullscreen.vert.hlsl"
        "conservative_rasterization/hlsl/fullscreen.frag.hlsl"        
        "conservative_rasterization/hlsl/triangle.vert.hlsl"
        "conservative_rasterization/hlsl/triangle.frag.hlsl"
        "conservative_rasterization/hlsl/triangleoverlay.frag.hlsl")
