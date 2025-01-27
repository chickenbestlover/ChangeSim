# ChangeSim

[![report](https://img.shields.io/badge/arxiv-report-red)](https://arxiv.org/abs/2103.05368)
[![page](https://img.shields.io/badge/page-changesim-green)](https://sammica.github.io/ChangeSim)
[![page](https://img.shields.io/badge/page-paperswithcode-blue)](https://paperswithcode.com/sota/scene-change-detection-on-changesim)

<p align="center"><img src="./fig/github_main_gif.gif"></p>

This repository provides ChangeSim dataset, codes and files for evaluation. Please refer to our [paper](https://arxiv.org/abs/2103.05368) (accepted to [IROS2021](https://www.iros2021.org/)) for more information about the dataset.


## Recent updates (Under construction)
- [x] Dataset download links (March 10, 2021)
- [ ] Documentation for the dataset 
- [ ] A Tutorial for the visualization of ChangeSim 
- [ ] A Tutorial for the data collection using Airsim and UE4

## Dataset download

The data is divided into train/test set and reference/query. 

[Reference_Sequence_Train](https://kaistackr-my.sharepoint.com/:u:/g/personal/jhyuk_kaist_ac_kr/Efxa73-liStOkSKpXVC4ARABY11jS0LP8O3HzhOdZ4fNNA?e=aYTREN)(52.8 GB)

[Reference_Sequence_Test](https://kaistackr-my.sharepoint.com/:u:/g/personal/jhyuk_kaist_ac_kr/EQy9p83-nvlMtY90aAnEItkBfJ7-1c3vpAe4dv5xsVlwKA?e=1OAD2l)(30.2 GB)

[Query_Sequence_Train](https://kaistackr-my.sharepoint.com/:u:/g/personal/jhyuk_kaist_ac_kr/EW1W0h1RzEhBrTUn7zcx2vUBw-W0yQ2JZGB2rREdeICEjw?e=0KRm3J)(42.8 GB)

[Query_Sequence_Test](https://kaistackr-my.sharepoint.com/:u:/g/personal/jhyuk_kaist_ac_kr/Ecy15_DweZ9EkNdKOFueMn0Bxsq7XkAYNtgHZ-klPZ9M3A?e=5J9Kd3)(30.3 GB)

### Data directory structure
```
Ref_Seq_
|
--- Warehouse_0                              # Environment folder
|       |
|       ---- Seq_0                           # Sequece
|       |      |
|       |      +--- rgb                      # 0.png - xxxx.png      
|       |      +--- depth                    # 0.png - xxxx.png
|       |      +--- semantic_segmentation    # 0.png - xxxx.png     
|       |      ---- raw                   
|       |      |     |
|       |      |     +--- rgb                # 0.png - xxxx.png
|       |      |     +--- depth              # 0.png - xxxx.png
|       |      |     ---- poses.g2o 
|       |      |     ---- rtabmap.yaml
|       |
|       +--- Seq_1
|
+-- Warehouse_1
.
.
+-- Warehouse_N



Query_Seq_
|
--- Warehouse_0                              # Environment folder
|       |
|       ---- Seq_0                           # Sequece
|       |      |
|       |      +--- rgb                      # 0.png - xxxx.png      
|       |      +--- depth                    # 0.png - xxxx.png
|       |      +--- semantic_segmentation    # 0.png - xxxx.png
|       |      +--- change_segmentation      # 0.png - xxxx.png
|       |      +--- pose                     # 0.txt - xxxx.txt
|       |      ---- t0                   
|       |      |     |
|       |      |     +--- rgb                # 0.png - xxxx.png
|       |      |     +--- depth              # 0.png - xxxx.png
|       |      |     +--- idx                # 0.txt - xxxx.txt
|       |      ---- cloud_map.ply
|       |      ---- trajectory.txt
|       |
|       +--- Seq_0_dust
|       .
|       .
|       +--- Seq_1_dark
|
+-- Warehouse_1
.
.
+-- Warehouse_N

```

## Citation
If you find this project helpful, please consider citing this project in your publications. The following is the BibTeX of our work.

```bibtex
@inproceedings{park2021changesim,
author = {Park, Jin-Man and Jang, Jae-hyuk, and Yoo, Sahng-Min and Lee, Sun-Kyung and Kim, Ue-hwan and Kim, Jong-Hwan},
title = {ChangeSim: Towards End-to-End Online Scene Change Detection in Industrial Indoor Environments},
booktitle={2021 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)},
year = {2021},
organization = {IEEE},
url = {https://arxiv.org/abs/2103.05368},
}
```
## Acknowledgement
This work was supported by Institute for Information & communications Technology Promotion (IITP) grant funded by the Korea government (MSIT) (No.2020-0-00440, Development of artificial intelligence technology that continuously improves itself as the situation changes in the real world).
