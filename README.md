**Note**: we recommend adding sigmoid() activation (up to a constant scaling such as $2 \pi$) in the Burger's equation experiment after the last layer in the parameterization neural network. This forces the parameterization to have small measure and helps the manifold learning with highly nonzero partial derivatives / Riemannian metrics. We have since reperformed this experiment by doing so. An updated preprint should be available on arXiv as of 7/9/24.
 

We present Ricci-flow guided autoencoders in learning time-dependent dynamics, an autoencoder method for learning PDE data with a manifold latent space subject to Ricci flow. The latent manifold faciliates qualities such as learning for out-of-distribution data and robustness. Simultaneously, the continuous nature of the geometric flow means a latent manifold is sustained for all values in the ambient PDE interval.



<div align="center">
<img src="https://github.com/agracyk2/Ricci-flow-guided-autoencoders-for-dynamics/assets/98125988/a10065f7-4348-49cf-b4aa-32be6ddbc956" width="500">
</div>




# Data sources

The sources used to create data were as follows:

Burger's equation: https://github.com/sachabinder/Burgers_equation_simulation/tree/main

Navier-Stokes: https://github.com/crewsdw/Incompressible2D
