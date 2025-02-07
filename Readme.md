# O2Vmapping
Source code for [ECCV2024] O2V-Mapping: Online Open-Vocabulary Mapping with Neural Implicit Representation



<div align="center">
    <a href='https://arxiv.org/abs/2404.06836'><img src='https://img.shields.io/badge/arXiv-2404.06836-b31b1b.svg'></a> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <a href='https://github.com/Fudan-MAGIC-Lab/O2Vmapping'><img src='https://img.shields.io/badge/Github-Code-blue'></a> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    <a href='https://www.youtube.com/watch?v=zWirggX_hiA&t=5s'><img src='https://img.shields.io/badge/Youtube-Video-red'></a> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
</div>
<p align="center">
  <a href="">
    <img src="https://github.com/Fudan-MAGIC-Lab/O2Vmapping/blob/main/semantic_search.gif" alt="Demo for O2Vmapping" width="80%">
  </a>
</p>


## ⚙️Installation
### Step 1. Setup Environment

```cmd
git clone --recursive https://github.com/Fudan-MAGIC-Lab/O2Vmapping.git

sudo apt-get install libopenexr-dev

cd O2Vmapping
conda env create -f environment.yml
conda activate O2V
```

### Step 2. Setup dependence

Our project relies on [SAM](https://github.com/facebookresearch/segment-anything) and [CLIP](https://github.com/openai/CLIP). Please ensure that both modules are functioning properly before running the code. For specific configuration procedures, please refer to the official repositories of [SAM](https://github.com/facebookresearch/segment-anything) and [CLIP](https://github.com/openai/CLIP). Additionally, we highly recommend using [MobileSAM](https://github.com/ChaoningZhang/MobileSAM), as it significantly enhances the runtime efficiency of the code.




## 📂Prepare Data

### 1. Replica

We recommend that you construct the dataset according to the official guidelines of the [Replica](https://github.com/facebookresearch/Replica-Dataset/tree/v1.0) dataset. The dataset should be organized as follows:

```cmd
├──config
├──Datasets
    ├──Replica
        ├──office0
            ├──pose
            ├──results
            ├──traj.txt
            └──transforms.json
   	    ...
        └──office1
    ...
    └──YOURDATA
└──run.py
...
```

### 2. Scannet

Coming soon …

### 3. Your own dataset

For the dataset you have collected yourselves, some additional processing is still required, and it will be gradually open-sourced in the future.

## 🏃Running
After ensuring the above process is correct, you can proceed to run:

```cmd
python run.py ./config/office0_door.yaml
```









## 😊Acknowlegement

This work is accomplished based on other excellent works, and we extend our gratitude for their contributions.
- [nice-slam](https://github.com/cvg/nice-slam)
- [lerf](https://github.com/kerrj/lerf)
- [segment-anything](https://github.com/facebookresearch/segment-anything)
- [MobileSAM](https://github.com/ChaoningZhang/MobileSAM)
- [CLIP](https://github.com/openai/CLIP)
