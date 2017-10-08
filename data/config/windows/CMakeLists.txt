# CMakeLists for data/config/windows

list(APPEND files "style.css")

if(WIN32)
    install(FILES ${files} DESTINATION "${KVIRC_BIN_PATH}")
endif()
