configure_file(config.h config.h.in)

list(APPEND APP_COMPILE_DEFINATIONS
    ${3RDPARTY_DEFINATIONS} ELPP_THREAD_SAFE
)

list(APPEND COMMON_SRC 
  ${CMAKE_CURRENT_SOURCE_DIR}/common/fileutils.cpp
  ${CMAKE_CURRENT_SOURCE_DIR}/common/stringutils.cpp
  ${CMAKE_CURRENT_SOURCE_DIR}/common/cryptolayer.cpp
)

list(APPEND CORE_SRC 
        core/filecache.cpp
        core/profileiconcache.cpp
        core/commandqueue.cpp
        core/sysmodel.cpp
        core/sysexplorer.cpp
        core/sysmodelfactory.cpp
        core/sysmodelsyncer.cpp
        core/session.cpp
        core/profileview.cpp
        core/profilepartview.cpp
        core/profileviewfactory.cpp
        core/profilestorage.cpp
        core/profilexmlparserfactory.cpp
)
list( APPEND INFO_SRC 
    core/info/infoproviderregistry.cpp
    core/info/common/cpuinfolscpu.cpp
)

list(APPEND CONTROLS_SRC
  core/components/controls/noop.cpp
)

list(APPEND SENSORS_SRC 
    core/components/sensors/graphitemprofilepart.cpp
)

list(APPEND UI_COMPONENTS_SRC
  core/uifactory.cpp
)

list(APPEND APP_SRC 
  app/app.cpp
)

list(APPEND TRANSLATABLE_FILES
  ${UI_COMPONENTS_SRC}
   app/systray.cpp
   qml/main.qml
)

list(APPEND TRANSLATIONS 
  translations/lang_en_EN.ts
)

set_source_files_properties(${TRANSLATIONS} PROPERTIES 
  OUTPUT_LOCATION ${CMAKE_CURRENT_SOURCE_DIR}/translations
)

option(UPDATE_TRANSLATIONS "")




