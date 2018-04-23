# CMakeLists for  data/config/linux

list(APPEND files "style.css")

if(UNIX)
	if(APPLE)
		install(FILES ${files} DESTINATION ${CMAKE_INSTALL_PREFIX}/Contents/Resources/config/)
	else()
		# Assume linux
		install(FILES ${files} DESTINATION ${CMAKE_INSTALL_PREFIX}/share/kvirc/${VERSION_BRANCH}/config/)
	endif()
endif()
