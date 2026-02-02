# ACES 1.3-OCIO-Config
Based on the [ACES 1.3 official OCIO Config](https://github.com/AcademySoftwareFoundation/OpenColorIO-Config-ACES/releases/tag/v2.0.0-v2.1.0) I have created a minimal OCIO config of ACES 1.3 for full CG projects:
* Inputs (textures) are in ACEScg
* Rendering and Nuke working space are also in ACEScg
* View Transforms are for sRGB (Gamma 2.2), Rec.1886 and Display P3 (also Gamma 2.2) displays
* This config uses OCIO 2.1, so please check your software's compatibility

Its main interest is the Look Modification Transform (LMT), which improves the visual artifacts present in ACES 1.3.

# Image Examples
Below are some visual examples with:
* First, vanilla ACES 1.3 (left screenshot)
* Then with my "Brejon v005" LMT (middle screenshot)
* Finally with the [Reference Gamut Compression "RGC"](https://docs.acescentral.com/rgc/overview/) (right screenshot)
<p>
    <img ![hue_sweep_aces] width="128" height="72" src="https://github.com/user-attachments/assets/61023c30-f9de-43b7-8e1e-5279f8ecf4ac" >
    <img ![hue_sweep_brejon] width="128" height="72" src="https://github.com/user-attachments/assets/f20f466c-af63-4a27-a2ff-2692eaebee9d" >
    <img ![hue_sweep_rgc] width="128" height="72" src="https://github.com/user-attachments/assets/b6c91eb0-6c65-4677-9ea0-15ad08f71bfc" >
    <img ![light_sabers_aces] width="128" height="72" src="https://github.com/user-attachments/assets/06f44366-7e64-45aa-9094-e5aa03067197" >    
    <img ![light_sabers_brejon] width="128" height="72" src="https://github.com/user-attachments/assets/8b2ecda3-4206-47ab-ac5e-6d526f415ba7" >
    <img ![light_sabers_rgc] width="128" height="72" src="https://github.com/user-attachments/assets/4d53dc76-0737-4738-8a84-a7e3a0e0e7e7" >
    <img ![blue_concert_aces] width="128" height="72" src="https://github.com/user-attachments/assets/8ae56c9c-cd35-487e-bfb9-0f684ee3a145" >
    <img ![blue_concert_brejon] width="128" height="72" src="https://github.com/user-attachments/assets/05207ef4-8913-471a-a3ee-db64c1ce597d" >
    <img ![blue_concert_rgc] width="128" height="72" src="https://github.com/user-attachments/assets/7c9523ff-59a6-42e6-9605-c6366348bcd9" >      
    <img ![blue_club_aces] width="128" height="72" src="https://github.com/user-attachments/assets/ef15e2eb-82d7-4df2-9247-323c5d7ff5c1" >
    <img ![blue_club_brejon] width="128" height="72" src="https://github.com/user-attachments/assets/59117e5e-f137-42e0-b5fa-1630681986dc" >
    <img ![blue_club_rgc] width="128" height="72" src="https://github.com/user-attachments/assets/f7ac69b3-7d5b-4b7d-8f0f-3baec1ed4867" >    
    <img ![louise_concert_aces] width="128" height="72" src="https://github.com/user-attachments/assets/17bec684-fe00-4500-823d-90545449a98f" >    
    <img ![louise_concert_brejon] width="128" height="72" src="https://github.com/user-attachments/assets/5ee6c506-c676-43d8-a0d8-36441d3ca0c5" >
    <img ![louise_concert_rgc] width="128" height="72" src="https://github.com/user-attachments/assets/bb8ac557-80d5-430d-a204-0d7414ae80f0" >
    <img ![dragon_scene_aces] width="128" height="72" src="https://github.com/user-attachments/assets/cb16ab68-a6e8-438c-bb56-50350ac986fd" >
    <img ![dragon_scene_brejon] width="128" height="72" src="https://github.com/user-attachments/assets/f24253a2-6ba5-4ad0-9700-db7a36252a8c" >
    <img ![dragon_scene_rgc] width="128" height="72" src="https://github.com/user-attachments/assets/f3fcfd04-1c7b-4a3b-8f1a-4f1434803265" >
    <img ![red_xmas_aces] width="128" height="72" src="https://github.com/user-attachments/assets/b1d78c54-f7b8-4645-ab61-260d05a78c22" >    
    <img ![red_xmas_brejon] width="128" height="72" src="https://github.com/user-attachments/assets/5612e711-6457-4fa7-ab45-a05567215d0b" >
    <img ![red_xmas_rgc] width="128" height="72" src="https://github.com/user-attachments/assets/407c14d3-99a8-416a-a649-9710185f9646" >
    <img ![red_diver_aces] width="128" height="72" src="https://github.com/user-attachments/assets/a407daf1-a2b9-4b28-99f9-16beb28cabaa" >
    <img ![red_diver_brejon] width="128" height="72" src="https://github.com/user-attachments/assets/6c12be54-0008-4548-9009-a39eb4a4437b" >
    <img ![red_diver_rgc] width="128" height="72" src="https://github.com/user-attachments/assets/2bb31550-935d-4f36-b9fd-0384bd41f009" >      
    <img ![stageLights_balls_aces] width="128" height="72" src="https://github.com/user-attachments/assets/c86d7fe3-9f34-4188-89e8-adb7b7e6c614" >    
    <img ![stageLights_balls_brejon] width="128" height="72" src="https://github.com/user-attachments/assets/0d275440-0dbd-4f5c-a1a1-f450a52bf520" >
    <img ![stageLights_balls_rgc] width="128" height="72" src="https://github.com/user-attachments/assets/37d39316-4e43-4b1a-80d5-c0ac5dab74c8" >
    <img ![sunny_spheres_aces] width="128" height="72" src="https://github.com/user-attachments/assets/65cb8a5f-5fd7-42ce-a814-9288ab3e4238" >    
    <img ![sunny_spheres_brejon] width="128" height="72" src="https://github.com/user-attachments/assets/fd6dfaf5-5b80-45b2-9cf9-656b3d0d1435" >
    <img ![sunny_spheres_rgc] width="128" height="72" src="https://github.com/user-attachments/assets/c4d3cfea-d8ba-4f84-94dd-fff24cb26e0b" >
    <img ![blue_bar_aces] width="128" height="72" src="https://github.com/user-attachments/assets/48970cc7-a061-40d1-b27b-49a6fe719c49" >
    <img ![blue_bar_brejon] width="128" height="72" src="https://github.com/user-attachments/assets/d3302cd2-562c-4c56-8278-d8bdff31a34f" >
    <img ![blue_bar_rgc] width="128" height="72" src="https://github.com/user-attachments/assets/3b7910e6-1c0f-4770-bc7e-7a4727ce47fb" >    
    <img ![blue_pool_aces] width="128" height="72" src="https://github.com/user-attachments/assets/342782de-2baa-403b-b880-8cc09646fc55" >
    <img ![blue_pool_brejon] width="128" height="72" src="https://github.com/user-attachments/assets/7b1ae5e6-208f-4b76-827c-aab61b46356d" >
    <img ![blue_pool_rgc] width="128" height="72" src="https://github.com/user-attachments/assets/5e6a81fb-2fdb-4178-b6d1-f046dfa05d96" >    
</p>

Original files (encoded in "ACES2065-1") are available [here](https://www.dropbox.com/scl/fo/fhzx0bcwcjylek1oz7kjc/ACGfmi0EHeufVOQPZLvvk7w?rlkey=53cp61955hbns8x46j6cf8k55&e=1&dl=0).

# About the config
* Reference color space is ACES2065-1
* All transforms come from the original OCIO config (based on [CTL code)](https://github.com/aces-aswf/aces-output/tree/dev)
* The "XYZ to RGB matrix" for the DisplayP3 transform comes from [Antler Post](https://antlerpost.com/colour-spaces/P3D65.html#matrices)
* This matrix can be generated using [Colour Science](https://www.colour-science.org/apps/) using "DCDM XYZ" and "P3-D65" with no CAT
* "ACEScct" can be used for a matte-painting workflow in Photoshop
* "ACEScct" can also be used for color timing and some log operations (such as sharpen)
* Substance_painter roles were set following [this page](https://mrlixm.github.io/blog/substance-painter-color-management/)
* One may easily add several colorspaces or displays for HDR output if needed (such as "p3_d65_pq")

# Look Modification Transform
* The main look in this config is called "Brejon" and is based on [my article about **picture formations**](https://chrisbrejon.com/articles/what-makes-a-good-picture-formation/)
* Its purpose is to give a pleasing aspect by carefully rebalancing purity, brilliance and hue path bendings
* The use of looks is highly recommended with ACES and the "Brejon" look has been added to the ACES Views by default to the config (just like the RGC)

# A plea for an ACES 1.3 LMT
* LMTs are not an anomaly. They are a necessary step of the pipeline, as [designed by The Academy](https://docs.acescentral.com/system-components/look-transforms/)
* LMTs are a way to make your projects look truly unique. With the right tools, you may craft your visual identity (picture formations should not be standardized)
* ACES 1.X got released in December 2014 and the Output Transforms are a bit crude and simplistic. My LMT compensates for the lack of "purity attenuation"
* My LMT is meant to give a better starting point to the artists by providing a better depiction of energy in our images. Something we **CANNOT** compensate for later
* My LMT is non-destructive since it is applied on-the-fy as part of the "View". It can be modified or even removed if needed.
* LMTs are easy to add to OCIO configs. Its implementattion lies in a few lines of code and an external LUT file.

# Other available Color Management Workflows
| Name                                                                                             | Author               | Release date |              Observations                             |
|:---:                                                                                             |         :---:        |      :---:   |                 :---:                                 |
| [ARRI K1S1](https://www.arri.com/en/learn-help/learn-help-camera-system/tools/lut-generator)     | Harald Brendel       | 2011         | THE most used LUT on the planet (ARRI Alexa workflow) |
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
