add_subdirectory(base)
add_subdirectory(usd)

pxr_setup_python()
pxr_setup_plugins()

export(PACKAGE pxr)

configure_file(pxrConfig.cmake.in
  "${PROJECT_BINARY_DIR}/pxrConfig.cmake" @ONLY)
install(FILES
  "${PROJECT_BINARY_DIR}/pxrConfig.cmake"
  DESTINATION "${CMAKE_INSTALL_PREFIX}"
)

install(EXPORT pxrTargets DESTINATION "cmake")

