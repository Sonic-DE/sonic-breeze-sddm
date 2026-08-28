configure_file(theme.conf.cmake ${CMAKE_CURRENT_BINARY_DIR}/theme.conf)

# Install the login theme into the SDDM themes directory. The components entry
# is a development-tree symlink to the shared org.kde.breeze.components QML
# module and is deliberately not installed with the theme.
install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/
        DESTINATION ${KDE_INSTALL_FULL_DATADIR}/sddm/themes/breeze
        PATTERN "README.txt" EXCLUDE
        PATTERN "CMakeLists.txt" EXCLUDE
        PATTERN "Messages.sh" EXCLUDE
        PATTERN "components" EXCLUDE
        PATTERN "dummydata" EXCLUDE
        PATTERN "theme.conf.cmake" EXCLUDE
)

install(FILES ${CMAKE_CURRENT_BINARY_DIR}/theme.conf
        DESTINATION ${KDE_INSTALL_FULL_DATADIR}/sddm/themes/breeze
)
