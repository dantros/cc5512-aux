add_subdirectory(libs/json)

add_executable(hello_json hello_json.cpp)
target_link_libraries(hello_json PRIVATE nlohmann_json::nlohmann_json)

add_executable(json_set json_set.cpp)
target_link_libraries(json_set PRIVATE nlohmann_json::nlohmann_json)

add_executable(serialization serialization.cpp)
target_link_libraries(serialization PRIVATE nlohmann_json::nlohmann_json)

add_executable(game_object game_object.cpp)
target_link_libraries(game_object PRIVATE nlohmann_json::nlohmann_json)

add_custom_target(aux3)
add_dependencies(aux3 hello_json json_set serialization game_object)
