file (GLOB_RECURSE SOURCES *.cpp)
file (GLOB_RECURSE HEADERS *.hpp)

add_executable (ApplicationLogicTestRunner ${HEADERS} ${SOURCES})
sober_naming_variant_target (ApplicationLogic Test TEST_LOGIC_TARGET)
target_link_libraries (ApplicationLogicTestRunner PRIVATE "${TEST_LOGIC_TARGET}")
add_test (NAME "TestApplicationLogic" COMMAND ApplicationLogicTestRunner)