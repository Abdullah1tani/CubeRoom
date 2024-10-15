# Cube Room

The Cube Room project is part of the project interactive [digital museum]([https://github.com/mboudr35/glgine](https://github.com/mboudr35/glgine/tree/music_show)) project that was created by a team of 5 and featured four sections:
- **Teleporting Train:** A room with a train that runs on train tracks. At the end of the track is a portal. The user can press E to board the train, which will make the camera follow the train as it moves along the track and through the portal.
- **Audio room:** An audio visualizer, that takes an audio file, and generates a visualization of the magnitude plot, using Fourier transforms.
- **Cube Room:** A room full of cubes, which come towards the user upon starting the game. The user must then press different keys properly to make the cubes disappear as they approach.
- **Colour Room:** A colour room, featuring a spotlight cast over certain objects. The spotlight’s red, green, and blue components can be toggled independently. There are also three coloured, transparent lenses placed in front of everything that can also be toggled independently.

The **cube room** section is my contribution to the interactive digital museum project.

## Implementation
The **Cube Room** was inspired by the VR game *Beat Saber*, where cubes move toward the player, and the objective is to slice as many as possible. 

In developing this section of the project, I implemented the following steps:
1. **Modeled the Cube and Environment:** I created a 3D cube and set up the room environment where the game takes place.
2. **Cube Movement:** I programmed the cubes to move toward the player at a constant speed, adjusting the movement based on frame time to ensure smooth gameplay.
3. **User Interaction:** I added user input functionality, allowing cubes to disappear when the player presses a designated key, simulating the slicing action.
4. **Score System:** A scoring system was implemented, requiring the player to reach a specific score to win.
5. **Game Mechanics and Difficulty Scaling:** Additional features included dynamic difficulty adjustment based on the player's score and a game-over condition if a cube crosses a red line without being "sliced."
   
