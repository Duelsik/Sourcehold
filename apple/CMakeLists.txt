if(TARGET_OS_MAC_OS OR TARGET_OS_IOS)
# AppleUtils
  add_library(AppleUtils Common/SHPathUtils.m)
  target_include_directories(AppleUtils
    PUBLIC ${CMAKE_SOURCE_DIR}/apple
  )
  target_link_libraries(AppleUtils
    PRIVATE "-framework Foundation"
    PRIVATE ProjectOptions
  )
endif() # TARGET_OS_MAC_OS OR TARGET_OS_IOS
