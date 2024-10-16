# Cube Room

The Cube Room project is part of the project interactive [digital museum](https://github.com/mboudr35/glgine/tree/music_show) project that was created by a team of 5 and featured four sections:
- **Teleporting Train:** A room with a train that runs on train tracks. At the end of the track is a portal. The user can press E to board the train, which will make the camera follow the train as it moves along the track and through the portal.
- **Audio room:** An audio visualizer, that takes an audio file, and generates a visualization of the magnitude plot, using Fourier transforms.
- **Cube Room:** A room full of cubes, which come towards the user upon starting the game. The user must then press different keys properly to make the cubes disappear as they approach.
- **Colour Room:** A colour room, featuring a spotlight cast over certain objects. The spotlight’s red, green, and blue components can be toggled independently. There are also three coloured, transparent lenses placed in front of everything that can also be toggled independently.

The **cube room** section is my contribution to the interactive digital museum project.

## Summary
1. [Implementation](#Implementation)
2. [Project Structure](#Project-Structure)
3. [Installation Guide](#Installation-Guide)
4. [Game Objective](#Game-Objective)
5. [Controls](#Controls)
6. [Video](#Video)

## Implementation
The **Cube Room** was inspired by the VR game *Beat Saber*, where cubes move toward the player, and the objective is to slice as many as possible. 

In developing this section of the project, I implemented the following steps:
1. **Modeled the Cube and Environment:** I created a 3D cube and set up the room environment where the game takes place.
2. **Cube Movement:** I programmed the cubes to move toward the player at a constant speed, adjusting the movement based on frame time to ensure smooth gameplay.
3. **User Interaction:** I added user input functionality, allowing cubes to disappear when the player presses a designated key, simulating the slicing action.
4. **Score System:** A scoring system was implemented, requiring the player to reach a specific score to win.
5. **Game Mechanics and Difficulty Scaling:** Additional features included dynamic difficulty adjustment based on the player's score and a game-over condition if a cube crosses a red line without being "sliced."

## Project Structure
The project contains several files and folders.

- **assets**: This folder contains all the assets used by the project, including:
   - **audio**: Contains sound effects and music.
   - **textures**: Contains textures files.
   - **libraries**: Third-party libraries used by the project (GLEW, GLFW, GLM, irrKlang).

- `CubeRoom.sln`: The solution file for Visual Studio, which groups the project files and allows the project to be opened and managed in the Visual Studio IDE.

- `CubeRoom.vcxproj`: The Visual Studio project file, containing settings for compiling, linking, and building the project.

- `CubeRoom.vcxproj.filters`: Filters used by Visual Studio to organize files within the IDE. This doesn't affect the actual folder structure on disk but helps organize files within the project in Visual Studio.

- `glew32.dll`: The GLEW dynamic library, which enables the project to handle OpenGL extensions.

- `ikpMP3.dll`: The MP3 plugin for irrKlang, necessary for playing MP3 files.

- `irrKlang.dll`: The core irrKlang dynamic library, responsible for sound playback in the project.

- `main.cpp`: The main source code file for the project, responsible for running the project.

You may ignore `.gitattributes` and `.gitignore` as they are automatically generated by Git.

## Installation Guide

### Pre-Requisites:
**No need to download third-party libraries**, All required libraries (`GLEW`, `GLFW`, `GLM`, and `irrKlang`) are already included in the `assets/libraries` folder of the repository.

### For Visual Studio 2022 on Windows
1. Clone the repository using this link: https://github.com/Abdullah1tani/CubeRoom.git
2. Open `CubeRoom.sln` in Visual Studio 2022.
3. Run `main.cpp`. All dependencies are preconfigured, so it should work without additional setup.

### For Other Versions of Visual Studio on Windows
1. Clone the repository using this link: https://github.com/Abdullah1tani/CubeRoom.git
2. Open `CubeRoom.sln` in your version of Visual Studio.
3. Depending on your version of **Visual Studio**, you need to adjust the library directory to point to the correct version of the GLFW libraries:
   - In **Solution Explorer** Right-Click on the `CubeRoom` project and select *Properties*
  
      ![image](https://github.com/user-attachments/assets/1ac47c63-382d-464a-b5c0-1ac989d451f3)

   - Navigate to *Linker* **>** *General* **>** *Additional Library Directories*
   
      ![image](https://github.com/user-attachments/assets/338439c7-53ab-42a0-8d70-c12508e0d805)

   - Click the dropdown next to **Additional Library Directories** and select **<Edit...>**
   
      ![image](https://github.com/user-attachments/assets/45ad0ecf-7b59-44d4-a642-f9c20e88d120)

      - Double click on `$(ProjectDir)assets\libraries\glfw\glfw-3.4.bin.WIN64\lib-vc2022` and update `lib-vc2022` to the correct version for your Visual Studio installation, as shown below::
      - **Visual Studio 2013**: `lib-vc2013`
      - **Visual Studio 2015**: `lib-vc2015`
      - **Visual Studio 2017**: `lib-vc2017`
      - **Visual Studio 2019**: `lib-vc2019`
      - **Visual Studio 2022**: `lib-vc2022` (default)
        
4. After making the changes, build the project and run `main.cpp`.

### For Other Compilers or Operating Systems
If you're using a compiler or operating system other than Visual Studio on Windows (e.g., GCC on Linux or Clang on macOS), additional configuration may be required:
1. You will need to ensure the project links to the correct libraries for your environment. The `assets/libraries` folder contains all necessary dependencies, but you might need to adjust paths, compile flags, or install the libraries using your system’s package manager (e.g., `apt` for Linux or `brew` for macOS).
2. On macOS or Linux, you'll need to install the appropriate `GLFW`, `GLEW`, `GLM`, and `irrKlang` libraries. Instructions for installing these libraries can be found in the relevant package manager (e.g., `brew install glfw` on macOS or `sudo apt-get install libglfw3-dev` on Ubuntu).
3. Consider using a cross-platform build system like **CMake** to help manage dependencies and platform-specific configurations more easily.

### Notes
Make sure the required `.dll` files (`glew32.dll`, `irrKlang.dll`, `ikpMP3.dll`) are placed in the same directory as the executable when running the project on Windows.

## Game Objective
- **Goal**: Destroy 18 cubes before any of them cross the red line.
- **Game Over**: If a cube crosses the red line, the game is over.

## Controls
Once the program is running, use the following controls to interact with the game:

### Movement:
- `W`: Move forward
- `S`: Move backward
- `A`: Move left
- `D`: Move right

### Game Actions:
- `P`: Start the game
- `G`: Destroy green cubes
- `B`: Destroy blue cubes
- `R`: Destroy red cubes
- `Y`: Destroy yellow cubes
- `O`: Destroy orange cubes
- `M`: Destroy magenta cubes

### Exit:
- `ESC`: Terminate the program

## Video
You can watch the video showcasing the **Cube Room** project on [youtube](https://youtu.be/mQbLZzpFWqA) or download it from the [github release](https://github.com/Abdullah1tani/CubeRoom/releases/tag/video)
