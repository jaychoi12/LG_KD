# Knowledge Distillation by On the fly Native Ensemble （ONE）NeurIPS2018
This is an [Pytorch](https://pytorch.org) implementation of  [Xu et al. Knowledge Distillation On the Fly Native Ensemble (ONE) NeurIPS 2018](https://arxiv.org/pdf/1806.04606.pdf) on Python 2.7, Pytorch 2.0. 
You may refer to our [Vedio](http://www.eecs.qmul.ac.uk/~xl309/Doc/Publication/2018/NIPS2018/ONE-Slide-PPT.mp4) and [Poster](http://www.eecs.qmul.ac.uk/~xl309/Doc/Publication/2018/NIPS2018/Poster_landscape.pdf)  for a quick overview.

# ONE





## Getting Started

### Prerequisites:

- Datasets: CIFAR100, CIFAR10
- ~Python 2.7.~ --> available on 3.7
- Pytorch version == ~0.2.0.~ --> availble on 1.3.1




## Running Experiments
you may need change GPU-ID in scripts， “--gpu-id”， the default is 1.
### Notebook
make jupyter kernel with matplotlib and torch 1.3.1 (with python 3.7)
And simply run 
```
cifar_one.ipynb
```
cifar100 and resnet model (ONE) is default setting

### Training: 

For example, to train the ONE model using `ResNet-32` or `ResNet-110`  on CIFAR100, run the the following scripts.
```
bash scripts/ONE_ResNet32.sh
bash scripts/ONE_ResNet110.sh
```
To train baseline model using `ResNet-32` or `ResNet-110` on CIFAR100, run the the following scripts.
```
bash scripts/Baseline_ResNet32.sh
bash scripts/Baseline_ResNet110.sh
```

## Tip for Stabilizing Model Training
It may help to ramp up [https://arxiv.org/abs/1703.01780] the KL cost in the beginning over the first few epochs until the teacher network starts giving good predictions.
## Citation
Please refer to the following if this repository is useful for your research.

### Bibtex:

```
@inproceedings{lan2018knowledge,
  title={Knowledge Distillation by On-the-Fly Native Ensemble},
  author={Lan, Xu and Zhu, Xiatian and Gong, Shaogang},
  booktitle={Advances in Neural Information Processing Systems},
  pages={7527--7537},
  year={2018}
}
```

## License

This project is licensed under the MIT License - see the [LICENSE.md](https://github.com/Lan1991Xu/ONE_NeurIPS2018/blob/master/LICENSE) file for details.


## Acknowledgements

This repository is partially built upon the [bearpaw/pytorch-classification](https://github.com/bearpaw/pytorch-classification) repository. 
