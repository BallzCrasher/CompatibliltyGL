# OpenGLEngine - Modern Showroom Demo

A custom-built C++ OpenGL 3D engine demonstrating advanced rendering techniques, a scene graph hierarchy, and basic physics integration. 
This project features an interactive modern showroom scene complete with glass architecture, dynamic lighting, 3D model loading (via Assimp), and interactable elements.
This project is a student assignment.

## Key Features

* **Rendering Pipeline:**
    * **Multi-Pass Rendering:** Handles opaque objects, planar shadows, and transparent objects (sorted back-to-front) for correct alpha blending.
    * **Materials System:** Custom material support for Glass, Neon, Chrome, Gold, Plastic, and Matte surfaces.
    * **Lighting:** Directional sun light and multiple point lights with attenuation (e.g., cyan tech lights, red neon glow).
    * **Fog & Atmosphere:** Distance fog calculation to blend distant geometry.

* **Physics & Interaction:**
    * **Collision Detection:** Custom AABB/OBB (Oriented Bounding Box) collision system for walls, furniture, and vehicles.
    * **Player Physics:** simple gravity implementation, jumping, and ground detection.
    * **Raycasting:** Interaction system to detect objects in front of the camera (used for opening doors).
    * **Animation:** Scripted update callbacks for rotating objects (cars) and animated doors.

* **Architecture:**
    * **Scene Graph:** Hierarchical `Container` and `GameObject` system allowing parent-child transformations.
    * **Model Loading:** Integrated `Assimp` support for loading `.gltf` assets (Cars, Furniture, Plants).

## Prerequisites

To build this project, you will need the following installed on your system:

* **C++ Compiler:** Supporting C++17 or later.
* **CMake:** Version 3.10 or higher.
* **OpenGL:** Core libraries.
* **FreeGLUT:** For window management and input handling.
* **Assimp:** The Open Asset Import Library for loading 3D models.

### Installing Dependencies (Linux/Debian)
```bash
sudo apt-get update
sudo apt-get install build-essential cmake libgl1-mesa-dev libglu1-mesa-dev freeglut3-dev libassimp-dev
```

## Building the Project

1. **Clone the repository** (if applicable) or navigate to the project root.
2. **Create a build directory:**
```bash
mkdir build
cd build
```


3. **Generate build files with CMake:**
```bash
cmake ..
```


4. **Compile:**
```bash
make
```


5. **Run:**
```bash
./OpenGLEngine
```
