## Project
This prototype project built on [Unity](https://unity.com/) explores alternative methodologies aiming for speed to calculate pixel colors to Hounsfield units set by the user and assess the quality of two different types of render methods.

Methodologies: [Unity's Burst compiler (v 1.4.1) multithreaded jobs on CPU](https://docs.unity3d.com/Packages/com.unity.burst@0.2-preview.20/manual/index.html) and [Compute Buffers on GPU](https://docs.unity3d.com/2020.3/Documentation/ScriptReference/ComputeBuffer.html). 

Rendering scenarios tested for quad meshes (2D-plane equivalent images) and raymarching volumetric cloud. Each scenario is contained in a Unity scene.

Each prototype scene was not extended in full because these are a proof of concept and used determine the viability of the approach for our purposes. There is no further support for this repo.

Project collaborator and donor of dicom images: Centre de Diagnosi per la Imatge de Tarragona. The project currently has no dicom images, unfortunately the images were never further anonymized for github distribution.

<p align="center">
<img width="150" alt="star" src="https://github.com/sergiosolorzano/ai_gallery/assets/24430655/3c0b02ea-9b11-401a-b6f5-c61b69ad651b">
</p>

---------------------------------------------

## Project Software
Unity version: Unity 2020.3.36f1, Build Platform PC Standalone.

Unity Render Pipeline: Built-in.

Dicom images data processed with the [Fellow Oak DICOM library](https://github.com/fo-dicom/fo-dicom) subject to [The MIT License (MIT), Copyright (c) Microsoft Corporation license]((https://github.com/fo-dicom/fo-dicom/blob/development/License.txt))

## License
This project is licensed under the MIT License. See [LICENSE.txt](https://github.com/sergiosolorzano/Dicom-3DRender/blob/main/LICENSE.md) for more information.

## Features

* Dicom Processing: When the scene is played, progress of the dicom images being processed is displayed in the Inspector:

  <img width="246" alt="Dicom-Images-Processed-Progress" src="https://user-images.githubusercontent.com/24430655/176902397-e3ed3745-2ba0-4c39-95e3-bd66d9aa6ad3.PNG">

* Render options:
  * Axial, Coronal and Sagittal axis are available. Axial axis was the base for our study and it is recommended to explore the Unity project.
  
  * Render Scenes (Scenes found in unity project folder ..\Assets\Scenes\):
  
    + VolumetricRender_3DRenderTexture.unity: Raymarching volumetric cloud render using 3D Render Textures with Slicing functionality. Hounsfield units set according to Window width and Window Center selected by the user. Single study axis (axial, coronal, sagittal) at once.

      <video src="https://user-images.githubusercontent.com/24430655/176890215-a7bb0a66-8046-4785-87d0-34494c17385b.mp4" controls="controls" muted="muted" playsinline="playsinline">
      </video>
      
    + VolumetricRender_3DTexture.unity: Raymarching volumetric cloud render using 3D Textures with Slicing functionality. Hounsfield units cannot be re-adjusted. Single study axis (axial, coronal, sagittal) at once.
  
      <video src="https://user-images.githubusercontent.com/24430655/176886772-4135dc33-e270-4643-8c2f-4b942009eaee.mp4" controls="controls" muted="muted" playsinline="playsinline">
      </video>

    + QuadMesh_CPU-RGBA_Range_Picker.unity: 3D model renders on multiple quad meshes according to the RGBA (0-255) unit range selected by the user. Multiple study axis (axial, coronal, sagittal) may be rendered at once and aligned.

      <video src="https://user-images.githubusercontent.com/24430655/176893082-cbd84e36-e1a6-43e7-a66e-0c1ad1fb441e.mp4" controls="controls" muted="muted" playsinline="playsinline">
      </video>
      
    + QuadMesh_GPU_CB_Windowing.unity: Quad meshes: 3D model renders on multiple quad meshes according to the Hounsfield unit set on a Window width and Window Center selected by the user. Multiple study axis (axial, coronal, sagittal) may be rendered at once and aligned.
  
      <video src="https://user-images.githubusercontent.com/24430655/176882412-39a4156d-2e70-451a-b6c3-ac033135e69a.mp4" controls="controls" muted="muted" playsinline="playsinline">
      </video>
  
      <video src="https://user-images.githubusercontent.com/24430655/178246241-c15854c9-c0c2-46b1-86a3-4885c7c21dad.mp4" controls="controls" muted="muted" playsinline="playsinline">
      </video>

      If you find this helpful you can buy me a coffee :)
   
      <a href="https://www.buymeacoffee.com/sergiosolorzano" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a>
      
