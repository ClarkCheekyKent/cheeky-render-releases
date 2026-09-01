# CheekyRender
## About
Cheeky Render is a mod that enables VR integration to Forza Horizon 6. It includes many features an optimizations to the point that it runs better than flat screen for me in mono. 

My setup is Quest 3 via Virtual Desktop on NVidia 5070. This has not been tested for other combinations.

Current release is an early preview that has some optionals features not working (like weather/time control which is still in development).

<img width="3840" height="2160" alt="c7f174cdf65543ed8ffb2f56bcf815c3" src="https://github.com/user-attachments/assets/18ecfc33-6e56-46ff-acd0-c5133a33c565" />
<img width="751" height="1373" alt="image" src="https://github.com/user-attachments/assets/1a1bd33f-00be-4b76-ad5a-f64cb0239b75" />

### Features
* Different options for running the game. Mono, AFR-Half, AFR full rate.
  * Mono - easiest and best for performance and clarity but no depth.
  * AFR-Half - runs the game at headset FPS, but half the rate for each eye. So if your headset is 72 FPS, this will provide 36 fps per eye. Not ideal since it causes smearing and just feels like low fps.
  * AFR full rate - runs the game at double the headset FPS, (so 144fps if your headset is 72) requires a beefy computer or lowered render resolution settings.
* Tagging of game frames to specific eye to reduce flickering in AFR
* Foveated rendering - Reduces GPU work around the periphery. Minor gains (few fps) if you're not using DLSS. Don't think it does anything if you are using DLSS though.
* Foveated DLSS-SR - Only applies DLSS upscaling in the center region. This is huge for performance (20-30 fps). This is how I am able to run VR mono at higher FPS than flat.
  * TAA on periphery implementation may be bugged, feels blurrier than it should so I leave it disabled for now 

* Foveated DLSS-NR (DLSS5) - Enables DLSS 5. Requires you to paste in the streamline .DLLs files into FH6 directory. Foveated just like DLSS-SR for MUCH lower performance hit.
* Vehicle LOD Fix - Fixes the really annoying flashing when you get close to vehicles by extending their LOD distance. I disabled by default since it searches and modifies game memory but been using it for a month with no issue.
* Camera controls with hotkeys. Alt-SHIFT-(WASD/QE) allows you to dynamically adjust the seating position inside the car. I bound these to the DPAD on my wheel and it allows me to adjust seating position inside the car in seconds.
* Floating Map/Speedo Scoreboard - The most important UI elements are not head tracked constantly in your view but instead floating in fixed location. You can enable/disable them as needed.
* Floating Flat Screen - When not in 6DOF mode (menu, cutscenes, etc) The menu is in a fixed floating location. There are controls for adjusting its size and location as well.
* Far Chase Cam - Allows VR mode outside cockpit view.


### What settings I run Forza Horizon 6

I care more about stability and clarify so I run mono at 72 FPS 1.3 render resolution GodLike setting in Virtual Desktop 500mbit connection via USB dongle. FOV tangent 85 Vertical 75 Horizontal. I can also do 100 FPS at 1.0 render res which is still 3024x2836.

I found for me Stereo AFR-Half 1.0 render resolution with headset set to 120 FPS works if you want depth. Maybe even make the Foveated DLSS smaller for more perf as the shimmer isnt as noticible in stereo.

#### HUD & GAMEPLAY
* Pause on Focus Lost - Disabled
  * Allows editing the VR settings live
* HUD Safe Frame Horizontal/Vertical - 3
  * Puts the UI elements in corner of screen so they're not in the way.

  * Default HUD settings in VR are based on this number, but you can adjust both

#### VIDEO
* **IMPORTANT** Make sure Frame Rate is unlocked, Vertical Sync OFF
* Full Screen Off helps me adjust VR settings while running game
* DLSS-Performance
  * Huge perf gains especially with Foveated-DLSS-SR
* FOV Sliders All maxed out

* Car Detail -> Extreme
  * More detailed/high-res car interior
* Environment Texture Quality -> Ultra
  * Required by the Geometry setting below, Extreme uses too much VRAM.  
* Environment Geometry Quality -> Extreme
  * Prevents object pop in 
* Reflections / SSR -> Medium
* Shadow -> Low
* Screen Space GI -> Medium
* Shader Quality -> High
* Other settings Low/medium
  
### Bugs/Issues
* Flicker can still happen in AFR if dropping below headset FPS rate.
* If settings set to high and you run out of VRAM it causes issues and you may have to restart game and the VR mod.

### Disclaimer
This mod injects hooks into the Forza Horizon 6 instance (similar to how reshade works). 

I have personally been using it for 50+ hours without issue, that said it is probably detectable IF Forza decides to adds anticheat and start banning people for graphical mods. 

This is probably unlikely given they haven't done so far for its other games and care more about cheating like money or gameplay but I do want to put that out there.
