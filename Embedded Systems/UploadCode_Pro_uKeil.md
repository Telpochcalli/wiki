# Upload code to the robot with uKeil Pro version

Before doing any of the following steps, you should the [GuideEmbeddedSystems file](GuideEmbeddedSystems.md).

## Actual steps:
1. Obtain your desired project from Robomaster's or your team's Git. 
1. Open uKeil IDE.
1. On the to left part of the screen:
    * Click project.
    * Open project.
    * Browse your files until you find `something.uvprojx`. It's usually under the MDK-ARM folder (from Robomaster's examples).
    * <img src="imgEmbSys/rm_selectfile.PNG"
     alt="Select file" />
1. Click on the **Magic Wand** from the tools menu.
    * <img src="imgEmbSys/rm_keilMagicWand.PNG"
        alt="Open Magic Wand settings" />
    * The following menu will pop-up:
    * <img src="imgEmbSys/rm_magicWandMenu.PNG"
        alt="Preview Magic Wand menu" />
1. Go to the Debug tab
    * <img src="imgEmbSys/rm_debugconfig.PNG"
        alt="Debug menu" /> 
    * Select ST-Link Debugger
1. Click on the `settings` button next to it
    * If you intalled correctly ST-Link drivers, and the USB stick is connected to the computer, a device will apear.
    *  <img src="imgEmbSys/rm_setup.PNG"
        alt="Select ST-Link in debug tab" /> 
1. Close all menus by saving or clickin ok.
1. Build the project.
    * <img src="imgEmbSys/rm_build.PNG"
        alt="Build project" /> 
1. Upload it `LOAD`.