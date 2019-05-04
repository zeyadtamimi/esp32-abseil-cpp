# ESP32 Abseil C++ library ESP32 component

Since the Abseil C++ library's make file structure does not play well with the ESP32 and also
requires the presence of the `pthread` library, I have added a simple CMake file to compile only the
abseil parts that are:
    A) Needed by other subprojects
    B) Are compatible with the ESP32 (i.e. dont need a threading library)

If you need other modules it should be as simple as adding the source files to the `CMakeLists.txt`
file. If it does work, feel free to push it upstream.

## Setup
Simply add the repository to your ESP IDF Project's component directory:
```bash
    mkdir -p components && git submodule add <url> components/abseil_cpp_port &&
    git submodule update --init --recursive
```

## Usage
Should be the exact same as the usage of the normal Abseil C++ library.

# License
This is licensed under the MIT license.
