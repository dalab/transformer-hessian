# What Does It Mean to Be a Transformer? Insights from a Theoretical Hessian Analysis
This is the code repository for the paper *What Does It Mean to Be a Transformer? Insights from a Theoretical Hessian Analysis* ([Ormaniec et al.,2025](https://openreview.net/forum?id=3ddi7Uss2A), ICLR 2025).
It contains the Jupyter notebook used to obtain numerical results presented in the paper and a customized fork of the TransformerLens library.

## Setup
We assume that you have already installed Conda. To create a Conda environment with required libraries and activate it run:
```
conda env create -f environment.yml
conda activate transformer-hessian
```
#### Local Version of TransformerLens
The above Conda configuration installs the required libraries and the local version of the TransformerLens library located in the `TransformerLens` folder. In addition to the usual library contents, it implements an option to define a self-attention layer without the softmax activation and an option to scale the residual connections. These options can be configured using the `linear_attention` and `residual_scaling` parameters in the `HookedTransformerConfig`. However, if you only want to use the provided Jupyter notebook, you don't need to worry about this, as we have already set everything up.

## Jupyter Notebook for Reproducing Results
We provide a Jupyter notebook
```
Transformer_Hessian.ipynb
```
that allows you to reproduce all the figures from the paper. The sections in the notebook will guide you through observing the Transformer Hessian heterogeneity and block growth rates, as well as comparing them with the MLP Hessian. After executing the notebook cells, the numerical results will be saved in the `results` folder in pickle format, and the figures will be saved in the `figures` folder.

## Reference
```
@inproceedings{
  ormaniec2025what,
  title={What Does It Mean to Be a Transformer? Insights from a Theoretical Hessian Analysis},
  author={Weronika Ormaniec and Felix Dangel and Sidak Pal Singh},
  booktitle={The Thirteenth International Conference on Learning Representations},
  year={2025},
  url={https://openreview.net/forum?id=3ddi7Uss2A}
}
```

