We present Ricci-flow guided autoencoders in learning time-dependent dynamics, an autoencoder method for learning PDE data with a manifold latent space subject to Ricci flow. The latent manifold faciliates qualities such as learning for out-of-distribution data and robustness. Simultaneously, the continuous nature of the geometric flow means a latent manifold is sustained for all values in the ambient PDE interval.



<div align="center">
<img src="https://github.com/user-attachments/assets/ffc1d916-f9b6-45ae-96b6-6c949aa5993b" width="500">
</div>



If you find this repository useful, please cite it as:
```bibtex
@misc{gracyk2024ricciflowguidedautoencoderslearning,
      title={Ricci flow-guided autoencoders in learning time-dependent dynamics}, 
      author={Andrew Gracyk},
      year={2024},
      eprint={2401.14591},
      archivePrefix={arXiv},
      primaryClass={cs.LG},
      url={https://arxiv.org/abs/2401.14591}, 
}
```


# Data sources

The sources used to create data were as follows:

Burger's equation: https://github.com/sachabinder/Burgers_equation_simulation/tree/main
Navier-Stokes: https://github.com/crewsdw/Incompressible2D
