INCLUDE_DIRECTORIES( ${PROJECT_SOURCE_DIR}/src )

ADD_EXECUTABLE(unit_mgs src/unit_mgs.cpp)

TARGET_LINK_LIBRARIES(unit_mgs ${OPENTISSUE_LIBS} ${Boost_UNIT_TEST_FRAMEWORK_LIBRARY} )
INSTALL(
  TARGETS unit_mgs
  RUNTIME DESTINATION  bin/units
  )

ADD_TEST( unit_mgs unit_mgs )

