We present Ricci-flow guided autoencoders in learning time-dependent dynamics, an autoencoder method for learning PDE data with a manifold latent space subject to Ricci flow.

Manifold-based methods in learning dynamics show great promise in not only reconstructing dynamical data from the underlying distribution as seen in the training procedure, but also by extensions to extrapolation and out-of-distribution data scenarios. Dynamics in the latent space have empirical performance gains over static methods. Static methods have been previously observed in the manifold-sense, but dynamics among a manifold itself has largely been unexplored. In this work, we capture high performance in both the in-distribution data as well as in extrapolation examples using a manifold space, and one that evolves, in which we choose Ricci flow.

We simulate Ricci flow in a physics-informed setting, using the Ricci flow equation

$$ \partial_t g(u,t) = -2 \text{Ric} (g(u,t)) $$

as a minimized residual as one would see in a typical physics-informed network. In particular, we parameterize 'g_{\theta_g}' with a neural network and minimize the corresponding residual. We additional parameterize three neural networks, one for the parameterization domain $u = \mathcal{P}_{\theta_{\mathcal{P}}} \in \mathcal{U}$ mapping the PDE initial condition to $\mathcal{U}$, one for the encoder $\mathcal{E}_{\theta_{\mathcal{E}}} mapping $u$ to a point on the manifold under Ricci flow embedded in Euclidean space, and a decoder $\mathcal{D}_{\theta_{\mathcal{D}}}$ mapping to the PDE solution.
