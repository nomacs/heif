# Building heif for nomacs

## Build heif (Windows)

### Compile heif

- Open CMake GUI
- set this folder to `where is the source code`
- choose a build folder (e.g. `build2017-x64`)
- Hit `Configure`then `Generate`
- Open the Project
- Compile the Solution (build Release and Debug)
- You should now have a `heif_shared.dll` in $YOUR_EXIV2_BUILD_PATH$/lib/Release
- In the `CMakeUserPaths.cmake` of your [nomacs](https://github.com/nomacs/nomacs) project, add this path:

```cmake
SET(CMAKE_PREFIX_PATH ${CMAKE_PREFIX_PATH} "$HEIF_PATH$/build2017-x64/")
```
