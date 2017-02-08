# Logging

Instead of using `std::cout` command, it is a better practice to use a logger.
This file present a list of logger that you can choose. It should be kept in
such way that one can start easily to use a logger.

### Boost logger

Probably, the best solution is to use the logger available in boost library.

#### CMake configuration

You will need to add the following line to your `CMakeLists.txt`:

``` cmake
add_definitions(-DBOOST_LOG_DYN_LINK=1)
set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_CXX_FLAGS "-lboost_system")
set(CMAKE_CXX_FLAGS "-lpthread")
find_package(Boost 1.54 COMPONENTS log_setup log program_options thread
REQUIRED)
include_directories(... ${Boost_INCLUDE_DIRS} ..)
target_link_libraries(... ${Boost_LIBRARIES} ...)
```

#### Usage

Check the [tutorial](
http://www.boost.org/doc/libs/1_62_0/libs/log/doc/html/log/tutorial.html) of the
boost documentation.
