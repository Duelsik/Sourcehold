add_library(Audio 
  Audio.cpp
  Effect.cpp
  Song.cpp
)

# TODO(seidl):
# change headers to correct paths
target_include_directories(Audio 
  PRIVATE ../
  PUBLIC ../FFMPEG
)

target_link_libraries(Audio 
  PRIVATE ProjectOptions
  PRIVATE System
  PUBLIC FFmpegUtil
  PUBLIC OpenAL::OpenAL
  PRIVATE SWRESAMPLE::SWRESAMPLE
  PRIVATE SDL2::SDL2
)
