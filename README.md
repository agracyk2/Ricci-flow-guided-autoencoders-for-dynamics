**Note**: we recommend adding sigmoid() activation (up to a constant scaling such as $2 \pi$) in the Burger's equation experiment after the last layer in the parameterization neural network. This forces the parameterization to have small measure and helps the manifold learning with highly nonzero partial derivatives / Riemannian metrics. We have since reperformed this experiment by doing so, in which an updated paper will be released eventually.
 

We present Ricci-flow guided autoencoders in learning time-dependent dynamics, an autoencoder method for learning PDE data with a manifold latent space subject to Ricci flow.


<div align="center">
<img src="https://github.com/agracyk2/Ricci-flow-guided-autoencoders-in-learning-time-dependent-dynamics/assets/98125988/9e64892d-c64f-4912-8e6f-b301beb0df87" width=50% height=60%>
</div>



Manifold-based methods in learning dynamics show great potential in enhancing learning for out-of-distribution data and robustness. Also, by dynamical latent space allows a manifold representation for all time in the ambient PDE time interval.

We simulate Ricci flow in a physics-informed setting, using the Ricci flow equation

$$ \partial_t g(u,t) = -2 \text{Ric} (g(u,t)) $$

as a minimized residual as one would see in a typical physics-informed network. In particular, we parameterize $g_{\theta_g}$ with a neural network and minimize the corresponding residual, where this neural network acts as the metric of the manifold. We additional parameterize three neural networks, one for the parameterization domain $`u = \mathcal{P}_{\theta_{\mathcal{P}}} \in \mathcal{U}`$ mapping the PDE initial condition to $`\mathcal{U}`$, one for the encoder $`\mathcal{E}_{\theta_{\mathcal{E}}}`$ mapping $`u`$ to a point on the manifold under Ricci flow embedded in Euclidean space, and a decoder $`\mathcal{D}_{\theta_{\mathcal{D}}}`$ mapping to the PDE solution.




Our objective function to minimize is as follows:

<p align="center">
<img width="609" alt="af9d2f04d24887d138630bcd63f8e80e" src="https://github.com/agracyk2/Ricci-flow-guided-autoencoders-in-learning-time-dependent-dynamics/assets/98125988/42f5cc89-34b4-47a3-b901-b87e1d0b50f0">

We minimize the Ricci flow residual for the first term. The second term is to match the decoder output with the PDE data, using a composition of functions mapping from the parameterization domain to the manifold to the decoded output. The third term is matching the metric coefficients with the matrix of inner product of tangent vectors, i.e.

<p align="center">
<img width="578" alt="245f5e7b520e95aece2caa80a3b11967" src="https://github.com/agracyk2/Ricci-flow-guided-autoencoders-in-learning-time-dependent-dynamics/assets/98125988/81c1bf76-b3ec-4390-bb7a-56e9836178c7">

# Data sources

The sources used to create data were as follows:

Burger's equation: https://github.com/sachabinder/Burgers_equation_simulation/tree/main

Navier-Stokes: https://github.com/crewsdw/Incompressible2D
