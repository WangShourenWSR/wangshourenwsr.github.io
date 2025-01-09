---
layout: page
title: Motion-Controlled Parkour Game
description: Developed a gesture-controlled parkour video game using the Unity3D engine and CNN model.
img: assets/img/projects/alien_shooter-like_game/motion-controlled_parkour_game.png
importance: 100
category: work
related_publications: false
---
Here is a introduction for our game (This video is in Chinese): 

<video controls width="640" height="360">
    <source src="{{ site.baseurl }}/assets/video/projects/alien_shooter-like_game/intro_video.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video>
## Introduction

This project explores gesture-based interaction technology applied to games by developing a gesture-controlled endless runner game using Unity3D. Inspired by games like *Subway Surfers*, this project leverages gesture recognition as a natural interaction method to control player movements, enhancing gameplay immersion. Players can use gestures to navigate a virtual world, controlling character movements such as jumping and switching lanes in real time. The game integrates gesture recognition, real-time graphics, and an interactive design to deliver a seamless gaming experience.

## Development Highlights
### Technical Highlights

- **Gesture Recognition System:** Developed a hand gesture recognition system using CNN model and OpenCV library to track hand positions from real-time video feeds. Recognized gestures include:
  - Left hand detected: Character moves left.
  - Right hand detected: Character moves right.
  - Both hands raised: Character jumps.
- **Integration with Unity3D:** Implemented a pipeline to connect Python-based gesture recognition with Unity3D using text files for real-time communication. Resolved cross-process file access conflicts to ensure smooth gameplay.
- **Endless Level Design:** Designed a dynamic "endless runner" level system with modular track segments that load and unload seamlessly during gameplay. This approach ensures a visually continuous environment while optimizing resource usage.
- **Collision and Reward Systems:** Programmed collision detection to handle player deaths and item pickups. Designed a coin collection system integrated with an in-game shop.

### Creative Highlights

- **Gameplay Design:** Conceptualized and implemented core gameplay mechanics, including gesture-based controls and an endless runner environment. The game features a simple yet intuitive interaction system that relies on hand gestures to control character actions, replacing traditional input methods for a more immersive experience.
- **Visual and Audio Aesthetics:** Designed vibrant game environments with Unity3D, creating subway-themed tracks, obstacle models, and interactive elements. Integrated background music and sound effects to enhance the gameplay atmosphere.


## Outcome

The project successfully delivered a functional prototype of a gesture-controlled endless runner game. The integration of gesture recognition with Unity3D demonstrated the potential of natural interaction methods in enhancing gameplay experiences. The game lays a strong foundation for future improvements, such as adding new levels, more gesture-based actions, and additional in-game features.

## Additional Notes

- Due to the large size of the project files, they have not been uploaded. If you are interested, please feel free to contact me via email.
- This project report was originally written in Chinese and has not been uploaded. If you wish to review the report, please contact me via email.
