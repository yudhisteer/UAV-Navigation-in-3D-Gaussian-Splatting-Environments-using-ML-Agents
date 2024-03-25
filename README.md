# UAV Navigation in 3D Gaussian Splatting Environments using ML-Agents

## Plan of Action
1. NeRF in a nutshell
2.  3D Gaussian Splatting

------------------------------
## 1. NeRF in a nutshell
In a previous project - [Assessing NeRF's Efficacy in 3D Model Reconstruction: A Comparative Analysis with Blender](https://github.com/yudhisteer/Assessing-NeRF-s-Efficacy-in-3D-Model-Reconstruction-A-Comparative-Analysis-with-Blender) - I explained the mechanics behind NeRF and how to train a NeRF from scratch. In this section, I will briefly recap on the workings of NeRF. 

In a nutshell, NeRF is about 3D reconstructing a scene and providing photorealistic novel-view synthesis based on a series of 2D images represented using a continuous neural radiance field, which is a neural network. 

But how is this different from traditional methods? Well, traditional 3D reconstruction methods such as point clouds, voxel grids, or meshes are **discrete methods**.

1. **Point clouds**: Each point in 3D space have its own set of **(x, y, z)** coordinates.
2. **Voxel Grids**: Represents the 3D geometry as a regular grid of **cubic voxels** (**volumetric pixels**), where each voxel is either occupied or empty.
3. **Meshes**: A mesh representation consists of a set of **vertices** (points in 3D space), **edges** (lines connecting vertices), and **faces** (typically triangles formed by vertices and edges). 

In all these three methods, the continuous 3D geometry is **approximated** by a ```finite set``` of **discrete** elements such as points, voxels, vertices, and faces. 

In NeRF, the 3D scene is represented by a ```continuous function``` that maps a **3D position coordinate** ```(x, y, z)``` and a **viewing direction** ```(θ, φ)``` to a **color** ```(RGB)``` and a **density** value. This function is modeled by a ```neural network``` trained on a series of 2D images and their corresponding ```camera poses``` (intrinsic and extrinsic parameters).

Again, how is this different from traditional rending 3D graphics?

1. **Rasterization**: We take 3D meshes and convert them into 2D pixels. The meshes are effectively projected onto the 2D image plane and filled in with color values.
2. **Ray Tracing**: Ray tracing calculates how light interacts with objects in a 3D scene. Rays are tracked from the viewer's eye through each pixel on the screen, considering complex interactions such as reflections and refractions.

With NeRF, we are reconstructing our scene within a Neural Network such that the **weights** and parameters of the latter, are an **encoding** representation of our actual scene. As such, NeRF renders images by **querying** the neural network at various points along camera rays and accumulating the color and density values.

<p align="center">
  <img src="https://github.com/yudhisteer/UAV-Navigation-in-3D-Gaussian-Splatting-Environments-using-ML-Agents/assets/59663734/7401dff2-a640-40a4-90fa-e48afb2b542a" width="50%" />
</p>


<p align="center">
  <img src="https://github.com/yudhisteer/UAV-Navigation-in-3D-Gaussian-Splatting-Environments-using-ML-Agents/assets/59663734/42c7119a-ae95-4355-acf8-b271b08e1ffc" width="50%" />
</p>



------------------------------
## 2.  3D Gaussian Splatting

------------------------------

## References
1. https://www.thomasantony.com/posts/gaussian-splatting-renderer/
2. https://github.com/MrNeRF/awesome-3D-gaussian-splatting
3. https://comfyanonymous.github.io/ComfyUI_examples/3d/
4. https://radiancefields.com/comfy3d-integrates-triposr/
5. https://github.com/MrForExample/ComfyUI-3D-Pack?tab=readme-ov-file#install
6. https://radiancefields.com/comfy3d-for-comfyui/
7. https://radiancefields.com/how-nerfs-will-alter-our-lives-fashion/
8. https://radiancefields.com/comfy3d-integrates-triposr/
9. https://huggingface.co/spaces/stabilityai/TripoSR
10. https://radiancefields.com/how-to-create-gaussian-splats-with-nerfstudio/
11. https://www.youtube.com/watch?v=x604ghp9R_Q
12. https://www.youtube.com/watch?v=Sxy7tcRZh-8
13. https://github.com/chiehwangs/3d-gaussian-theory
14. https://www.youtube.com/watch?v=VkIJbpdTujE
15. https://www.reshot.ai/3d-gaussian-splatting
16. https://johnowhitaker.github.io/tglcourse/
17. https://www.youtube.com/watch?v=jV1g5OY0L5s
18. https://sketchfab.com/3d-models/sleeping-cat-on-the-bed-1-3d-scan-ae07a741be6944e8ba5e2657069d3aaf
