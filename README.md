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

#### **I. Decomposition of Transmitted and Reflected Radiance**

**2022**

**NeRFReN: Neural Radiance Fields With Reflections.** *Yuan-Chen Guo, Di Kang, Linchao Bao, Yu He, Song-Hai Zhang.*
<a href="https://openaccess.thecvf.com/content/CVPR2022/html/Guo_NeRFReN_Neural_Radiance_Fields_With_Reflections_CVPR_2022_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR22-blue" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://bennyguo.github.io/nerfren">
  <img src="https://img.shields.io/badge/Project-Page-yellow" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://github.com/bennyguo/nerfren">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**Neural Transmitted Radiance Fields.** *Chengxuan Zhu, Renjie Wan, Boxin Shi.*
<a href="https://proceedings.neurips.cc/paper_files/paper/2022/hash/fe989bb038b5dcc44181255dd6913e43-Abstract-Conference.html">
  <img src="https://img.shields.io/badge/Paper-NeurIPS22-purple" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://github.com/FreeButUselessSoul/TNeRF">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**2023**

**Looking Through the Glass: Neural Surface Reconstruction Against High Specular Reflections.** *Jiaxiong Qiu, Peng-Tao Jiang, Yifan Zhu, Ze-Xin Yin, Ming-Ming Cheng, Bo Ren.*
<a href="https://openaccess.thecvf.com/content/CVPR2023/html/Qiu_Looking_Through_the_Glass_Neural_Surface_Reconstruction_Against_High_Specular_CVPR_2023_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR23-blue" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://github.com/JiaxiongQ/NeuS-HSR">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**Seeing Through the Glass: Neural 3D Reconstruction of Object Inside a Transparent Container.** *Jinguang Tong, Sundaram Muthu, Fahira Afzal Maken, Chuong Nguyen, Hongdong Li.*
<a href="https://openaccess.thecvf.com/content/CVPR2023/html/Tong_Seeing_Through_the_Glass_Neural_3D_Reconstruction_of_Object_Inside_CVPR_2023_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR23-blue" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://github.com/hirotong/ReNeuS">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**Ref-NeuS: Ambiguity-Reduced Neural Implicit Surface Learning for Multi-View Reconstruction with Reflection.** *Wenhang Ge, Tao Hu, Haoyu Zhao, Shu Liu, Ying-Cong Chen.*
<a href="https://openaccess.thecvf.com/content/ICCV2023/html/Ge_Ref-NeuS_Ambiguity-Reduced_Neural_Implicit_Surface_Learning_for_Multi-View_Reconstruction_with_ICCV_2023_paper.html">
  <img src="https://img.shields.io/badge/Paper-ICCV23-blue" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://g3956.github.io/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="http://github.com/EnVision-Research/Ref-NeuS">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**DE-NeRF: DEcoupled Neural Radiance Fields for View-Consistent Appearance Editing and High-Frequency Environmental Relighting.** *Tong Wu, Jia-Mu Sun, Yu-Kun Lai, Lin Gao.*
<a href="ttps://dl.acm.org/doi/abs/10.1145/3588432.3591483">
  <img src="https://img.shields.io/badge/Paper-SIGGRAPH23-red" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**2024**

**Localised-NeRF: Specular Highlights and Colour Gradient Localising in NeRF.** *Dharmendra Selvaratnam, Dena Bazazian.*
<a href="https://openaccess.thecvf.com/content/CVPR2024W/NRI/html/Selvaratnam_Localised-NeRF_Specular_Highlights_and_Colour_Gradient_Localising_in_NeRF_CVPRW_2024_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR24W-blue" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://github.com/Dharmendra04/Localised-NeRF">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**REFRAME: Reflective Surface Real-Time Rendering for Mobile Devices.** *Chaojie Ji, Yufeng Li, Yiyi Liao.*
<a href="https://link.springer.com/chapter/10.1007/978-3-031-72995-9_14">
  <img src="https://img.shields.io/badge/Paper-ECCV24-003E8C" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://xdimlab.github.io/REFRAME/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://github.com/MARVELOUSJI/REFRAME">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" alt="paper" height="15" style="vertical-align:middle"/>
