# CMake file for compiling the static library.
#
# To use this, simply add this project as a Git submodule and use:
# add_subdirectory(restclient-cpp) in your make CMakeLists.txt file and link
# against the 'restclient-cpp' library.

# Add sources as a 'restclient-cpp' library.
add_library (restclient-cpp
  include/restclient.h
  source/restclient.cpp
)
