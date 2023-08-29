set(APP converter)

add_executable(${APP})
target_sources(${APP} PRIVATE main.cpp)
target_link_libraries(${APP} PRIVATE wordconverter stdc++fs)
target_compile_features(${APP} PRIVATE cxx_std_17)

if(CMAKE_INSTALL_PREFIX_INITIALIZED_TO_DEFAULT)
    set(CMAKE_INSTALL_PREFIX "/opt/word-converter/" CACHE PATH "install prefix" FORCE)
endif(CMAKE_INSTALL_PREFIX_INITIALIZED_TO_DEFAULT)

install(TARGETS ${APP}
        DESTINATION bin
        COMPONENT ${APP})
