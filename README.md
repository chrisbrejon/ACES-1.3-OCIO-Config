# ACES 1.3-OCIO-Config
Based on the [ACES 1.3 official OCIO Config](https://github.com/AcademySoftwareFoundation/OpenColorIO-Config-ACES/releases/tag/v2.0.0-v2.1.0) I have created a minimal OCIO config of ACES 1.3 for full CG projects:
* Inputs (textures) are in ACEScg
* Rendering and Nuke working space are also in ACEScg
* View Transform is for sRGB, Rec.1886 and Display P3 displays

The main interest of this config is the LMT called "Brejon". I hope it will help you **crafting beautiful images**. Enjoy!

# Image Examples
Below are some examples of ACES 1.3 without and with the LMT. The LMT tries to improve some of the visual artifacts present in ACES 1.3.
<p>
    <img ![hue_sweep_aces] width="144" height="81" src="https://github.com/user-attachments/assets/877ce4d2-2062-4c17-9903-405dcd04a563" >
    <img ![hue_sweep_brejon] width="144" height="81" src="https://github.com/user-attachments/assets/db1af377-ccbe-40f4-a227-36202cbe5370" >
    <img ![light_sabers_aces] width="144" height="81" src="https://github.com/user-attachments/assets/ebcd2771-139e-4aec-911a-03db1e10be3d" >
    <img ![light_sabers_brejon] width="144" height="81" src="https://github.com/user-attachments/assets/6699cc31-448f-4abc-8eb4-2933e8f0510b" >
    <img ![dragon_scene_aces] width="144" height="81" src="https://github.com/user-attachments/assets/45e9cac1-2bd5-4260-af17-18506d88bbf0" >
    <img ![dragon_scene_brejon] width="144" height="81" src="https://github.com/user-attachments/assets/ddf4c39c-0aa4-44f0-b657-3de75cdd4dd7" >
</p>

Original files (encoded in "linear-AP0") are available [here](https://www.dropbox.com/scl/fo/fhzx0bcwcjylek1oz7kjc/ACGfmi0EHeufVOQPZLvvk7w?rlkey=53cp61955hbns8x46j6cf8k55&e=1&dl=0).

# About the config
* Reference color space is ACES2065-1
* All matrixes come from the original OCIO config
* "ACEScct" can be used for a matte-painting workflow in Photoshop
* "ACEScct" is the shaper space for the LMT. It can be used for color timing and some log operations (such as sharpen)
* Substance_painter roles were set following [this page](https://mrlixm.github.io/blog/substance-painter-color-management/)
* No inverse of the View Transforms has been provided
* One may easily add several colorspaces or displays for HDR output if needed (such as "p3_d65_pq")

# Looks
* There is only one look in this config. It is called "Brejon" and it is based on [my article about **picture formations**](https://chrisbrejon.com/articles/what-makes-a-good-picture-formation/)
* The use of Looks is highly recommended with ACES
* To use the "Brejon" look, I have combined it with the Views. This is the default View in the config.

# Other available Color Management Workflows
| Name                                                                                             | Author               | Release date |              Observations                             |
|:---:                                                                                             |         :---:        |      :---:   |                 :---:                                 |
| [ARRI K1S1](https://www.arri.com/en/learn-help/learn-help-camera-system/tools/lut-generator)     | Harald Brendel       | 2011         | THE most used LUT on the planet (ARRI Alexa workflow) |
| [ACES](https://github.com/AcademySoftwareFoundation/OpenColorIO-Config-ACES/releases)            | AMPAS                | 2016         | Color Encoding System developed by the Academy |
| [Filmic](https://github.com/sobotka/filmic-blender)                                              | Troy Sobotka         | 2017         | Original Blender Color Management used on [this movie](https://www.youtube.com/watch?v=uf3ALGKgpGU) |
| [RED IPP2](https://support.red.com/hc/en-us/articles/360041467533-RED-LUT-Downloads)             | Graeme Natress       | 2017         | RED Image Processing Pipeline explained [here](https://www.red.com/red-tech/image-processing-pipeline-ipp2) |
| [Sony Venice](https://sonycine.com/resources/luts/)                                              | Sony / Picture Shop  | 2022         | LUT files made in partnership with [Picture Shop](https://www.pictureshop.com/) |
| [ARRI Reveal](https://www.arri.com/en/learn-help/learn-help-camera-system/tools/lut-generator)   | Sean Cooper          | 2022         | The new ARRI Alexa35 workflow described [here](https://www.youtube.com/watch?v=s_RXjVeC_7s) |
| [Tony](https://github.com/h3r2tic/tony-mc-mapface)                                     | Tomasz Stachowiak    | 2023         | A cool-headed display transform |
| [AgX Blender](https://github.com/EaryChow/AgX)                                                   | Eary Chow            | 2023         | Blender Color Management used on [this video game](https://www.youtube.com/watch?v=mVjBRZqajYY) |
| [TCAMv3](https://www.filmlight.ltd.uk/support/customer-login/colourspaces/colourspaces.php)      | Daniele Siragusano   | 2024         | Baselight Color Management Workflow explained [here](https://youtu.be/DL4n6LErMbw?t=325) |
| [AgX SB2383](https://github.com/sobotka/SB2383-Configuration)                                    | Troy Sobotka         | 2024         | Minimal AgX OCIO Config using Linear BT.709 |
| [JP-2499](https://github.com/jedypod/JP2499)                                                     | JP Zambrano          | 2024         | A popular picture formation pipeline described [here](https://www.liftgammagain.com/forum/index.php?threads/2499-drt-an-alternative-picture-formation-pipeline.18639/) |
| [Open DRT](https://github.com/jedypod/open-display-transform)                                    | Jed Smith            | 2024         | State-of-the-art Color Management Workflow |
