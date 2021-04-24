sober_test_begin (Persistence)
    file (GLOB_RECURSE SOURCES *.cpp)
    file (GLOB_RECURSE HEADERS *.hpp)
    list (APPEND SOURCES ${HEADERS})

    sober_library_set_sources ("${SOURCES}")
    sober_library_include_directory (PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}")

    sober_test_variant_begin (Binary)
    sober_test_variant_end ()

    sober_test_variant_begin (PlainText)
    sober_test_variant_end ()

    sober_test_variant_begin (TestStub)
    sober_test_variant_end ()
sober_test_end ()