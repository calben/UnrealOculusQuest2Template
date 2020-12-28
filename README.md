# Oculus Quest 2 Unreal Engine Template

Template project designed to serve as a reference for developing on the Oculus Quest 2!

# Preparing a Project for the Oculus Quest 2

## Project Setup

1. Create a new VR project with mobile, scalable 2d or 3d, and raytracing disabled.  You could also use a blank project, but the VR project set up reasonable input mappings for you.
1. Add Android and Win32 to the supported platforms.

## Project > Packaging

1. Add "MotionControllerMap" to the list of maps to include in packaged build. (ontent not included in the maps will not be packaged, reducing the package size)
1. Check cook only maps
1. Exclude editor content
1. Add your used maps to the List of maps to include in a packaged build


## Project > Rendering

1. Enable forward rendering. (forward rendering has better performance on lower specc'd devices and is a good choice for virtual reality applications)
1. Enable msaa and set mobile MSAA to 4x (switches to an anti-aliasing appropriate for forward rendering with a reasonable quality level)
1. Instanced stereo enabled (performance improvement that reduces cpu usage)
1. Mobile HDR disabled (mobile hdr is reportedly dodgy on the quest)

## Platforms > Android

1. Run configure now after setting up for Android development
1. Set Android package Name
1. Set the minimum SDK version to 23 and target to 25
1. Ensure fullscreen immersive is checked
1. Uncheck support OpenGL ES3.1 and support Vulkan instead (improves CPU performance)
1. Add Oculus Quest 2 and Oculus Quest to package for Oculus devices array

## Plugins > OculusVR

1. Enable specific color gamut with the Quest color space
1. Enable HQDistortion
1. Enable FFRLevel on Low
1. Enable Chroma Correction

Open the "Launch Oculus Performance Window Mode" as well and review these items.


# Packaging

1. Under File > Package Project > Android select Android (ASTC), opening a file dialogue
1. Create a new directory "Build" in the top level of your project
1. Select the "Project/Build" directory as the destination for the Android build

