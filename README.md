# GNNs Getting ComFy: Community and Feature Similarity Guided Rewiring (ICLR 2025)

[![arXiv](https://img.shields.io/badge/arXiv-2502.04891-b31b1b.svg)](https://arxiv.org/abs/2502.04891)
[![ICLR](https://img.shields.io/badge/ICLR-2025-green.svg)](https://openreview.net/forum?id=g6v09VxgFw)

>Celia Rubio-Madrigal\*, Adarsh Jamadandi\*, Rebekka Burkholz. 
>CISPA Helmholtz Center for Information Security. \* Equal Contribution

This repository contains the code for the paper "GNNs Getting ComFy: Community and Feature Similarity Guided Rewiring", which has been accepted at ICLR 2025.

#### Abstract

>Maximizing the spectral gap through graph rewiring has been proposed to enhance the performance of message-passing graph neural networks (GNNs) by addressing over-squashing. However, as we show, minimizing the spectral gap can also improve generalization. To explain this, we analyze how rewiring can benefit GNNs within the context of stochastic block models. Since spectral gap optimization primarily influences community strength, it improves performance when the community structure aligns with node labels. Building on this insight, we propose three distinct rewiring strategies that explicitly target community structure, node labels, and their alignment: (a) community structure-based rewiring (ComMa), a more computationally efficient alternative to spectral gap optimization that achieves similar goals; (b) feature similarity-based rewiring (FeaSt), which focuses on maximizing global homophily; and (c) a hybrid approach (ComFy), which enhances local feature similarity while preserving community structure to optimize label-community alignment. Extensive experiments confirm the effectiveness of these strategies and support our theoretical insights.

![ComFy](https://github.com/RelationalML/ComFy/blob/main/ComFy.jpg)

## Requirements

The following libraries are required to run the code and reproduce the results:

```Python
1. Pytorch = 2.2.1
2. Pytorch-Geometric - 2.5.2
3. DGL - 2.2.1+cu121
```

## Structure

ComFy has the following directories:

1. Comm+Sim - this has all the code need to reproduce results for rewiring based on maximizing the feature similarity (FeaSt) and Community detection plus feature similarity based rewiring (ComFy).

2. CommunityRewiring - contains code to delete/add inter-class edges/intra-class edges directly based on communities detected.

3. Spectral - contains codes to maximize/minimise spectral gap and add/delete edges (based on our previous work [(Jamadandi et al., 2024)](https://github.com/RelationalML/SpectralPruningBraess)).

## Citation

If you found this work helpful, please consider citing our paper:

```bibtex
@inproceedings{
rubio-madrigal2025gnns,
title={{GNN}s Getting ComFy: Community and Feature Similarity Guided Rewiring},
author={Celia Rubio-Madrigal and Adarsh Jamadandi and Rebekka Burkholz},
booktitle={The Thirteenth International Conference on Learning Representations},
year={2025},
url={https://openreview.net/forum?id=g6v09VxgFw}
}
```

The spectral gap optimization [code](https://github.com/RelationalML/SpectralPruningBraess) is based on our previous work accepted at NeurIPS 2024:

[![NeurIPS 2024](https://img.shields.io/badge/NeurIPS-2024-purple.svg)](https://openreview.net/forum?id=EMkrwJY2de)

```bibtex
@inproceedings{
jamadandi2024spectral,
title={Spectral Graph Pruning Against Over-Squashing and Over-Smoothing},
author={Adarsh Jamadandi and Celia Rubio-Madrigal and Rebekka Burkholz},
booktitle={The Thirty-eighth Annual Conference on Neural Information Processing Systems},
year={2024},
url={https://openreview.net/forum?id=EMkrwJY2de}
}
```
