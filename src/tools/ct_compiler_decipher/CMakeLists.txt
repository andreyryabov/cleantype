add_executable(ct_compiler_decipher ct_compiler_decipher.cpp)
clean_type_set_target_option(ct_compiler_decipher)
install(TARGETS ct_compiler_decipher DESTINATION ${CMAKE_INSTALL_PREFIX}/bin)

if (NOT MSVC) # ct_compiler_decipher_example contains intentional bugs for demo purposes, but msvc considers them as build failure
    add_executable(ct_compiler_decipher_example EXCLUDE_FROM_ALL example/ct_compiler_decipher_example.cpp)
    clean_type_set_target_option(ct_compiler_decipher_example)
endif()
