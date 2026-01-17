# Awesome 3D Non-Lambertian List

> A curated list of papers & resources linked to **3D Reconstruction and Novel View Synthesis on Non-Lambertian Surface**.


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
      - [Inverse Rendering for Arbitrary Reflectance](#i-inverse-rendering-for-arbitrary-reflectance)
      - [Approximation of Light Transport, Joint Optimization of Geometry and Materials for Non-Lambertian Surfaces](#ii-approximation-of-light-transport-joint-optimization-of-geometry-and-materials-for-non-lambertian-surfaces)
      - [Multi Stage Factorization and Optimization for Non-Lambertian Surfaces](#iii-multi-stage-factorization-and-optimization-for-non-lambertian-surfaces)
    - [Others](#others)
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


**NeTO:Neural Reconstruction of Transparent Objects with Self-Occlusion Aware Refraction-Tracing.** *Zongcheng Li, Xiaoxiao Long, Yusen Wang, Tuo Cao, Wenping Wang, Fei Luo, Chunxia Xiao.*
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

#### I. Inverse Rendering for Arbitrary Reflectance

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

