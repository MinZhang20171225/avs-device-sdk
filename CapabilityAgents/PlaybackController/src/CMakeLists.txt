add_definitions("-DACSDK_LOG_MODULE=playbackcontroller")

add_library(PlaybackController SHARED
    "${CMAKE_CURRENT_LIST_DIR}/PlaybackController.cpp"
    "${CMAKE_CURRENT_LIST_DIR}/PlaybackMessageRequest.cpp")

target_include_directories(PlaybackController
    PUBLIC "${PlaybackController_SOURCE_DIR}/include")

target_link_libraries(PlaybackController AVSCommon ContextManager)

# install target
asdk_install()