option(USE_KWIN_NO_SCALE "use deepin LD_PRELOAD kwin_no_scale" ON)

# 被注释掉的都是 deepin-kwin 已经内置的
install(
    FILES
    #kglobalshortcutsrc
    #kwinrc
    #deepin-kwinrulesrc
    #klaunchrc
    #kdeglobals
    DESTINATION
    "/etc/xdg"
)

install(
    FILES
    org.kde.kwin.splitmenu.display.json
    DESTINATION
    "/usr/share/dsg/configs/org.kde.kwin"
)

# deepin kwin 5.27 内置 kwin_no_scale
#if (USE_KWIN_NO_SCALE)
#    configure_file(kwin_no_scale.in kwin_no_scale)
#    install_files("/bin" FILES ${CMAKE_CURRENT_BINARY_DIR}/kwin_no_scale)
#endif()
