# LearnOpenGL

A small C++ project created while working through the [LearnOpenGL](https://learnopengl.com/) tutorials.

This is primarily a learning project for experimenting with C++, OpenGL, GLFW, and GLAD.

## Requirements

* C++11-compatible compiler
* CMake 3.10 or newer
* GLFW 3
* OpenGL
* A working OpenGL graphics driver

GLAD is included in the repository, so it does not need to be installed separately.

## Building

The project uses CMake, so the general build process is:

```bash
cmake -S . -B build
cmake --build build
```

The resulting executable will be located at:

```text
build/LearnOpenGL
```

### Ubuntu / Debian

Install the required development packages:

```bash
sudo apt update
sudo apt install build-essential cmake libgl-dev libglfw3-dev
```

Then build:

```bash
cmake -S . -B build
cmake --build build
```

Run:

```bash
./build/LearnOpenGL
```

### Fedora

Install the required development packages:

```bash
sudo dnf install gcc-c++ cmake glfw-devel mesa-libGL-devel
```

Then build:

```bash
cmake -S . -B build
cmake --build build
```

Run:

```bash
./build/LearnOpenGL
```

### Arch Linux

Install the required packages:

```bash
sudo pacman -S base-devel cmake glfw mesa
```

Then build:

```bash
cmake -S . -B build
cmake --build build
```

Run:

```bash
./build/LearnOpenGL
```

### Windows

Install:

* [CMake](https://cmake.org/download/)
* A C++ compiler, such as Visual Studio or MinGW
* GLFW

With a CMake-compatible compiler available, configure and build the project:

```powershell
cmake -S . -B build
cmake --build build
```

The executable will be located in the generated build directory. The exact location depends on the CMake generator being used.

### macOS

Install the Xcode Command Line Tools if they are not already installed:

```bash
xcode-select --install
```

Install CMake and GLFW using Homebrew:

```bash
brew install cmake glfw
```

Then build:

```bash
cmake -S . -B build
cmake --build build
```

Run:

```bash
./build/LearnOpenGL
```

## Project Structure

```text
.
├── include/          # GLAD and KHR headers
├── src/
│   ├── glad.c        # GLAD-generated OpenGL loader
│   ├── main.cpp      # Application source
│   ├── vertex.shader
│   └── fragment.shader
├── CMakeLists.txt
└── README.md
```

## Notes

This project is a work-in-progress learning project and is not intended to be a complete OpenGL application.

The GLAD source and headers in this repository were generated using the GLAD generator.

