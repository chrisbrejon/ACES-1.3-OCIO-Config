# ACES 1.3-OCIO-Config
Based on the [ACES 1.3 official OCIO Config](https://github.com/AcademySoftwareFoundation/OpenColorIO-Config-ACES/releases/tag/v2.0.0-v2.1.0) I have created a minimal OCIO config of ACES 1.3 for full CG projects:
* Inputs (textures) are in ACEScg
* Rendering and Nuke working space are also in ACEScg
* View Transforms are for sRGB, Rec.1886 and Display P3 displays
* This config uses OCIO 2.3. This is **important**. Please check your software's compatibility.

The main interest of this config is the Look Modification Transform (LMT), which improves some of the visual artifacts present in ACES 1.3.

# Image Examples
Below are some examples of ACES 1.3 without and with the LMT:
<p>
    <img ![hue_sweep_aces] width="128" height="72" src="https://github.com/user-attachments/assets/556a224f-cc91-4907-bf80-0e11c93a5cae" >
    <img ![hue_sweep_brejon] width="128" height="72" src="https://github.com/user-attachments/assets/4182023e-2876-44e3-a2fc-b165dff40e62" >
    <img ![light_sabers_aces] width="128" height="72" src="https://github.com/user-attachments/assets/fcfbad67-4fdf-468d-a932-1c42e436797a" >
    <img ![light_sabers_brejon] width="128" height="72" src="https://github.com/user-attachments/assets/eb749e78-e846-46ee-8e17-8c472d3f1932" >
    <img ![dragon_scene_aces] width="128" height="72" src="https://github.com/user-attachments/assets/6e6df738-2775-4760-9171-52a9b3a5d3da" >
    <img ![dragon_scene_brejon] width="128" height="72" src="https://github.com/user-attachments/assets/ba02a9da-c759-4046-acbf-d3dcb867cc1b" >
    <img ![blue_club_aces] width="128" height="72" src="https://github.com/user-attachments/assets/8abebc34-247e-4a05-ae02-9c539a2de5bb" >
    <img ![blue_club_brejon] width="128" height="72" src="https://github.com/user-attachments/assets/2b533e89-b53e-48d6-adef-58e5c5eb361b" >
    <img ![red_xmas_aces] width="128" height="72" src="https://github.com/user-attachments/assets/2a2d80ac-32f4-4cc0-b976-9d576875a90d" >
    <img ![red_xmas_brejon] width="128" height="72" src="https://github.com/user-attachments/assets/f89cd3fa-95fa-415e-9857-f38168b5a76f" >
    <img ![blue_bar_aces] width="128" height="72" src="https://github.com/user-attachments/assets/a004038f-db0f-4440-9f15-0408de16d82f" >
    <img ![blue_bar_brejon] width="128" height="72" src="https://github.com/user-attachments/assets/59275857-db39-4d2b-a03b-6ea366e324c3" >
    <img ![louise_concert_aces] width="128" height="72" src="https://github.com/user-attachments/assets/0433569a-cf9c-4000-a493-7a50c46aae1b" >
    <img ![louise_concert_brejon] width="128" height="72" src="https://github.com/user-attachments/assets/60990356-f3f7-45ab-bc1f-618758a15332" >
    <img ![stageLights_balls_aces] width="128" height="72" src="https://github.com/user-attachments/assets/597fe9a0-9bd9-449b-be9b-e146763e2a98" >
    <img ![stageLights_balls_brejon] width="128" height="72" src="https://github.com/user-attachments/assets/96628f8d-53d3-4e78-8bf9-a327828e2446" >
    <img ![sunny_spheres_aces] width="128" height="72" src="https://github.com/user-attachments/assets/7b44311a-c8ef-449c-8ea7-42b8ac703f3f" >
    <img ![sunny_spheres_brejon] width="128" height="72" src="https://github.com/user-attachments/assets/6b38eb40-0b79-4c14-99e0-8cf8a370ea6b" >      
</p>

Original files (encoded in "linear-AP0") are available [here](https://www.dropbox.com/scl/fo/fhzx0bcwcjylek1oz7kjc/ACGfmi0EHeufVOQPZLvvk7w?rlkey=53cp61955hbns8x46j6cf8k55&e=1&dl=0).

# About the config
* Reference color space is ACES2065-1
* All transforms come from the original OCIO config
* "ACEScct" can be used for a matte-painting workflow in Photoshop
* "ACEScct" can also be used for color timing and some log operations (such as sharpen)
* Substance_painter roles were set following [this page](https://mrlixm.github.io/blog/substance-painter-color-management/)
* No inverse of the View Transforms has been provided
* One may easily add several colorspaces or displays for HDR output if needed (such as "p3_d65_pq")

# Looks
* There is only one look in this config. It is called "Brejon" and it is based on [my article about **picture formations**](https://chrisbrejon.com/articles/what-makes-a-good-picture-formation/)
* The use of Looks is highly recommended with ACES
* The "Brejon" look has been added to the ACES Views, which have been set by default in the config

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
