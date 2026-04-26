# Project README

## Overview
This project demonstrates polymorphism using pointer and header files in C. It includes a simple GUI application that allows users to manipulate elements through different interfaces.

## Features
- Polymorphism implemented using pointers to structures and function pointers.
- Support for basic window operations (display, render text).
- Cross-platform build with Makefiles for Linux, Windows, Wine, and WebAssembly.

## Project Structure
```
Gui_Polymorphism_PointerHeader/
├── build/                  # .exe files produced by Main.c
├── src/
│   ├── Main.c              # Entry point
│   ├── Shape.h             # Header file for the Shape interface
│   ├── Shape.c             # Implementation of the Shape interface
│   ├── Rectangle.h         # Header file for the Rectangle implementation
│   ├── Rectangle.c         # Implementation of the Rectangle class
│   ├── Circle.h            # Header file for the Circle implementation
│   ├── Circle.c            # Implementation of the Circle class
├── Makefile.linux          # Linux Build configuration
├── Makefile.windows        # Windows Build configuration
├── Makefile.wine           # Wine Build configuration
├── Makefile.web            # Emscripten Build configuration
└── README.md               # This file
```

### Prerequisites
- C/C++ Compiler and Debugger (GCC)
- Make utility

## Build & Run
To build the project for Linux:
```sh
cd Gui_Polymorphism_PointerHeader/
make -f Makefile.linux all
./build/Main
```

To build the project for Windows:
```sh
cd Gui_Polymorphism_PointerHeader/
make -f Makefile.windows all
build\Main.exe
```

To build the project for Wine (Linux cross compile for Windows):
```sh
cd Gui_Polymorphism_PointerHeader/
make -f Makefile.wine all
wine build\Main.exe
```

To build the project for WebAssembly:
```sh
cd Gui_Polymorphism_PointerHeader/
make -f Makefile.web all
emrun --no_browser --port 8080 build/index.html
```

These commands will handle building and running the application on different platforms.