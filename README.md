# MetaNO
# A Meta-Learning Framework for Neural Operators

![MetaNO Multi-Task Architecture Demo.](https://github.com/github.com/fishmoon1234/MetaNO/architecture.png)

This repository houses the code for our paper published on Computer Methods in Applied Mechanics and Engineering:
- [MetaNO: How to transfer your knowledge on learning hidden physics](https://doi.org/10.1016/j.cma.2023.116280)

**Abstract**: Gradient-based meta-learning methods have primarily been applied to classical machine learning tasks such as image classification. Recently, partial differential equation (PDE)-solving deep learning methods, such as neural operators, are starting to make an important impact on learning and predicting the response of a complex physical system directly from observational data. Taking the material modeling problems for example, the neural operator approach learns a surrogate mapping from the loading field to the corresponding material response field, which can be seen as learning the solution operator of a hidden PDE. The microstructure and mechanical parameters of each material specimen correspond to the (possibly heterogeneous) parameter field in this hidden PDE. Due to the limitation on experimental measurement techniques, the data acquisition for each material specimen is commonly challenging and may also be costly. This fact calls for the utilization and transfer of existing knowledge to new and unseen material specimens, which corresponds to sampling efficient learning of the solution operator of a hidden PDE with a different parameter field. Herein, we propose a novel meta-learning approach for neural operators that can be seen as transferring the knowledge of solution operators between governing (unknown) PDEs with varying parameter fields. Our approach is a provably universal solution operator for multiple PDE solving tasks, with a key theoretical observation that underlying parameter fields can be captured in the first layer of neural operator models, in contrast to typical final-layer transfer in existing meta-learning methods. As applications, we demonstrate the efficacy of our proposed approach on PDE-based datasets and a real-world material modeling problem, illustrating that our method can handle complex and nonlinear physical response learning tasks while greatly improving the sampling efficiency in unseen tasks.

## Requirements
- [PyTorch](https://pytorch.org/)


## Running experiments
To run the synthetic dataset (HGO) example in the MetaNO paper
```
python3 HGO_MetaTrain.py
python3 HGO_MetaTest_valid.py
python3 HGO_MetaTest_test
```

## Datasets
We provide the synthetic datasets that are used in the paper.

## Citation

```
@article{zhang2023metano,
  title={MetaNO: How to transfer your knowledge on learning hidden physics},
  author={Zhang, Lu and You, Huaiqian and Gao, Tian and Yu, Mo and Lee, Chung-Hao and Yu, Yue},
  journal={Computer Methods in Applied Mechanics and Engineering},
  volume={417},
  pages={116280},
  year={2023},
  publisher={Elsevier}
}
```

## Acknowledgement
Special thanks to Dr. Ning Liu for his help in cleaning up the code.
