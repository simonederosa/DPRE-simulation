# DPRE-simulation
Simulations of a 2-dimensional lazy random walk DPRE model.
We report the code for computing the partition function and the path probability $P_N(Z_M = x)$ for
the directed polymer model. These are the input parameters:
\begin{itemize}
\item[] N: max size of the system.
• samples: number of samples to compute.
• beta: disorder intensity.
• noise: matrices of disorder at each time step.
• periodic: sets the boundary conditions to periodic if 1, or Dirichlet if 0.
• normalize: if True returns the normalization of the partition function.
• r0, range_val: parameters for computing space dimensions and initial conditions (if r0 = 0 the walk starts from (0, 0)). The spatial domain is defined on a square grid.
• full: if True returns the partition function at each time, if False returns only the final step.
\end{itemize}

The function laplacian_lazy computes the laplacian for the current partition function (Z).

noise_generator produces the disorder matrices at each time step. The input value D represents
the number of integer points along the square side.

The function zeta computes the partition function for the model.

The function zeta_inverse computes the partition function backwards, starting from time
step N to 0.

path_probability computes the path probability at each time step.
