# Awesome 3D Non-Lambertian List

> A curated list of papers and resources linked to **3D Reconstruction and Novel View Synthesis on Non-Lambertian Surfaces**.

# ReadMe
> The categorization of methods for handling 3D non-Lambertian surfaces is inherently subjective, and no single taxonomy can be considered definitive. To provide a clearer chronological perspective, this repository first groups methods according to their underlying scene representations, namely neural representations and Gaussian Splatting (GS)-based methods. For each type of scene representation, we further organize the manuscripts into three categories:
(i) view-dependent appearance modeling and component decomposition, (ii) ray tracing, and (iii) inverse rendering.

> Notes:
> 1. Inverse rendering can be regarded as a physically grounded form of view-dependent appearance modeling and component decomposition, as it jointly accounts for material properties, illumination, and related factors.
> 2. Manuscripts that combine ray tracing with inverse rendering are categorized under the Inverse Rendering section.
> 3. In the Inverse Rendering section, we also include several representative methods that consider materials with arbitrary reflectance. Although these methods are not exclusively designed for non-Lambertian surfaces, they are partially applicable to such cases and may serve as foundations for subsequent work.
> 4. When a manuscript has been accepted by a journal (conference), and an official early-access, open-access, or proceedings version is available, we no longer provide a link to its arXiv preprint.

# Contents

