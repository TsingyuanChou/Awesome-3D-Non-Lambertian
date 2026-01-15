# Awesome 3D Non-Lambertian List

> A curated list of papers & resources linked to **3D Reconstruction and Novel View Synthesis on Non-Lambertian Surface**.


# Contents

- [Awesome 3D Non-Lambertian List](#awesome-3d-non-lambertian-list)
- [Contents](#contents)
- [Papers](#papers)
  - [3D Neural Representation](#3d-neural-representation)
    - [View-dependent Appearance Modeling](#view-dependent-appearance-modeling)
      - [Decomposition of Transmitted and Reflected Radiance](#decomposition-of-transmitted-and-reflected-radiance)
      - [Directional Encoding for High-frequency Specularity](#directional-encoding-for-high-frequency-specularity)
    - [Ray Tracing](#ray-tracing)
      - [Reflection-aware Ray Tracing](#reflection-aware-ray-tracing)
      - [Refraction-aware Ray Tracing](#refraction-aware-ray-tracing)
    - [Inverse Rendering](#inverse-rendering)
      - [Inverse Rendering for Arbitrary Reflectance](#inverse-rendering-for-arbitrary-reflectance)
  - [Gaussian Splatting](#gaussian-splatting)
    - [Component Decomposition](#component-decomposition)
    - [Ray Tracing](#ray-tracing-1)
    - [Inverse Rendering](#inverse-rendering-1)
- [Datasets](#datasets)
  - [Specular](#specular)
    - [Synthetic](#synthetic)
    - [Real World](#real-world)
  - [Mirrors](#mirrors)
    - [Synthetic](#synthetic-1)
    - [Real World](#real-world-1)
  - [Transparent](#transparent)



# Papers

## 3D Neural Representation
### View-dependent Appearance Modeling
#### Decomposition of Transmitted and Reflected Radiance

**NeRFReN: Neural Radiance Fields With Reflections.** Yuan-Chen Guo, Di Kang, Linchao Bao, Yu He, Song-Hai Zhang. [<a href="...">
  <img src="https://img.shields.io/badge/Paper-CVPR22-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://openaccess.thecvf.com/content/CVPR2022/html/Guo_NeRFReN_Neural_Radiance_Fields_With_Reflections_CVPR_2022_paper.html)  [<a href="...">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>](https://bennyguo.github.io/nerfren)       [<a href="...">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>](https://github.com/bennyguo/nerfren) 




#### Directional Encoding for High-frequency Specularity
**Ref-NeRF: Structured View-Dependent Appearance for Neural Radiance Fields.** Dor Verbin, Peter Hedman, Ben Mildenhall, Todd Zickler, Jonathan T. Barron, Pratul P. Srinivasan. [<a href="...">
  <img src="https://img.shields.io/badge/Paper-CVPR22-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://openaccess.thecvf.com/content/CVPR2022/html/Verbin_Ref-NeRF_Structured_View-Dependent_Appearance_for_Neural_Radiance_Fields_CVPR_2022_paper.html)  [<a href="...">
  <img src="https://img.shields.io/badge/Paper-TPAMI25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://ieeexplore.ieee.org/abstract/document/10416701) [<a href="...">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>](https://dorverbin.github.io/refnerf)    [<a href="...">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>](https://github.com/google-research/multinerf)




### Ray Tracing
#### Reflection-aware Ray Tracing
**Mirror-NeRF: Learning Neural Radiance Fields for Mirrors with Whitted-Style Ray Tracing.** Junyi Zeng, Chong Bao, Rui Chen, Zilong Dong, Guofeng Zhang, Hujun Bao, Zhaopeng Cui. [<a href="...">
  <img src="https://img.shields.io/badge/Paper-MM23-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://dl.acm.org/doi/abs/10.1145/3581783.3611857) [<a href="...">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>](https://zju3dv.github.io/Mirror-NeRF/) [<a href="...">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>](https://github.com/zju3dv/Mirror-NeRF/)

#### Refraction-aware Ray Tracing
**Eikonal Fields for Refractive Novel-View Synthesis.** Mojtaba Bemana, Karol Myszkowski, Jeppe Revall Frisvad, Hans-Peter Seidel, Tobias Ritschel. [<a href="...">
  <img src="https://img.shields.io/badge/Paper-SIGGRAPH22-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://dl.acm.org/doi/abs/10.1145/3581783.3611857) [<a href="...">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>](https://eikonalfield.mpi-inf.mpg.de/) [<a href="...">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>](https://github.com/m-bemana/eikonalfield) 


### Inverse Rendering

#### Inverse Rendering for Arbitrary Reflectance

**TensoIR: Tensorial Inverse Rendering.** Haian Jin, Isabella Liu, Peijia Xu, Xiaoshuai Zhang, Songfang Han, Sai Bi, Xiaowei Zhou, Zexiang Xu, Hao Su. [<a href="...">
  <img src="https://img.shields.io/badge/Paper-CVPR23-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://openaccess.thecvf.com/content/CVPR2023/html/Jin_TensoIR_Tensorial_Inverse_Rendering_CVPR_2023_paper.html) [<a href="...">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>](https://haian-jin.github.io/TensoIR/) [<a href="...">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>](https://github.com/Haian-Jin/TensoIR)

**NeRO: Neural Geometry and BRDF Reconstruction of Reflective Objects from Multiview Images.** Yuan Liu, Peng Wang, Cheng Lin, Xiaoxiao Long, Jiepeng Wang, Lingjie Liu, Taku Komura, Wenping Wang. [<a href="...">
  <img src="https://img.shields.io/badge/Paper-ToG23-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://dl.acm.org/doi/abs/10.1145/3592134)    [<a href="...">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>](https://liuyuan-pal.github.io/NeRO/)        [<a href="...">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>](https://github.com/liuyuan-pal/NeRO)

## Gaussian Splatting
### Component Decomposition 
### Ray Tracing
### Inverse Rendering



# Datasets

## Specular
### Synthetic
**Shiny Blender Dataset** [<a href="...">
  <img src="https://img.shields.io/badge/Paper-CVPR22-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://openaccess.thecvf.com/content/CVPR2022/html/Verbin_Ref-NeRF_Structured_View-Dependent_Appearance_for_Neural_Radiance_Fields_CVPR_2022_paper.html)
[<a href="...">
  <img src="https://img.shields.io/badge/Data-Download-green.svg?logo=google" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://storage.googleapis.com/gresearch/refraw360/ref.zip)

**Glossy Blender Dataset** [<a href="...">
  <img src="https://img.shields.io/badge/Paper-ToG23-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://dl.acm.org/doi/abs/10.1145/3592134) [<a href="..."> <img src="https://img.shields.io/badge/Data-Download-green.svg?logo=googledrive" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://drive.google.com/drive/folders/1arqYrMxfPc7ZOCSwgZxgLjBRDZ_8leGV)


**TensoIR Dataset** [<a href="...">
  <img src="https://img.shields.io/badge/Paper-CVPR23-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://openaccess.thecvf.com/content/CVPR2023/html/Jin_TensoIR_Tensorial_Inverse_Rendering_CVPR_2023_paper.html)  [<a href="..."> <img src="https://img.shields.io/badge/Data-Download-green.svg?logo=zenodo" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://zenodo.org/records/7880113#.ZE68FHZBz18) 

### Real World
**Ref-NeRF Real Dataset** [<a href="...">
  <img src="https://img.shields.io/badge/Paper-CVPR22-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://openaccess.thecvf.com/content/CVPR2022/html/Verbin_Ref-NeRF_Structured_View-Dependent_Appearance_for_Neural_Radiance_Fields_CVPR_2022_paper.html)
[<a href="...">
  <img src="https://img.shields.io/badge/Data-Download-green.svg?logo=google" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://storage.googleapis.com/gresearch/refraw360/ref_real.zip)

**Glossy Real Dataset** [<a href="...">
  <img src="https://img.shields.io/badge/Paper-ToG23-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://dl.acm.org/doi/abs/10.1145/3592134) [<a href="..."> <img src="https://img.shields.io/badge/Data-Download-green.svg?logo=googledrive" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://drive.google.com/drive/folders/1arqYrMxfPc7ZOCSwgZxgLjBRDZ_8leGV)



## Mirrors
### Synthetic
**Mirror-NeRF Synthetic Dataset** [<a href="...">
  <img src="https://img.shields.io/badge/Paper-MM23-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://dl.acm.org/doi/abs/10.1145/3581783.3611857) [<a href="..."> <img src="https://img.shields.io/badge/Data-Download-green.svg?logo=googledrive" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://drive.google.com/drive/folders/1fBeIAI64v5GRoIo7eceGnbqS0sF07YN_)

### Real World
**RFFR Dataset**  [<a href="...">
  <img src="https://img.shields.io/badge/Paper-CVPR22-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://openaccess.thecvf.com/content/CVPR2022/html/Guo_NeRFReN_Neural_Radiance_Fields_With_Reflections_CVPR_2022_paper.html)  [<a href="..."> <img src="https://img.shields.io/badge/Data-Download-green.svg?logo=googledrive" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://drive.google.com/file/d/1UFHdcLgn9wXBcYZVM5qojYP1NNpg5bsS/view)

**Mirror-NeRF Real Dataset** [<a href="...">
  <img src="https://img.shields.io/badge/Paper-MM23-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://dl.acm.org/doi/abs/10.1145/3581783.3611857) [<a href="..."> <img src="https://img.shields.io/badge/Data-Download-green.svg?logo=googledrive" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://drive.google.com/drive/folders/1fBeIAI64v5GRoIo7eceGnbqS0sF07YN_)

## Transparent

**Eikonal Fields Dataset** [<a href="...">
  <img src="https://img.shields.io/badge/Paper-SIGGRAPH22-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>](https://dl.acm.org/doi/abs/10.1145/3581783.3611857) [<a href="...">
  <img src="https://img.shields.io/badge/Data-Download-green.svg" height="15" style="vertical-align:middle" />
</a>](https://eikonalfield.mpi-inf.mpg.de/)