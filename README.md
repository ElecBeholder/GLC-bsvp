
# [Batch Singular Value Polarization and Weighted Semantic Augmentation for Universal Domain Adaptation [ICML 2024]](https://icml.cc/virtual/2024/poster/32860)

## Introduction
This is a preliminary implementation of replacing [GLC](https://arxiv.org/abs/2303.07110) counterpart module with our [**Batch Singular Value Polarization**](https://icml.cc/virtual/2024/poster/32860), which demonstrates the plug-and-play nature of our module.
We conducted Universal DA experiments on the Office-31, Office-Home, and VisDA, achieving an average improvement of 1.27 points over the original [GLC](https://arxiv.org/abs/2303.07110).
This code is based on [GLC](https://arxiv.org/abs/2303.07110).

## Key insights of Batch Singular Value Polarization
<img src="figures/max.pdf" width="500"/>
<img src="figures/min.pdf" width="500"/>

## Prerequisites
- python3, pytorch, numpy, PIL, scipy, sklearn, tqdm, etc.
- We have presented the our conda environment file in `./environment.yml`.

## Results
| OPDA    |Source-free         | Veneue| Office-31| OfficeHome | VisDA| DomainNet |
| ------- | --------  | ----- |-------- | --------   | ---- | ---- | 
|DANCE | No | NeurIPS-21 |80.3 | 63.9 | 42.8| 33.5|
|OVANet| No | ICCV-21    |86.5 | 71.8 | 53.1| 50.7|
|GATE  | No | CVPR-22    |87.6 | 75.6 | 56.4| 52.1|
|UMAD  | Yes | Arxiv-21      |87.0 | 70.1 | 58.3| 47.1|
|GLC   | Yes | CVPR-23    |87.8 | 75.6 | 73.1| 55.1|
|GLC_bsvp| Yes | ICML-24    |**89.0** | **76.4** | **74.9**| |

## Citation
```
@InProceedings{pmlr-v235-ziqi24a,
  title = 	 {Batch Singular Value Polarization and Weighted Semantic Augmentation for Universal Domain Adaptation},
  author =       {Ziqi, Wang and Wang, Wei and Huang, Chao and Wen, Jie and Wang, Cong},
  booktitle = 	 {Proceedings of the 41st International Conference on Machine Learning},
  pages = 	 {52361--52371},
  year = 	 {2024},
  editor = 	 {Salakhutdinov, Ruslan and Kolter, Zico and Heller, Katherine and Weller, Adrian and Oliver, Nuria and Scarlett, Jonathan and Berkenkamp, Felix},
  volume = 	 {235},
  series = 	 {Proceedings of Machine Learning Research},
  month = 	 {21--27 Jul},
  publisher =    {PMLR},
  pdf = 	 {https://raw.githubusercontent.com/mlresearch/v235/main/assets/ziqi24a/ziqi24a.pdf},
  url = 	 {https://proceedings.mlr.press/v235/ziqi24a.html},
  abstract = 	 {As a more challenging domain adaptation setting, universal domain adaptation (UniDA) introduces category shift on top of domain shift, which needs to identify unknown category in the target domain and avoid misclassifying target samples into source private categories. To this end, we propose a novel UniDA approach named Batch Singular value Polarization and Weighted Semantic Augmentation (BSP-WSA). Specifically, we adopt an adversarial classifier to identify the target unknown category and align feature distributions between the two domains. Then, we propose to perform SVD on the classifier’s outputs to maximize larger singular values while minimizing those smaller ones, which could prevent target samples from being wrongly assigned to source private classes. To better bridge the domain gap, we propose a weighted semantic augmentation approach for UniDA to generate data on common categories between the two domains. Extensive experiments on three benchmarks demonstrate that BSP-WSA could outperform existing state-of-the-art UniDA approaches.}
}
```

## Contact
- hhdxdwzq@gmail.com
