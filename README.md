# Unreal_JabberwockHospital
I recreated the Jabberwock Hospital from Danganronpa 2: Goodbye Despair in 3D using Unreal Engine and Blender, and used blueprint programming to create events that trigger based on the time of day as well as events that are based on the player's position. 

Dangaonronpa 2 is a murder mystery game. Here are the screenshots from the original game that's mostly 2D.
![hospital outside](https://github.com/user-attachments/assets/1c530dc1-45ea-41fa-936d-8a6caff88290)
![hospital lobby](https://github.com/user-attachments/assets/7b5ff54e-d3ce-4b5d-abc2-1a1a418b7c66)
![hallway](https://github.com/user-attachments/assets/f204c36d-82cf-4710-9072-a7b59602b900)



And here is my recreation of the hospital from the game.

The playthrough video: https://www.youtube.com/watch?v=W069lV4zNYE

The breakdown video: https://www.youtube.com/watch?v=WH4GCpHf2HU

![hospital_exterior](https://github.com/user-attachments/assets/abf9ab75-0c8f-47a2-b5cf-114f161cb950)

I took creative liberties with the surrounding area of the hospital as I wanted to move onto other aspects of the Unreal Engine, like blueprint programming. 


![BP_security_cam](https://github.com/user-attachments/assets/37771fec-e627-496d-80dd-ae2e0a7cc9f0)
The cameras in the original game didn't move to face the player since they were part of a 2D background, but since this was a 3D open space environment, I wanted the cameras to always be facing the player to make it feel like they're being watched. The above script takes the positions of the camera and the player and updates the camera's z rotation value (with an offset of -90 degrees applied) so that it only rotates in that axis to follow the player while keeping the other axes constant.


![BP_Day_Night_cycle](https://github.com/user-attachments/assets/80184347-364a-4638-8c77-aff24dfa32fc)
I had pretty neon lights in the hospital interior just like in the actual game, and wanted to do both a day time look as well as a night time look, so I opted for updating the sun and moon's position in real time to do the day/night cycle. The time variable controls the speed of the day/night cycle. I opted to use a small value for the time variable so that there's enough time to see both looks in the video. If it were an actual game, a larger value would have been chosen for the time variable to make the day/night cycle feel more real.

![Material_Editor_Day_Night_Cycle](https://github.com/user-attachments/assets/578c00f7-f768-4fa1-a3c8-e59981ac4827)
This is the sky material that gets updated based on the positions of the sun and the moon.


![BP_ceiling_light](https://github.com/user-attachments/assets/b189d15f-7727-4b28-9ffb-d5c30d98809d)
The ceiling lights are turned off a few hours after the moon shows up and the world outside is dark, and turn back on when the sun reappears. These values being used in the if/else conditions are based on the positions of the sun and the moon.