</a>

---

#### **II. Directional Encoding for High-frequency Specularity**
**2022**

**Ref-NeRF: Structured View-Dependent Appearance for Neural Radiance Fields.** *Dor Verbin, Peter Hedman, Ben Mildenhall, Todd Zickler, Jonathan T. Barron, Pratul P. Srinivasan.*
<a href="https://openaccess.thecvf.com/content/CVPR2022/html/Verbin_Ref-NeRF_Structured_View-Dependent_Appearance_for_Neural_Radiance_Fields_CVPR_2022_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR22-blue" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://ieeexplore.ieee.org/abstract/document/10416701">
  <img src="https://img.shields.io/badge/Paper-TPAMI25-blue" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://dorverbin.github.io/refnerf">
  <img src="https://img.shields.io/badge/Project-Page-yellow" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://github.com/google-research/multinerf">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" alt="paper" height="15" style="vertical-align:middle"/>
</a>


---
---


### Ray Tracing
#### Reflection-aware Ray Tracing
**Mirror-NeRF: Learning Neural Radiance Fields for Mirrors with Whitted-Style Ray Tracing.** Junyi Zeng, Chong Bao, Rui Chen, Zilong Dong, Guofeng Zhang, Hujun Bao, Zhaopeng Cui. 
<a href="https://dl.acm.org/doi/abs/10.1145/3581783.3611857">
  <img src="https://img.shields.io/badge/Paper-MM23-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://zju3dv.github.io/Mirror-NeRF">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/zju3dv/Mirror-NeRF/">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

#### Refraction-aware Ray Tracing
**Eikonal Fields for Refractive Novel-View Synthesis.** Mojtaba Bemana, Karol Myszkowski, Jeppe Revall Frisvad, Hans-Peter Seidel, Tobias Ritschel. 
<a href="https://dl.acm.org/doi/abs/10.1145/3581783.3611857">
  <img src="https://img.shields.io/badge/Paper-SIGGRAPH22-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://eikonalfield.mpi-inf.mpg.de/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/m-bemana/eikonalfield">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>


### Inverse Rendering

#### Inverse Rendering for Arbitrary Reflectance

**TensoIR: Tensorial Inverse Rendering.** Haian Jin, Isabella Liu, Peijia Xu, Xiaoshuai Zhang, Songfang Han, Sai Bi, Xiaowei Zhou, Zexiang Xu, Hao Su. 
<a href="https://openaccess.thecvf.com/content/CVPR2023/html/Jin_TensoIR_Tensorial_Inverse_Rendering_CVPR_2023_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR23-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://haian-jin.github.io/TensoIR/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/Haian-Jin/TensoIR">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**NeRO: Neural Geometry and BRDF Reconstruction of Reflective Objects from Multiview Images.** Yuan Liu, Peng Wang, Cheng Lin, Xiaoxiao Long, Jiepeng Wang, Lingjie Liu, Taku Komura, Wenping Wang. 
<a href="https://dl.acm.org/doi/abs/10.1145/3592134">
  <img src="https://img.shields.io/badge/Paper-ToG23-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://liuyuan-pal.github.io/NeRO/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/liuyuan-pal/NeRO">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

## Gaussian Splatting
### Component Decomposition 
### Ray Tracing
### Inverse Rendering



# Datasets

## Specular
### Synthetic
**Shiny Blender Dataset** 
<a href="https://openaccess.thecvf.com/content/CVPR2022/html/Verbin_Ref-NeRF_Structured_View-Dependent_Appearance_for_Neural_Radiance_Fields_CVPR_2022_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR22-blue" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://ieeexplore.ieee.org/abstract/document/10416701">
  <img src="https://img.shields.io/badge/Paper-TPAMI25-blue" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://storage.googleapis.com/gresearch/refraw360/ref.zip">
  <img src="https://img.shields.io/badge/Data-Download-green.svg?logo=google" alt="Paper" height="15" style="vertical-align:middle" />
