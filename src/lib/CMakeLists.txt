set(LIB_NAME wordconverter)

add_library(${LIB_NAME})
target_sources(${LIB_NAME} PRIVATE WordConverter.cpp WordConverter.h)

# All the directories following PUBLIC will be used for the current target and the other targets that have dependencies on the current target.
target_include_directories(${LIB_NAME} PUBLIC .)