- [Awesome 3D Non-Lambertian List](#awesome-3d-non-lambertian-list)
- [Contents](#contents)
- [Papers](#papers)
  - [3D Neural Representation](#3d-neural-representation)
    - [View-dependent Appearance Modeling](#view-dependent-appearance-modeling)
      - [Decomposition of Transmitted and Reflected Radiance](#i-decomposition-of-transmitted-and-reflected-radiance)
      - [Directional Encoding for High-frequency Specularity](#ii-directional-encoding-for-high-frequency-specularity)
      - [Other Methods](#iii-other-methods)
    - [Ray Tracing](#ray-tracing)
      - [Reflection-aware Ray Tracing](#i-reflection-aware-ray-tracing)
      - [Refraction-aware Ray Tracing](#ii-refraction-aware-ray-tracing)
    - [Inverse Rendering](#inverse-rendering)
      - [Inverse Rendering for Surfaces of Arbitrary Reflectance](#i-inverse-rendering-for-surfaces-of-arbitrary-reflectance)
      - [Approximation of Light Transport, Joint Optimization of Geometry and Materials for Non-Lambertian Surfaces](#ii-approximation-of-light-transport-joint-optimization-of-geometry-and-materials-for-non-lambertian-surfaces)
      - [Multi-Stage Factorization and Optimization for Non-Lambertian Surfaces](#iii-multi-stage-factorization-and-optimization-for-non-lambertian-surfaces)
    - [Others](#others)
  - [Gaussian Splatting](#gaussian-splatting)
    - [View-dependent Component Decomposition](#view-dependent-component-decomposition)
      - [Decomposed Representations of Appearance](#i-decomposed-representations-of-appearance)
      - [Decomposed Appearance from Geometry](#ii-decomposed-appearance-from-geometry)
    - [Ray Tracing for Enhanced Rasterization](#ray-tracing-for-enhanced-rasterization)
    - [Inverse Rendering](#inverse-rendering-1)
      - [Inverse Rendering for Surfaces of Arbitrary Reflectance](#i-inverse-rendering-for-surfaces-of-arbitrary-reflectance-1)
      - [Environment-based Approximation of Illumination for Non-Lambertian Surfaces](#ii-environment-based-approximation-of-illumination-for-non-lambertian-surfaces)
      - [Ray Tracing-augmented Inverse Rendering for Non-Lambertian Surfaces](#iii-ray-tracing-augmented-inverse-rendering-for-non-lambertian-surfaces)
- [Commonly Used Datasets](#commonly-used-datasets)
  - [Specular](#specular)
    - [Synthetic](#synthetic)
    - [Real World](#real-world)
  - [Mirrors](#mirrors)
    - [Synthetic](#synthetic-1)
    - [Real World](#real-world-1)
  - [Transparent](#transparent)



# Papers

## 3D Neural Representation
### <span style="color: lightgreen;">View-dependent Appearance Modeling</span>

#### **I. Decomposition of Transmitted and Reflected Radiance**

>**2022**

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

>**2023**

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


**MS-NeRF: Multi-Space Neural Radiance Fields.** (Multi-Space Neural Radiance Fields.) *Ze-Xin Yin, Peng-Yi Jiao, Jiaxiong Qiu, Ming-Ming Cheng, Bo Ren.*
<a href="https://openaccess.thecvf.com/content/CVPR2023/html/Yin_Multi-Space_Neural_Radiance_Fields_CVPR_2023_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR23-blue" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://ieeexplore.ieee.org/abstract/document/10878467/">
  <img src="https://img.shields.io/badge/Paper-TPAMI25-blue" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://zx-yin.github.io/msnerf">
  <img src="https://img.shields.io/badge/Project-Page-yellow" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://github.com/ZX-Yin/ms-nerf">
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

**NeRF-DS: Neural Radiance Fields for Dynamic Specular Objects.** *Zhiwen Yan, Chen Li, Gim Hee Lee.*
<a href="https://openaccess.thecvf.com/content/CVPR2023/html/Yan_NeRF-DS_Neural_Radiance_Fields_for_Dynamic_Specular_Objects_CVPR_2023_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR23-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://jokeryan.github.io/projects/nerf-ds/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/JokerYan/NeRF-DS">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

>**2024**

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

>**2025**

**NeRF-THO: Neural Radiance Fields for Transparent and Highlighted Objects.** *Chenyu Tian, Wentao Hu, Huafeng Ding, Long Wen.*
<a href="https://ieeexplore.ieee.org/abstract/document/11124338">
  <img src="https://img.shields.io/badge/Paper-TII25-blue" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**NeRFs are Mirror Detectors: Using Structural Similarity for Multi-View Mirror Scene Reconstruction with 3D Surface Primitives.** *Leif Van Holland, Michael Weinmann, Jan U. Müller, Patrick Stotko, Reinhard Klein.*
<a href="https://ieeexplore.ieee.org/abstract/document/10943830/">
  <img src="https://img.shields.io/badge/Paper-WACV25-blue" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://cg.cs.uni-bonn.de/publication/holland-2025-nerfs-are-mirror-detectors">
  <img src="https://img.shields.io/badge/Project-Page-yellow" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://github.com/vc-bonn/nerfs-are-mirror-detectors">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**αSurf: Implicit Surface Reconstruction for Semi-Transparent and Thin Objects with Decoupled Geometry and Opacity.** *Tianhao Wu, Hanxue Liang, Fangcheng Zhong, Gernot Riegler, Shimon Vainer, Jiankang Deng.*
<a href="https://ieeexplore.ieee.org/abstract/document/11125620/">
  <img src="https://img.shields.io/badge/Paper-3DV25-blue" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://alphasurf.netlify.app/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://github.com/ChikaYan/alphasurf">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**AniSDF: Fused-Granularity Neural Surfaces with Anisotropic Encoding for High-Fidelity 3D Reconstruction.** *Jingnan Gao, Zhuo Chen, Xiaokang Yang, Yichao Yan.*
<a href="https://arxiv.org/abs/2410.01202">
  <img src="https://img.shields.io/badge/arXiv-2410.01202-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://openreview.net/forum?id=v1f6c7wVBm/">
  <img src="https://img.shields.io/badge/OpenReview-ICLR25-darkred" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://g-1nonly.github.io/AniSDF_Website/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://github.com/G-1nOnly/AniSDF">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" alt="paper" height="15" style="vertical-align:middle"/>
</a>




------

#### **II. Directional Encoding for High-frequency Specularity**

>**2022**

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

>**2023**

**Ref-DVGO: Reflection-Aware Direct Voxel Grid Optimization for an Improved Quality-Efficiency Trade-Off in Reflective Scene Reconstruction.** *Georgios Kouros, Minye Wu, Shubham Shrivastava, Sushruth Nagesh, Punarjay Chakravarty, Tinne Tuytelaars.*
<a href="https://arxiv.org/abs/2308.08530">
  <img src="https://img.shields.io/badge/arXiv-2308.08530-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://sites.google.com/view/iccv23trickyworkshop">
  <img src="https://img.shields.io/badge/Site-ICCV23W(TRICKY)-blue" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://github.com/gkouros/ref-dvgo">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" alt="paper" height="15" style="vertical-align:middle"/>
</a>

>**2024**

**SpecNeRF: Gaussian Directional Encoding for Specular Reflections.** *Li Ma, Vasu Agrawal, Haithem Turki, Changil Kim, Chen Gao, Pedro Sander, Michael Zollhöfer, Christian Richardt.*
<a href="https://openaccess.thecvf.com/content/CVPR2024/html/Ma_SpecNeRF_Gaussian_Directional_Encoding_for_Specular_Reflections_CVPR_2024_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR24-blue" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://limacv.github.io/SpecNeRF_web/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**Neural Directional Encoding for Efficient and Accurate View-Dependent Appearance Modeling.** *Liwen Wu, Sai Bi, Zexiang Xu, Fujun Luan, Kai Zhang, Iliyan Georgiev, Kalyan Sunkavalli, Ravi Ramamoorthi.*
<a href="https://openaccess.thecvf.com/content/CVPR2024/html/Wu_Neural_Directional_Encoding_for_Efficient_and_Accurate_View-Dependent_Appearance_Modeling_CVPR_2024_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR24-blue" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://lwwu2.github.io/nde/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://github.com/lwwu2/nde">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

------

#### **III. Other Methods**

>2023

**ABLE-NeRF: Attention-Based Rendering With Learnable Embeddings for Neural Radiance Field.** *Zhe Jun Tang, Tat-Jen Cham, Haiyu Zhao.*
<a href="https://openaccess.thecvf.com/content/CVPR2023/html/Tang_ABLE-NeRF_Attention-Based_Rendering_With_Learnable_Embeddings_for_Neural_Radiance_Field_CVPR_2023_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR23-blue" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://github.com/TangZJ/able-nerf">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

>2025

**Normal-NeRF: Ambiguity-Robust Normal Estimation for Highly Reflective Scenes.** *Ji Shi, Xianghua Ying, Ruohao Guo, Bowei Xing, Wenzhen Yue.*
<a href="https://ojs.aaai.org/index.php/AAAI/article/view/32737">
  <img src="https://img.shields.io/badge/Paper-AAAI25-lightblue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/sjj118/Normal-NeRF">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>




---
---


### <span style="color: lightblue;">Reflection and Refraction Ray Tracing</span>
#### I. Reflection-aware Ray Tracing

>2023

**Mirror-NeRF: Learning Neural Radiance Fields for Mirrors with Whitted-Style Ray Tracing.** *Junyi Zeng, Chong Bao, Rui Chen, Zilong Dong, Guofeng Zhang, Hujun Bao, Zhaopeng Cui.* 
<a href="https://dl.acm.org/doi/abs/10.1145/3581783.3611857">
  <img src="https://img.shields.io/badge/Paper-MM23-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://zju3dv.github.io/Mirror-NeRF">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/zju3dv/Mirror-NeRF/">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

>2024

**TraM-NeRF: Tracing Mirror and Near-Perfect Specular Reflections Through Neural Radiance Fields.** *Leif Van Holland, Ruben Bliersbach, Jan U. Müller, Patrick Stotko, Reinhard Klein.*
<a href="https://onlinelibrary.wiley.com/doi/full/10.1111/cgf.15163
">
  <img src="https://img.shields.io/badge/Paper-CGF24-darkgray" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://cg.cs.uni-bonn.de/publication/holland-2024-tram-nerf">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/Rubikalubi/TraM-NeRF">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**Planar Reflection-Aware Neural Radiance Fields.** *Chen Gao, Yipeng Wang, Changil Kim, Jia-Bin Huang, Johannes Kopf.*
<a href="https://dl.acm.org/doi/full/10.1145/3680528.3687560">
  <img src="https://img.shields.io/badge/Paper-SIGGRAPH_Asia24-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>

**NeRF-Casting: Improved View-Dependent Appearance with Consistent Reflections.** *Dor Verbin, Pratul P. Srinivasan, Peter Hedman, Ben Mildenhall, Benjamin Attal, Richard Szeliski, Jonathan T. Barron.*
<a href="https://dl.acm.org/doi/full/10.1145/3680528.3687585">
  <img src="https://img.shields.io/badge/Paper-SIGGRAPH_Asia24-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://dorverbin.github.io/nerf-casting/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>

>2025

**RS-SpecSDF: Reflection-supervised Surface Reconstruction and Material Estimation for Specular Indoor Scenes.** *Dong-Yu Chen, Hao-Xiang Chen, Qun-Ce Xu, Tai-Jiang Mu.* 
<a href="https://www.sciencedirect.com/science/article/pii/S1524070325000244">
  <img src="https://img.shields.io/badge/Paper-GMOD25-orange" alt="Paper" height="15" style="vertical-align:middle" />
</a>

---

#### II. Refraction-aware Ray Tracing

>2022

**LB-NERF: Light Bending Neural Radiance Fields for Transparent Medium.** *Taku Fujitomi, Ken Sakurada, Ryuhei Hamaguchi, Hidehiko Shishido, Masaki Onishi, Yoshinari Kameda.*
<a href="https://ieeexplore.ieee.org/abstract/document/9897642">
  <img src="https://img.shields.io/badge/Paper-ICIP22-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>

**Eikonal Fields for Refractive Novel-View Synthesis.** *Mojtaba Bemana, Karol Myszkowski, Jeppe Revall Frisvad, Hans-Peter Seidel, Tobias Ritschel.* 
<a href="https://dl.acm.org/doi/abs/10.1145/3581783.3611857">
  <img src="https://img.shields.io/badge/Paper-SIGGRAPH22-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://eikonalfield.mpi-inf.mpg.de/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/m-bemana/eikonalfield">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**Sampling Neural Radiance Fields for Refractive Objects.** *Jen-I Pan, Jheng-Wei Su, Kai-Wen Hsiao, Ting-Yu Yen, Hung-Kuo Chu.*
<a href="https://dl.acm.org/doi/abs/10.1145/3550340.3564234">
  <img src="https://img.shields.io/badge/Paper-SIGGRAPH_Asia22TC-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://alexkeroro86.github.io/SampleNeRFRO/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/alexkeroro86/SampleNeRFRO">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

>2023

**NeRRF: 3D Reconstruction and View Synthesis for Transparent and Specular Objects with Neural Refractive-Reflective Fields.** *Xiaoxue Chen, Junchen Liu, Hao Zhao, Guyue Zhou, Ya-Qin Zhang.*
<a href="https://arxiv.org/abs/2309.13039">
  <img src="https://img.shields.io/badge/arXiv-2309.13039-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://github.com/JunchenLiu77/NeRRF">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>


**NeReF: Neural Refractive Field for Fluid Surface Reconstruction and Rendering.** *Ziyu Wang, Wei Yang; Junming Cao; Qiang Hu; Lan Xu; Junqing Yu.*
<a href="https://ieeexplore.ieee.org/abstract/document/10233838">
  <img src="https://img.shields.io/badge/Paper-ICCP23-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>

**NeRFrac: Neural Radiance Fields through Refractive Surface.** *Yifan Zhan, Shohei Nobuhara, Ko Nishino, Yinqiang Zheng.*
<a href="https://openaccess.thecvf.com/content/ICCV2023/html/Zhan_NeRFrac_Neural_Radiance_Fields_through_Refractive_Surface_ICCV_2023_paper.html">
  <img src="https://img.shields.io/badge/Paper-ICCV23-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/Yifever20002/NeRFrac">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>


**NeTO: Neural Reconstruction of Transparent Objects with Self-Occlusion Aware Refraction-Tracing.** *Zongcheng Li, Xiaoxiao Long, Yusen Wang, Tuo Cao, Wenping Wang, Fei Luo, Chunxia Xiao.*
<a href="https://openaccess.thecvf.com/content/ICCV2023/html/Li_NeTONeural_Reconstruction_of_Transparent_Objects_with_Self-Occlusion_Aware_Refraction-Tracing_ICCV_2023_paper.html">
  <img src="https://img.shields.io/badge/Paper-ICCV23-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://www.xxlong.site/NeTO/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/xxlong0/NeTO">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**NEMTO: Neural Environment Matting for Novel View and Relighting Synthesis of Transparent Objects.** *Dongqing Wang, Tong Zhang, Sabine Süsstrunk.*
<a href="https://openaccess.thecvf.com/content/ICCV2023/html/Wang_NEMTO_Neural_Environment_Matting_for_Novel_View_and_Relighting_Synthesis_ICCV_2023_paper.html">
  <img src="https://img.shields.io/badge/Paper-ICCV23-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://ivrl.github.io/NEMTO//">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/IVRL/NEMTO">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

>2024

**Refracting Once is Enough: Neural Radiance Fields for Novel-View Synthesis of Real Refractive Objects.** *Xiaoqian Liang, Jianji Wang, Yuanliang Lu, Xubin Duan, Xichun Liu, Nanning Zheng.*
<a href="https://dl.acm.org/doi/abs/10.1145/3652583.3658000">
  <img src="https://img.shields.io/badge/Paper-ICMR24-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/Yubel426/RoseNeRF">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**REF<sup>2</sup>-NeRF: Reflection and Refraction aware Neural Radiance Field.** *Wooseok Kim, Taiki Fukiage, Takeshi Oishi.*
<a href="https://ieeexplore.ieee.org/abstract/document/10801830">
  <img src="https://img.shields.io/badge/Paper-IROS24-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>

**Ray Deformation Networks for Novel View Synthesis of Refractive Objects.** *Weijian Deng, Dylan Campbell, Chunyi Sun, Shubham Kanitkar, Matthew Shaffer, Stephen Gould.*
<a href="https://openaccess.thecvf.com/content/WACV2024/html/Deng_Ray_Deformation_Networks_for_Novel_View_Synthesis_of_Refractive_Objects_WACV_2024_paper.html">
  <img src="https://img.shields.io/badge/Paper-WACV24-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>

**Differentiable Neural Surface Refinement for Modeling Transparent Objects.** *Weijian Deng, Dylan Campbell, Chunyi Sun, Shubham Kanitkar, Matthew E. Shaffer, Stephen Gould.*
<a href="https://openaccess.thecvf.com/content/CVPR2024/html/Deng_Differentiable_Neural_Surface_Refinement_for_Modeling_Transparent_Objects_CVPR_2024_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR24-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://tnsr.rios.ai/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/rios/TNSR">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

>2025

**Efficient Multi-Bounce Ray Tracing for Specular and Transparent Materials in NeRF.** *Haozhe Liu, Yu Wei Tan, Anand Bhojan.*
<a href="https://ieeexplore.ieee.org/abstract/document/10896123">
  <img src="https://img.shields.io/badge/Paper-AIxVR25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>


**An Index of Refraction Adaptive Neural Refractive Radiance Field for Transparent Scenes.** *Jiangnan Wei, Ziyi Yue, Shuai Li, Zhiqi Cheng, Zhouhui Lian, Mengxiao Song, Yinqian Cheng, Hongying Zhao.*
<a href="https://www.mdpi.com/2079-9292/14/6/1073">
  <img src="https://img.shields.io/badge/Paper-Electronics25-darkgreen" alt="Paper" height="15" style="vertical-align:middle" />
</a>


---
---


### <span style="color: lightyellow;">Inverse Rendering</span>

#### I. Inverse Rendering for Surfaces of Arbitrary Reflectance

>2020

**Neural Reflectance Fields for Appearance Acquisition.** *Sai Bi, Zexiang Xu, Pratul Srinivasan, Ben Mildenhall, Kalyan Sunkavalli, Miloš Hašan, Yannick Hold-Geoffroy, David Kriegman, Ravi Ramamoorthi.*
<a href="https://arxiv.org/abs/2008.03824">
  <img src="https://img.shields.io/badge/arXiv-2008.03824-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**Deep Reflectance Volumes: Relightable Reconstructions from Multi-view Photometric Images.**
*Sai Bi, Zexiang Xu, Kalyan Sunkavalli, Miloš Hašan, Yannick Hold-Geoffroy, David Kriegman, Ravi Ramamoorthi.*
<a href="https://link.springer.com/chapter/10.1007/978-3-030-58580-8_18">
  <img src="https://img.shields.io/badge/Paper-ECCV20-003E8C" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**Multiview Neural Surface Reconstruction by Disentangling Geometry and Appearance.**
*Lior Yariv, Yoni Kasten, Dror Moran, Meirav Galun, Matan Atzmon, Basri Ronen, Yaron Lipman.*
<a href="https://proceedings.neurips.cc/paper/2020/hash/1a77befc3b608d6ed363567685f70e1e-Abstract.html">
  <img src="https://img.shields.io/badge/Paper-NeurIPS20-purple" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://lioryariv.github.io/idr/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/lioryariv/idr">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>


>2021

**NeRD: Neural Reflectance Decomposition From Image Collections.** *Mark Boss, Raphael Braun, Varun Jampani, Jonathan T. Barron, Ce Liu, Hendrik P.A. Lensch.*
<a href="https://openaccess.thecvf.com/content/ICCV2021/html/Boss_NeRD_Neural_Reflectance_Decomposition_From_Image_Collections_ICCV_2021_paper.html">
  <img src="https://img.shields.io/badge/Paper-ICCV21-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://markboss.me/publication/2021-nerd/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/cgtuebingen/NeRD-Neural-Reflectance-Decomposition">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**PhySG: Inverse Rendering With Spherical Gaussians for Physics-Based Material Editing and Relighting.** *Kai Zhang, Fujun Luan, Qianqian Wang, Kavita Bala, Noah Snavely.*
<a href="https://openaccess.thecvf.com/content/CVPR2021/html/Zhang_PhySG_Inverse_Rendering_With_Spherical_Gaussians_for_Physics-Based_Material_Editing_CVPR_2021_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR21-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://kai-46.github.io/PhySG-website/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/Kai-46/PhySG">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**NeRFactor: neural factorization of shape and reflectance under an unknown illumination.**
*Xiuming Zhang, Pratul P. Srinivasan, Boyang Deng, Paul Debevec, William T. Freeman, Jonathan T. Barron.*
<a href="https://dl.acm.org/doi/abs/10.1145/3478513.3480496">
  <img src="https://img.shields.io/badge/Paper-ToG21-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://xiuming.info/projects/nerfactor/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/google/nerfactor">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

>2022

**Modeling Indirect Illumination for Inverse Rendering.** *Yuanqing Zhang, Jiaming Sun, Xingyi He, Huan Fu, Rongfei Jia, Xiaowei Zhou.*
<a href="https://openaccess.thecvf.com/content/CVPR2022/html/Zhang_Modeling_Indirect_Illumination_for_Inverse_Rendering_CVPR_2022_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR22-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://zju3dv.github.io/invrender/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/zju3dv/invrender">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

>2023

**TensoIR: Tensorial Inverse Rendering.** *Haian Jin, Isabella Liu, Peijia Xu, Xiaoshuai Zhang, Songfang Han, Sai Bi, Xiaowei Zhou, Zexiang Xu, Hao Su.* 
<a href="https://openaccess.thecvf.com/content/CVPR2023/html/Jin_TensoIR_Tensorial_Inverse_Rendering_CVPR_2023_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR23-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://haian-jin.github.io/TensoIR/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/Haian-Jin/TensoIR">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**NeMF: Inverse Volume Rendering with Neural Microflake Field.** *Youjia Zhang, Teng Xu, Junqing Yu, Yuteng Ye, Yanqing Jing, Junle Wang, Jingyi Yu, Wei Yang.*
<a href="https://openaccess.thecvf.com/content/ICCV2023/html/Zhang_NeMF_Inverse_Volume_Rendering_with_Neural_Microflake_Field_ICCV_2023_paper.html">
  <img src="https://img.shields.io/badge/Paper-ICCV23-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://youjiazhang.github.io/NeMF/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/YoujiaZhang/NeMF">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>


>2024

**TensoSDF: Roughness-aware Tensorial Representation for Robust Geometry and Material Reconstruction.** *Jia Li, Lu Wang, Lei Zhang, Beibei Wang.*
<a href="https://dl.acm.org/doi/abs/10.1145/3658211">
  <img src="https://img.shields.io/badge/Paper-ToG24-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://riga2.github.io/tensosdf/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/Riga2/TensoSDF">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**UniSDF: Unifying Neural Representations for High-Fidelity 3D Reconstruction of Complex Scenes with Reflections.** *Fangjinhua Wang, Marie-Julie Rakotosaona, Michael Niemeyer, Richard Szeliski, Marc Pollefeys, Federico Tombari.*
<a href="https://proceedings.neurips.cc/paper_files/paper/2024/hash/05b12f103c9e613efc4c85674cdc9066-Abstract-Conference.html">
  <img src="https://img.shields.io/badge/Paper-NeurIPS24-purple" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://fangjinhuawang.github.io/UniSDF/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>

>2025

**TensoFlow: Tensorial Flow-based Sampler for Inverse Rendering.** *Chun Gu, Xiaofei Wei, Li Zhang, Xiatian Zhu.*
<a href="https://openaccess.thecvf.com/content/CVPR2025/html/Gu_TensoFlow_Tensorial_Flow-based_Sampler_for_Inverse_Rendering_CVPR_2025_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/fudan-zvg/tensoflow">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

---

#### II. Approximation of Light Transport, Joint Optimization of Geometry and Materials for Non-Lambertian Surfaces

>2021

**NeRV: Neural Reflectance and Visibility Fields for Relighting and View Synthesis.** *Pratul P. Srinivasan, Boyang Deng, Xiuming Zhang, Matthew Tancik, Ben Mildenhall, Jonathan T. Barron.*
<a href="https://openaccess.thecvf.com/content/CVPR2021/html/Srinivasan_NeRV_Neural_Reflectance_and_Visibility_Fields_for_Relighting_and_View_CVPR_2021_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR21-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://pratulsrinivasan.github.io/nerv/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>

**Neural Ray-Tracing: Learning Surfaces and Reflectance for Relighting and View Synthesis.** *Julian Knodt, Joe Bartusek, Seung-Hwan Baek, Felix Heide.*
<a href="https://arxiv.org/abs/2104.13562">
  <img src="https://img.shields.io/badge/arXiv-2104.13562-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://github.com/princeton-computational-imaging/neural_raytracing">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>


>2022

**Neural Point Catacaustics for Novel-View Synthesis of Reflections.** *Georgios Kopanas, Thomas Leimkühler, Gilles Rainer, Clément Jambon, George Drettakis.*
<a href="https://dl.acm.org/doi/abs/10.1145/3550454.3555497">
  <img src="https://img.shields.io/badge/Paper-ToG22-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://repo-sam.inria.fr/fungraph/neural_catacaustics/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://gitlab.inria.fr/fungraph/neural-catacaustics">
  <img src="https://img.shields.io/badge/GitLab-Repo-blue?logo=gitlab" height="15" style="vertical-align:middle" />
</a>

>2023

**ENVIDR: Implicit Differentiable Renderer with Neural Environment Lighting.** *Ruofan Liang, Huiting Chen, Chunlin Li, Fan Chen, Selvakumar Panneer, Nandita Vijaykumar.*
<a href="https://openaccess.thecvf.com/content/ICCV2023/html/Liang_ENVIDR_Implicit_Differentiable_Renderer_with_Neural_Environment_Lighting_ICCV_2023_paper.html">
  <img src="https://img.shields.io/badge/Paper-ICCV23-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://nexuslrf.github.io/ENVIDR/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/nexuslrf/ENVIDR">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**Neural Microfacet Fields for Inverse Rendering.** *Alexander Mai, Dor Verbin, Falko Kuester, Sara Fridovich-Keil.*
<a href="https://openaccess.thecvf.com/content/ICCV2023/html/Mai_Neural_Microfacet_Fields_for_Inverse_Rendering_ICCV_2023_paper.html">
  <img src="https://img.shields.io/badge/Paper-ICCV23-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://half-potato.gitlab.io/nmf/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/half-potato/nmf">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**NeILF++: Inter-Reflectable Light Fields for Geometry and Material Estimation.** *Jingyang Zhang, Yao Yao, Shiwei Li, Jingbo Liu, Tian Fang, David McKinnon, Yanghai Tsin, Long Quan.*
<a href="https://openaccess.thecvf.com/content/ICCV2023/html/Zhang_NeILF_Inter-Reflectable_Light_Fields_for_Geometry_and_Material_Estimation_ICCV_2023_paper.html">
  <img src="https://img.shields.io/badge/Paper-ICCV23-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://yoyo000.github.io/NeILF_pp/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/apple/ml-neilfpp">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>


>2024

**PBIR-NIE: Glossy Object Capture under Non-Distant Lighting.** *Guangyan Cai, Fujun Luan, Miloš Hašan, Kai Zhang, Sai Bi, Zexiang Xu, Iliyan Georgiev, Shuang Zhao.*
<a href="https://arxiv.org/abs/2408.06878">
  <img src="https://img.shields.io/badge/arXiv-2408.06878-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://github.com/GuangyanCai/pbir-nie">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**Multi-times Monte Carlo Rendering for Inter-reflection Reconstruction.** *Tengjie Zhu, Zhuo Chen, Jingnan Gao, Yichao Yan, Xiaokang Yang.*
<a href="https://proceedings.neurips.cc/paper_files/paper/2024/hash/e7c3ac813288e4aff606c24e59a8410a-Abstract-Conference.html">
  <img src="https://img.shields.io/badge/Paper-NeurIPS24-purple" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://zhutengjie.github.io/Ref-MC2/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/zhutengjie/Ref-MC2-Code">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>


>2025

**PBR-NeRF: Inverse Rendering with Physics-Based Neural Fields.** *Sean Wu, Shamik Basu, Tim Broedermann, Luc Van Gool, Christos Sakaridis.*
<a href="https://openaccess.thecvf.com/content/CVPR2025/html/Wu_PBR-NeRF_Inverse_Rendering_with_Physics-Based_Neural_Fields_CVPR_2025_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/s3anwu/pbrnerf">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

---

#### III. Multi-stage Factorization and Optimization for Non-Lambertian Surfaces


>2023

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

**Neural-PBIR Reconstruction of Shape, Material, and Illumination.** *Cheng Sun, Guangyan Cai, Zhengqin Li, Kai Yan, Cheng Zhang, Carl Marshall, Jia-Bin Huang, Shuang Zhao, Zhao Dong.*
<a href="https://openaccess.thecvf.com/content/ICCV2023/html/Sun_Neural-PBIR_Reconstruction_of_Shape_Material_and_Illumination_ICCV_2023_paper.html">
  <img src="https://img.shields.io/badge/Paper-ICCV23-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://neural-pbir.github.io/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/facebookresearch/DigitalTwinCatalog/">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>



>2024

**Inverse Rendering of Glossy Objects via the Neural Plenoptic Function and Radiance Fields.** *Haoyuan Wang, Wenbo Hu, Lei Zhu, Rynson W.H. Lau.*
<a href="https://openaccess.thecvf.com/content/CVPR2024/html/Wang_Inverse_Rendering_of_Glossy_Objects_via_the_Neural_Plenoptic_Function_CVPR_2024_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR24-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://www.whyy.site/paper/nep">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/onpix/NeP">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>


**NeuralTO: Neural Reconstruction and View Synthesis of Translucent Objects.** *Yuxiang Cai, Jiaxiong Qiu, Zhong Li, Bo Ren.*
<a href="https://dl.acm.org/doi/abs/10.1145/3658186">
  <img src="https://img.shields.io/badge/Paper-ToG24-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/YuiCtwo/JNeuralTO">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**NU-NeRF: Neural Reconstruction of Nested Transparent Objects with Uncontrolled Capture Environment.** *Jia-Mu Sun, Tong Wu, Ling-Qi Yan, Lin Gao.*
<a href="https://dl.acm.org/doi/abs/10.1145/3687757">
  <img src="https://img.shields.io/badge/Paper-ToG24-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="http://geometrylearning.com/NU-NeRF/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/78ij/NU-NeRF">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>


>2025

**RISE-SDF: A Relightable Information-Shared Signed Distance Field for Glossy Object Inverse Rendering.** *Deheng Zhang, Jingyu Wang, Shaofei Wang, Marko Mihajlovic, Sergey Prokudin, Hendrik P.A. Lensch.*
<a href="https://ieeexplore.ieee.org/abstract/document/11125617">
  <img src="https://img.shields.io/badge/Paper-3DV25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://dehezhang2.github.io/RISE-SDF/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/dehezhang2/RISE-SDF">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>


**Hash-NURF: Efficient Nested Transparent Object Reconstruction Using Multi-Resolution Hash Encoding.** *Fan Gao, Yibo Zhao, Youcheng Cai, Ligang Liu.*
<a href="https://www.researchsquare.com/article/rs-7805209/v1">
  <img src="https://img.shields.io/badge/Preprint-UnderReview-gray" alt="Paper" height="15" style="vertical-align:middle" />
</a>

**Factored-NeuS: Reconstructing Surfaces, Illumination, and Materials of Possibly Glossy Objects.** *Yue Fan, Ningjing Fan, Ivan Skorokhodov, Oleg Voynov, Savva Ignatyev, Evgeny Burnaev, Peter Wonka, Yiqun Wang.*
<a href="https://openaccess.thecvf.com/content/CVPR2025/html/Fan_Factored-NeuS_Reconstructing_Surfaces_Illumination_and_Materials_of_Possibly_Glossy_Objects_CVPR_2025_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://yiqun-wang.github.io/Factored-NeuS/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/yiqun-wang/Factored-NeuS">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>


---
---

### Others

>2024

**From Transparent to Opaque: Rethinking Neural Implicit Surfaces with α-NeuS.** *Haoran Zhang, Junkai Deng, Xuhui Chen, Fei Hou, Wencheng Wang, Hong Qin, Chen Qian, Ying He.*
<a href="https://proceedings.neurips.cc/paper_files/paper/2024/hash/3173c427cb4ed2d5eaab029c17f221ae-Abstract-Conference.html">
  <img src="https://img.shields.io/badge/Paper-NeurIPS24-purple" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://lcs.ios.ac.cn/~houf/pages/alphaneus/index.html">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/728388808/alpha-NeuS">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>


---
---

## Gaussian Splatting

### View-dependent Component Decomposition 

#### I. Decomposed Representations of Appearance

>2024

**RefGaussian: Disentangling Reflections from 3D Gaussian Splatting for Realistic Rendering.** *Rui Zhang, Tianyue Luo, Weidong Yang, Ben Fei, Jingyi Xu, Qingyuan Zhou, Keyi Liu, Ying He.*
<a href="https://arxiv.org/abs/2406.05852">
  <img src="https://img.shields.io/badge/arXiv-2406.05852-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**HMGS: Hybrid Model of Gaussian Splatting for Enhancing 3D Reconstruction with Reflections.** *Hengbin Zhang, Chengliang Wang, Ji Liu, Tian Jiang, Yonggang Luo, Lecheng Xie.*
<a href="https://link.springer.com/chapter/10.1007/978-981-96-0972-7_9">
  <img src="https://img.shields.io/badge/Paper-ACCV24-003E8C" alt="Paper" height="15" style="vertical-align:middle" />
</a>


**Spec-Gaussian: Anisotropic View-Dependent Appearance for 3D Gaussian Splatting.** *Ziyi Yang, Xinyu Gao, Yang-Tian Sun, Yi-Hua Huang, Xiaoyang Lyu, Wen Zhou, Shaohui Jiao, Xiaojuan Qi, Xiaogang Jin.*
<a href="https://proceedings.neurips.cc/paper_files/paper/2024/hash/708e0d691a22212e1e373dc8779cbe53-Abstract-Conference.html">
  <img src="https://img.shields.io/badge/Paper-NeurIPS24-purple" alt="paper" height="15" style="vertical-align:middle"/>
</a><a href="https://ingra14m.github.io/Spec-Gaussian-website/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/ingra14m/Specular-Gaussians">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**DC-Gaussian: Improving 3D Gaussian Splatting for Reflective Dash Cam Videos.**
*Linhan Wang, Kai Cheng, Shuo Lei, Shengkun Wang, Wei Yin, Chenyang Lei, Xiaoxiao Long, Chang-Tien Lu.*
<a href="https://proceedings.neurips.cc/paper_files/paper/2024/hash/b51b50262b492dd89bb9cd3105a46702-Abstract-Conference.html">
  <img src="https://img.shields.io/badge/Paper-NeurIPS24-purple" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://linhanwang.github.io/dcgaussian/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/linhanwang/DC-Gaussian">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**SpecGaussian with Latent Features: A High-quality Modeling of the View-dependent Appearance for 3D Gaussian Splatting.** *Zhiru Wang, Shiyun Xie, Chengwei Pan, Guoping Wang.*
<a href="https://dl.acm.org/doi/abs/10.1145/3664647.3681059">
  <img src="https://img.shields.io/badge/Paper-MM24-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/MarcWangzhiru/SpeclatentGS">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>


>2025

**Reflections Unlock: Geometry-Aware Reflection Disentanglement in 3D Gaussian Splatting for Photorealistic Scenes Rendering.**  *Jiayi Song, Zihan Ye, Qingyuan Zhou, Weidong Yang, Ben Fei, Jingyi Xu, Ying He, Wanli Ouyang.*
<a href="https://arxiv.org/abs/2507.06103">
  <img src="https://img.shields.io/badge/arXiv-2507.06103-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://ref-unlock.github.io/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/Kallyelish/Ref-Unlock">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**VoD-3DGS: View-opacity-Dependent 3D Gaussian Splatting.** *Mateusz Nowak, Wojciech Jarosz, Peter Chin.*
<a href="https://arxiv.org/abs/2501.17978">
  <img src="https://img.shields.io/badge/arXiv-2501.17978-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a> 

**TR-Gaussians: High-fidelity Real-time Rendering of Planar Transmission and Reflection with 3D Gaussian Splatting.**  *Yong Liu, Keyang Ye, Tianjia Shao, Kun Zhou.*
<a href="https://arxiv.org/abs/2511.13009">
  <img src="https://img.shields.io/badge/arXiv-2511.13009-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**Dual Spherical Harmonics for 3D Gaussian Splatting: Novel View Synthesis with Dynamic Lighting.** *Alp Bora Orgun, Marco Volino, Adrian Hilton, Jean-Yves Guillemaut.*
<a href="https://dl.acm.org/doi/full/10.1145/3756863.3769709">
  <img src="https://img.shields.io/badge/Paper-CVMP25-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>

**Image-based View-dependent Appearance for 3D Gaussian Splatting.** *Yanan Guo, Ying Xie, Ying Chang, Benkui Zhang, Kangning Du, Lin Cao.*
<a href="https://www.sciencedirect.com/science/article/pii/S0141938225002227">
  <img src="https://img.shields.io/badge/Paper-Displa25-orange" alt="Paper" height="15" style="vertical-align:middle" />
</a>

**Gaussian Splatting with NeRF-based Color and Opacity.** *Dawid Malarz, Weronika Smolak-Dyżewska, Jacek Tabor, Sławomir Tadeja, Przemysław Spurek.*
<a href="https://www.sciencedirect.com/science/article/abs/pii/S1077314224003540">
  <img src="https://img.shields.io/badge/Paper-CVIU25-orange" alt="Paper" height="15" style="vertical-align:middle" />
</a>

**Glossy-Gaussian: Adaptive Anisotropic Gaussians for View-Dependent Appearances.** *Wendi Zhang, Tengfei Wang, Zongqian Zhan, Xin Wang.*
<a href="https://ieeexplore.ieee.org/abstract/document/10878500">
  <img src="https://img.shields.io/badge/Paper-LSP25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/gwen233666/Glossy-Gaussian-Splatting">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**2D Gaussian Splatting-based Sparse-view Transparent Object Depth Reconstruction via Physics Simulation for Scene Update.** *Jeongyun Kim, Seunghoon Jeong, Giseop Kim, Myung-Hwan Jeon, Eunji Jun, Ayoung Kim.*
<a href="https://openaccess.thecvf.com/content/ICCV2025/html/Kim_2D_Gaussian_Splatting-based_Sparse-view_Transparent_Object_Depth_Reconstruction_via_Physics_ICCV_2025_paper.html">
  <img src="https://img.shields.io/badge/Paper-ICCV25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://jeongyun0609.github.io/TRAN-D/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/jeongyun0609/TRAN-D">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

---

#### II. Decomposed Appearance from Geometry

>2024

**Space-View Decoupled 3D Gaussians for Novel-View Synthesis of Mirror Reflections.** *Zhenwu Wang, Zhuopeng Li, Zhenhua Tang, Yanbin Hao, Huasen He.*
<a href="https://link.springer.com/chapter/10.1007/978-981-96-0125-7_7">
  <img src="https://img.shields.io/badge/Paper-PRICAI24-003E8C" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**Gaussian Splatting in Mirrors: Reflection-aware Rendering via Virtual Camera Optimization.** *Zihan Wang, Shuzhe Wang, Matias Turkulainen, Junyuan Fang, Juho Kannala.*
<a href="https://bmvc2024.org/proceedings/945/">
  <img src="https://img.shields.io/badge/Paper-BMVC24-000E8D" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://github.com/rzhevcherkasy/BMVC24-GSIM">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**Mirror-3DGS: Incorporating Mirror Reflections into 3D Gaussian Splatting.** *Jiarui Meng, Haijie Li, Yanmin Wu, Qiankun Gao, Shuzhou Yang, Jian Zhang.*
<a href="https://ieeexplore.ieee.org/abstract/document/10849936">
  <img src="https://img.shields.io/badge/Paper-VCIP24-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>

**MirrorGaussian: Reflecting 3D Gaussians for Reconstructing Mirror Reflections.** *Jiayue Liu, Xiao Tang, Freeman Cheng, Roy Yang, Zhihao Li, Jianzhuang Liu, Yi Huang, Jiaqi Lin, Shiyong Liu, Xiaofei Wu, Songcen Xu, Chun Yuan.*
<a href="https://link.springer.com/chapter/10.1007/978-3-031-73220-1_22">
  <img src="https://img.shields.io/badge/Paper-ECCV24-003E8C" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://mirror-gaussian.github.io/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**3D Gaussian Splatting with Deferred Reflection.** *Keyang Ye, Qiming Hou, Kun Zhou.*
<a href="https://dl.acm.org/doi/abs/10.1145/3641519.3657456">
  <img src="https://img.shields.io/badge/Paper-SIGGRAPH24-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://gapszju.github.io/3DGS-DR/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/gapszju/3DGS-DR">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>




>2025

**Car-GS: Addressing Reflective and Transparent Surface Challenges in 3D Car Reconstruction.** *Congcong Li, Jin Wang, Xiaomeng Wang, Xingchen Zhou, Wei Wu, Yuzhi Zhang, Tongyi Cao.*
<a href="https://arxiv.org/abs/2501.11020">
  <img src="https://img.shields.io/badge/arXiv-2501.11020-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://lcc815.github.io/Car-GS/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>

**Seeing Through Reflections: Advancing 3D Scene Reconstruction in Mirror-Containing Environments with Gaussian Splatting.**
*Zijing Guo, Yunyang Zhao, Lin Wang.*
<a href="https://arxiv.org/abs/2509.18956">
  <img src="https://img.shields.io/badge/arXiv-2509.18956-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**GlassGaussian: Extending 3D Gaussian Splatting for Realistic Imperfections and Glass Materials.** *Junming Cao, Jiadi Cui, Sören Schwertfeger.*
<a href="https://ieeexplore.ieee.org/abstract/document/10884729">
  <img src="https://img.shields.io/badge/Paper-IEEE_Access25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>

**Dynamic 3D Gaussian Reconstruction with Specular Reflection.** *Mingyang Zhao, Yuanzhi Xu, Yifan Zuo, Xiaoshui Huang, Qiang Chen, Yuming Fang.*
<a href="https://ieeexplore.ieee.org/abstract/document/11084729">
  <img src="https://img.shields.io/badge/Paper-ICIP25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>

**GS-SE: Gaussian Splatting for Novel View Synthesis in Specular Effects.** *Yang Bai, Zhengxuan Jiang, Ying Wang, Jiahao Wang, Xiaosheng Yu.*
<a href="https://ieeexplore.ieee.org/abstract/document/11090650">
  <img src="https://img.shields.io/badge/Paper-CCDC25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>

**Disentangled Gaussian Splatting: High-Fidelity Relightable Volumetric Video through Geometry-Appearance Decoupling.** *Yifeng Zhou, Chao Zhang, Shuheng Wang, Wenfa Li, Xu Yi, Degang Wang, Yuzhong Chen, Shaohui Jiao*
<a href="https://dl.acm.org/doi/full/10.1145/3757376.3771406">
  <img src="https://img.shields.io/badge/Paper-SIGGRAPH_Aisa25TC-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>

**Improving Gaussian Splatting for Transparent Surface Reconstruction via Normal and De-lighting Priors.** *Mingwei Li, Pu Pang, Hehe Fan, Hua Huang, Yi Yang.*
<a href="https://dl.acm.org/doi/abs/10.1145/3746027.3754548">
  <img src="https://img.shields.io/badge/Paper-MM25-red" alt="Paper" height="15" style="vertical-align:middle" />
</a><a href="https://longxiang-ai.github.io/TSGS/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/longxiang-ai/TSGS">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>


**Ref-GS: Directional Factorization for 2D Gaussian Splatting.** *Youjia Zhang, Anpei Chen, Yumin Wan, Zikai Song, Junqing Yu, Yawei Luo, Wei Yang.*
<a href="https://openaccess.thecvf.com/content/CVPR2025/html/Zhang_Ref-GS_Directional_Factorization_for_2D_Gaussian_Splatting_CVPR_2025_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://ref-gs.github.io/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/YoujiaZhang/Ref-GS">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>



**MGSR: 2D/3D Mutual-boosted Gaussian Splatting for High-fidelity Surface Reconstruction under Various Light Conditions** *Qingyuan Zhou, Yuehu Gong, Weidong Yang, Jiaze Li, Yeqi Luo, Baixin Xu, Shuhao Li, Ben Fei, Ying He.*
<a href="https://openaccess.thecvf.com/content/ICCV2025/html/Zhou_MGSR_2D3D_Mutual-boosted_Gaussian_Splatting_for_High-fidelity_Surface_Reconstruction_under_ICCV_2025_paper.html">
  <img src="https://img.shields.io/badge/Paper-ICCV25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/TsingyuanChou/MGSR">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

---
---

### Ray Tracing for Enhanced Rasterization

>2025

**Stochastic Ray Tracing of Transparent 3D Gaussians.** *Xin Sun, Iliyan Georgiev, Yun Fei, Miloš Hašan.*
<a href="https://arxiv.org/abs/2504.06598">
  <img src="https://img.shields.io/badge/arXiv-2504.06598-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**TraceFlow: Dynamic 3D Reconstruction of Specular Scenes Driven by Ray Tracing.** *Jiachen Tao, Junyi Wu, Haoxuan Wang, Zongxin Yang, Dawen Cai, Yan Yan.*
<a href="https://arxiv.org/abs/2512.10095">
  <img src="https://img.shields.io/badge/arXiv-2512.10095-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**HybridSplat: Fast Reflection-baked Gaussian Tracing using Hybrid Splatting.** *Chang Liu, Hongliang Yuan, Lianghao Zhang, Sichao Wang, Jianwei Guo, Shi-Sheng Huang.*
<a href="https://arxiv.org/abs/2512.08334">
  <img src="https://img.shields.io/badge/arXiv-2512.08334-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://aetheryne.github.io/HybridSplat/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>


**EnvGS: Modeling View-Dependent Appearance with Environment Gaussian.**
*Tao Xie, Xi Chen, Zhen Xu, Yiman Xie, Yudong Jin, Yujun Shen, Sida Peng, Hujun Bao, Xiaowei Zhou.*
<a href="https://openaccess.thecvf.com/content/CVPR2025/html/Xie_EnvGS_Modeling_View-Dependent_Appearance_with_Environment_Gaussian_CVPR_2025_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://zju3dv.github.io/envgs/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/zju3dv/EnvGS">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

---
---

### Inverse Rendering

#### I. Inverse Rendering for Surfaces of Arbitrary Reflectance

>2024



**Phys3DGS: Physically-based 3D Gaussian Splatting for Inverse Rendering.** *Euntae Choi, Sungjoo Yoo.*
<a href="https://arxiv.org/abs/2409.10335">
  <img src="https://img.shields.io/badge/arXiv-2409.10335-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**Subsurface Scattering for Gaussian Splatting.** *Jan-Niklas Dihlmann, Arjun Majumdar, Andreas Engelhardt, Raphael Braun, Hendrik P.A. Lensch.*
<a href="https://proceedings.neurips.cc/paper_files/paper/2024/hash/dc72529d604962a86b7730806b6113fa-Abstract-Conference.html">
  <img src="https://img.shields.io/badge/Paper-NeurIPS24-purple" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://sss.jdihlmann.com/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/cgtuebingen/SSS-GS">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**Relightable 3D Gaussians: Realistic Point Cloud Relighting with BRDF Decomposition and Ray Tracing.** *Jian Gao, Chun Gu, Youtian Lin, Zhihao Li, Hao Zhu, Xun Cao, Li Zhang, Yao Yao.*
<a href="https://link.springer.com/chapter/10.1007/978-3-031-72995-9_5">
  <img src="https://img.shields.io/badge/Paper-ECCV24-003E8C" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://nju-3dv.github.io/projects/Relightable3DGaussian/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/NJU-3DV/Relightable3DGaussian">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>



**GS-IR: 3D Gaussian Splatting for Inverse Rendering.** *Zhihao Liang, Qi Zhang, Ying Feng, Ying Shan, Kui Jia.*
<a href="https://openaccess.thecvf.com/content/CVPR2024/html/Liang_GS-IR_3D_Gaussian_Splatting_for_Inverse_Rendering_CVPR_2024_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR24-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://lzhnb.github.io/project-pages/gs-ir.html">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/lzhnb/GS-IR">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

>2025

**3D Gaussian Inverse Rendering with Approximated Global Illumination.**
*Zirui Wu, Jianteng Chen, Laijian Li, Shaoteng Wu, Zhikai Zhu, Kang Xu, Martin R. Oswald, Jie Song.*
<a href="https://arxiv.org/abs/2504.01358">
  <img src="https://img.shields.io/badge/arXiv-2504.01358-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://wuzirui.github.io/gs-ssr/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/wuzirui/gs-ssr">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**MatSpray: Fusing 2D Material World Knowledge on 3D Geometry.** *Philipp Langsteiner, Jan-Niklas Dihlmann, Hendrik P.A. Lensch.*
<a href="https://arxiv.org/abs/2512.18314">
  <img src="https://img.shields.io/badge/arXiv-2512.18314-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a><a href="https://matspray.jdihlmann.com/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/cgtuebingen/MatSpray">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**InvGS: a Novel Real-Time Inverse Rendering Framework Utilizing 3D Gaussian Splatting.** *Yang Pu, Qingfeng Wu.*
<a href="https://ieeexplore.ieee.org/abstract/document/10888981">
  <img src="https://img.shields.io/badge/Paper-ICASSP25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>

**GI-GS: Global Illumination Decomposition on Gaussian Splatting for Inverse Rendering.** *Hongze Chen, Zehong Lin, Jun Zhang.*
<a href="https://arxiv.org/abs/2410.02619">
  <img src="https://img.shields.io/badge/arXiv-2410.02619-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://openreview.net/forum?id=hJIEtJlvhL">
  <img src="https://img.shields.io/badge/OpenReview-ICLR25-darkred" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://stopaimme.github.io/GI-GS-site/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/stopaimme/GI-GS">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**GS-ID: Illumination Decomposition on Gaussian Splatting via Adaptive Light Aggregation and Diffusion-Guided Material Priors.** *Kang Du, Zhihao Liang, Yulin Shen, Zeyu Wang.*
<a href="https://openaccess.thecvf.com/content/ICCV2025/papers/Du_GS-ID_Illumination_Decomposition_on_Gaussian_Splatting_via_Adaptive_Light_Aggregation_ICCV_2025_paper.pdf">
  <img src="https://img.shields.io/badge/Paper-ICCV25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://kangdu.top/gsid/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/dukang/GS-ID">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

---

#### II. Environment-based Approximation of Illumination for Non-Lambertian Surfaces

>2024

**Progressive Radiance Distillation for Inverse Rendering with Gaussian Splatting.** *Keyang Ye, Qiming Hou, Kun Zhou.*
<a href="https://arxiv.org/abs/2408.07595">
  <img src="https://img.shields.io/badge/arXiv-2408.07595-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**Normal-GS: 3D Gaussian Splatting with Normal-Involved Rendering.** *Meng Wei, Qianyi Wu, Jianmin Zheng, Hamid Rezatofighi, Jianfei Cai.*
<a href="https://proceedings.neurips.cc/paper_files/paper/2024/hash/8bd4f1dbc7a70c6b80ce81b8b4fdc0b2-Abstract-Conference.html">
  <img src="https://img.shields.io/badge/Paper-NeurIPS24-purple" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://github.com/Meng-Wei/Normal-GS">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>


**3iGS: Factorised Tensorial Illumination for 3D Gaussian Splatting.** *Zhe Jun Tang, Tat-Jen Cham.* 
<a href="https://link.springer.com/chapter/10.1007/978-3-031-72630-9_9">
  <img src="https://img.shields.io/badge/Paper-ECCV24-003E8C" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://github.com/TangZJ/3iGS">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>


**GaussianShader: 3D Gaussian Splatting with Shading Functions for Reflective Surfaces.** *Yingwenqi Jiang, Jiadong Tu, Yuan Liu, Xifeng Gao, Xiaoxiao Long, Wenping Wang, Yuexin Ma.*
<a href="https://openaccess.thecvf.com/content/CVPR2024/html/Jiang_GaussianShader_3D_Gaussian_Splatting_with_Shading_Functions_for_Reflective_Surfaces_CVPR_2024_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR24-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://asparagus15.github.io/GaussianShader.github.io/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/Asparagus15/GaussianShader">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>


>2025

**GlossGau: Efficient Inverse Rendering for Glossy Surface with Anisotropic Spherical Gaussian.** *Bang Du, Runfa Blark Li, Chen Du, Truong Nguyen.*
<a href="https://arxiv.org/abs/2502.14129">
  <img src="https://img.shields.io/badge/arXiv-2502.14129-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**ROSGS: Relightable Outdoor Scenes With Gaussian Splatting.** *Lianjun Liao, Chunhui Zhang, Tong Wu, Henglei Lv, Bailin Deng, Lin Gao.*
<a href="https://arxiv.org/abs/2509.11275">
  <img src="https://img.shields.io/badge/arXiv-2509.11275-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**GS-2M: Gaussian Splatting for Joint Mesh Reconstruction and Material Decomposition.** *Dinh Minh Nguyen, Malte Avenhaus, Thomas Lindemeier.*
<a href="https://arxiv.org/abs/2509.22276">
  <img src="https://img.shields.io/badge/arXiv-2509.22276-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://ndming.github.io/publications/gs2m/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/ndming/GS-2M">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**GAINS: Gaussian-based Inverse Rendering from Sparse Multi-View Captures.** *Patrick Noras, Jun Myeong Choi, Didier Stricker, Pieter Peers, Roni Sengupta.*
<a href="https://arxiv.org/abs/2512.09925">
  <img src="https://img.shields.io/badge/arXiv-2512.09925-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://patrickbail.github.io/gains/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>

**Efficient 3D Gaussian Splatting Surface Rendering for Reflective Objects.** *Peiyao Xie, Xi-En Cheng.*
<a href="https://www.spiedigitallibrary.org/conference-proceedings-of-spie/13793/137932A/Efficient-3D-Gaussian-splatting-surface-rendering-for-reflective-objects/10.1117/12.3077433.short">
  <img src="https://img.shields.io/badge/Paper-MVAID25-FFF100" alt="Paper" height="15" style="vertical-align:middle" />
</a>

**RTR-GS: 3D Gaussian Splatting for Inverse Rendering with Radiance Transfer and Reflection.** *Yongyang Zhou, Fanglue Zhang, Zichen Wang, Lei Zhang.*
<a href="https://dl.acm.org/doi/abs/10.1145/3746027.3755197">
  <img src="https://img.shields.io/badge/Paper-MM25-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/ZyyZyy06/RTR-GS">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**GS-2DGS: Geometrically Supervised 2DGS for Reflective Object Reconstruction.** *Jinguang Tong, Xuesong Li, Fahira Afzal Maken, Sundaram Muthu, Lars Petersson, Chuong Nguyen, Hongdong Li.*
<a href="https://openaccess.thecvf.com/content/CVPR2025/html/Tong_GS-2DGS_Geometrically_Supervised_2DGS_for_Reflective_Object_Reconstruction_CVPR_2025_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/hirotong/GS2DGS">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**SVG-IR: Spatially-Varying Gaussian Splatting for Inverse Rendering.** *Hanxiao Sun, Yupeng Gao, Jin Xie, Jian Yang, Beibei Wang.*
<a href="https://openaccess.thecvf.com/content/CVPR2025/html/Sun_SVG-IR_Spatially-Varying_Gaussian_Splatting_for_Inverse_Rendering_CVPR_2025_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://learner-shx.github.io/project_pages/SVG-IR/index">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/learner-shx/SVG-IR">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**SpectroMotion: Dynamic 3D Reconstruction of Specular Scenes.** *Cheng-De Fan, Chen-Wei Chang, Yi-Ruei Liu, Jie-Ying Lee, Jiun-Long Huang, Yu-Chee Tseng, Yu-Lun Liu.*
<a href="https://openaccess.thecvf.com/content/CVPR2025/html/Fan_SpectroMotion_Dynamic_3D_Reconstruction_of_Specular_Scenes_CVPR_2025_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://cdfan0627.github.io/spectromotion/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/cdfan0627/SpectroMotion">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**Gaussian Splatting with Discretized SDF for Relightable Assets.** *Zuo-Liang Zhu, Jian Yang, Beibei Wang.*
<a href="https://openaccess.thecvf.com/content/ICCV2025/html/Zhu_Gaussian_Splatting_with_Discretized_SDF_for_Relightable_Assets_ICCV_2025_paper.html">
  <img src="https://img.shields.io/badge/Paper-ICCV25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://nk-cs-zzl.github.io/projects/dsdf/index.html">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/NK-CS-ZZL/DiscretizedSDF">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**GlossyGS: Inverse Rendering of Glossy Objects With 3D Gaussian Splatting.**
*Shuichang Lai, Letian Huang, Jie Guo, Kai Cheng, Bowen Pan, Xiaoxiao Long.*
<a href="https://ieeexplore.ieee.org/abstract/document/10908905">
  <img src="https://img.shields.io/badge/Paper-TVCG25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>

**GS-ROR2: Bidirectional-guided 3DGS and SDF for Reflective Object Relighting and Reconstruction.**
*Zuoliang Zhu, Beibei Wang, Jian Yang.*
<a href="https://dl.acm.org/doi/full/10.1145/3759248">
  <img src="https://img.shields.io/badge/Paper-ToG25-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://nk-cs-zzl.github.io/projects/gsror/index.html">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/NK-CS-ZZL/GS-ROR">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>


**GUS-IR: Gaussian Splatting With Unified Shading for Inverse Rendering.** *Zhihao Liang, Hongdong Li, Kui Jia, Kailing Guo, Qi Zhang.*
<a href="https://ieeexplore.ieee.org/abstract/document/11045434">
  <img src="https://img.shields.io/badge/Paper-TPAMI25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>

**DeferredGS: Decoupled and Relightable Gaussian Splatting With Deferred Shading.** *Tong Wu, Jia-Mu Sun, Yu-Kun Lai, Yuewen Ma, Leif Kobbelt, Lin Gao.*
<a href="https://ieeexplore.ieee.org/abstract/document/10964878">
  <img src="https://img.shields.io/badge/Paper-TPAMI25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/IGLICT/DeferredGS">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**GIR: 3D Gaussian Inverse Rendering for Relightable Scene Factorization.** *Yahao Shi, Yanmin Wu, Chenming Wu, Xing Liu, Chen Zhao, Haocheng Feng.*
<a href="https://ieeexplore.ieee.org/abstract/document/11030850">
  <img src="https://img.shields.io/badge/Paper-TPAMI25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://3dgir.github.io/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/guduxiaolang/GIR">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

>2026

**RGS-DR: Reflective Gaussian Surfels with Deferred Rendering for Shiny Objects.** *Georgios Kouros, Minye Wu, Tinne Tuytelaars.*
<a href="https://arxiv.org/abs/2504.18468">
  <img src="https://img.shields.io/badge/arXiv-2504.18468-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://3dvconf.github.io/2026/accepted-papers/">
  <img src="https://img.shields.io/badge/List-3DV26-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/gkouros/RGS-DR">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**TextureSplat: Per-Primitive Texture Mapping for Reflective Gaussian Splatting.** *Mae Younes, Adnane Boukhayma.*
<a href="https://arxiv.org/abs/2506.13348">
  <img src="https://img.shields.io/badge/arXiv-2506.13348-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://3dvconf.github.io/2026/accepted-papers/">
  <img src="https://img.shields.io/badge/List-3DV26-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/maeyounes/TextureSplat">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

---

#### III. Ray Tracing-augmented Inverse Rendering for Non-Lambertian Surfaces

>2025

**GOGS: High-Fidelity Geometry and Relighting for Glossy Objects via Gaussian Surfels.**
*Xingyuan Yang, Min Wei.*
<a href="https://arxiv.org/abs/2508.14563">
  <img src="https://img.shields.io/badge/arXiv-2508.14563-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>

**MaterialRefGS: Reflective Gaussian Splatting with Multi-view Consistent Material Inference.** *Wenyuan Zhang, Jimin Tang, Weiqi Zhang, Yi Fang, Yu-Shen Liu, Zhizhong Han.*
<a href="https://neurips.cc/virtual/2025/loc/san-diego/poster/118850">
  <img src="https://img.shields.io/badge/Paper-NeurIPS25-purple" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://wen-yuan-zhang.github.io/MaterialRefGS/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/wen-yuan-zhang/MaterialRefGS">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**Reflective Gaussian Splatting.** *Yuxuan Yao, Zixuan Zeng, Chun Gu, Xiatian Zhu, Li Zhang.*
<a href="https://arxiv.org/abs/2412.19282">
  <img src="https://img.shields.io/badge/arXiv-2412.19282-b31b1b?logo=arxiv" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://openreview.net/forum?id=xPxHQHDH2u">
  <img src="https://img.shields.io/badge/OpenReview-ICLR25-darkred" alt="paper" height="15" style="vertical-align:middle"/>
</a>
<a href="https://fudan-zvg.github.io/ref-gaussian/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/fudan-zvg/ref-gaussian">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>


**Editable Physically-based Reflections in Raytraced Gaussian Radiance Fields.** *Yohan Poirier-Ginter, Jeffrey Hu, Jean-Francois Lalonde, George Drettakis.*
<a href="https://dl.acm.org/doi/full/10.1145/3757377.3763971">
  <img src="https://img.shields.io/badge/Paper-SIGGRAPH_Asia25-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://repo-sam.inria.fr/nerphys/editable-gaussian-reflections/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/graphdeco-inria/editable-gaussian-reflections">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>


**SpecTRe-GS: Modeling Highly Specular Surfaces with Reflected Nearby Objects by Tracing Rays in 3D Gaussian Splatting.** *Jiajun Tang, Fan Fei, Zhihao Li, Xiao Tang, Shiyong Liu, Youyu Chen, Binxiao Huang, Zhenyu Chen, Xiaofei Wu, Boxin Shi.*
<a href="https://openaccess.thecvf.com/content/CVPR2025/html/Tang_SpecTRe-GS_Modeling_Highly_Specular_Surfaces_with_Reflected_Nearby_Objects_by_CVPR_2025_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://spectre-gs.github.io/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>

**IRGS: Inter-Reflective Gaussian Splatting with 2D Gaussian Ray Tracing.** *Chun Gu, Xiaofei Wei, Zixuan Zeng, Yuxuan Yao, Li Zhang.*
<a href="https://openaccess.thecvf.com/content/CVPR2025/html/Gu_IRGS_Inter-Reflective_Gaussian_Splatting_with_2D_Gaussian_Ray_Tracing_CVPR_2025_paper.html">
  <img src="https://img.shields.io/badge/Paper-CVPR25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://fudan-zvg.github.io/IRGS/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/fudan-zvg/IRGS">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**GeoSplatting: Towards Geometry Guided Gaussian Splatting for Physically-based Inverse Rendering.** *Kai Ye, Chong Gao, Guanbin Li, Wenzheng Chen, Baoquan Chen.*
<a href="https://openaccess.thecvf.com/content/ICCV2025/html/Ye_GeoSplatting_Towards_Geometry_Guided_Gaussian_Splatting_for_Physically-based_Inverse_Rendering_ICCV_2025_paper.html">
  <img src="https://img.shields.io/badge/Paper-ICCV25-blue" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://pku-vcl-geometry.github.io/GeoSplatting/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/PKU-VCL-Geometry/GeoSplatting">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

**TransparentGS: Fast Inverse Rendering of Transparent Objects with Gaussians.** *Letian Huang, Dongwei Ye, Jialin Dan, Chengzhi Tao, Huiwen Liu, Kun Zhou, Bo Ren, Yuanqi Li, Yanwen Guo, Jie Guo.*
<a href="https://dl.acm.org/doi/abs/10.1145/3730892">
  <img src="https://img.shields.io/badge/Paper-ToG25-red" alt="Paper" height="15" style="vertical-align:middle" />
</a>
<a href="https://letianhuang.github.io/transparentgs/">
  <img src="https://img.shields.io/badge/Project-Page-yellow" height="15" style="vertical-align:middle" />
</a>
<a href="https://github.com/LetianHuang/transparentgs">
  <img src="https://img.shields.io/badge/Github-Repo-blue?logo=github" height="15" style="vertical-align:middle" />
</a>

---
---

# Commonly Used Datasets

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