</a>

**Glossy Blender Dataset** 
<a href="https://dl.acm.org/doi/abs/10.1145/3592134">
  <img src="https://img.shields.io/badge/Paper-ToG23-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://drive.google.com/drive/folders/1arqYrMxfPc7ZOCSwgZxgLjBRDZ_8leGV"> <img src="https://img.shields.io/badge/Data-Download-green.svg?logo=googledrive" alt="Paper" height="15" style="vertical-align:middle" />
</a>


**TensoIR Dataset** 
<a href="https://openaccess.thecvf.com/content/CVPR2023/html/Jin_TensoIR_Tensorial_Inverse_Rendering_CVPR_2023_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR23-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a><a href="https://zenodo.org/records/7880113#.ZE68FHZBz18"> <img src="https://img.shields.io/badge/Data-Download-green.svg?logo=zenodo" alt="Paper" height="15" style="vertical-align:middle" />
</a>

### Real World
**Ref-NeRF Real Dataset** 
<a href="https://openaccess.thecvf.com/content/CVPR2022/html/Verbin_Ref-NeRF_Structured_View-Dependent_Appearance_for_Neural_Radiance_Fields_CVPR_2022_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR22-blue" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://ieeexplore.ieee.org/abstract/document/10416701">
  <img src="https://img.shields.io/badge/Paper-TPAMI25-blue" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://storage.googleapis.com/gresearch/refraw360/ref_real.zip">
  <img src="https://img.shields.io/badge/Data-Download-green.svg?logo=google" alt="Paper" height="15" style="vertical-align:middle" />
</a>

**Glossy Real Dataset** <a href="https://dl.acm.org/doi/abs/10.1145/3592134">
  <img src="https://img.shields.io/badge/Paper-ToG23-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://drive.google.com/drive/folders/1arqYrMxfPc7ZOCSwgZxgLjBRDZ_8leGV"> <img src="https://img.shields.io/badge/Data-Download-green.svg?logo=googledrive" alt="Paper" height="15" style="vertical-align:middle" />
</a>



## Mirrors
### Synthetic
**Mirror-NeRF Synthetic Dataset** <a href="https://dl.acm.org/doi/abs/10.1145/3581783.3611857">
  <img src="https://img.shields.io/badge/Paper-MM23-red" alt="Paper" height="15" style="vertical-align:middle" />
</a><a href="https://drive.google.com/drive/folders/1fBeIAI64v5GRoIo7eceGnbqS0sF07YN_"> <img src="https://img.shields.io/badge/Data-Download-green.svg?logo=googledrive" alt="Paper" height="15" style="vertical-align:middle" />
</a>

### Real World
**RFFR Dataset**  <a href="https://openaccess.thecvf.com/content/CVPR2022/html/Guo_NeRFReN_Neural_Radiance_Fields_With_Reflections_CVPR_2022_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR22-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a><a href="https://drive.google.com/file/d/1UFHdcLgn9wXBcYZVM5qojYP1NNpg5bsS/view"> <img src="https://img.shields.io/badge/Data-Download-green.svg?logo=googledrive" alt="Paper" height="15" style="vertical-align:middle" />
</a>

**Mirror-NeRF Real Dataset** <a href="https://dl.acm.org/doi/abs/10.1145/3581783.3611857">
  <img src="https://img.shields.io/badge/Paper-MM23-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://drive.google.com/drive/folders/1fBeIAI64v5GRoIo7eceGnbqS0sF07YN_"> <img src="https://img.shields.io/badge/Data-Download-green.svg?logo=googledrive" alt="Paper" height="15" style="vertical-align:middle" />
</a>

## Transparent

**Eikonal Fields Dataset** <a href="https://dl.acm.org/doi/abs/10.1145/3581783.3611857">
  <img src="https://img.shields.io/badge/Paper-SIGGRAPH22-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://eikonalfield.mpi-inf.mpg.de/">
  <img src="https://img.shields.io/badge/Data-Download-green.svg" height="15" style="vertical-align:middle" />
</a>

