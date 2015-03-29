SET(MainProjSrc
  ${SOLUTION_NAME}.cpp
)

set(BOOST_INCLUDEDIR "${BOOST_ROOT}")
set(BOOST_LIBRARYDIR "${BOOST_ROOT}/lib")
set(Boost_USE_STATIC_LIBS ON)

find_package(Boost 1.36.0 REQUIRED program_options)

include_directories(${BOOST_INCLUDEDIR} ${PELIB_ROOT})

add_executable (${SOLUTION_NAME} ${MainProjSrc})

target_link_libraries (${SOLUTION_NAME} pelib ${Boost_LIBRARIES})