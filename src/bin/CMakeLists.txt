set(APP converter)

add_executable(${APP})
target_sources(${APP} PRIVATE main.cpp)
target_link_libraries(${APP} PRIVATE wordconverter stdc++fs)
target_compile_features(${APP} PRIVATE cxx_std_17)
