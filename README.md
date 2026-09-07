# Machine learning enhanced MHD simulations of the Interstellar Medium
Javier Palau Master's thesis in hybrid ML-numerical simulations of the ISM at the Astro AI Laboratory in Heidelberg University.

## Code & Repositories

The work developed for this thesis is available across the following repositories:

- Super-resolution part: [Super-resolution turbulence]()
- Solver-in-the-loop part (Available as a fork): [Astronomix SOL](https://github.com/leo1200/astronomix/tree/sol_tests)

The fork builds upon the original project and contains the modifications and extensions developed as part of this thesis within the arena/arena_tests/ solecito and solver_in_the_loop folders.

## Abstract

In this work, two hybrid machine-learning–numerical methods are studied in the context
of three dimensional magnetohydrodynamic simulations of the interstellar medium: su-
perresolution and solvers-in-the-loop. Superresolution methods are used to recover fine
scale structures from low resolution simulations using Fourier Neural Operators. We
further introduce an additional parameter to the FNO model that shifts the spectral
region on which the model is applied. In contrast, solvers-in-the-loop introduce learned
corrections directly into the numerical simulation, allowing the core numerical methods
to be maintained while improving simulation accuracy. We test curriculum learning
and multiproblem approaches, with early signs of generalisation. Both approaches show
potential for improving the computational efficiency and accuracy of MHD simulations
while maintaining the advantages of numerical methods.

## Author

Javier Palau Alegria
- Contact email: javier.palau.alegria@gmail.com

## License

This thesis is licensed under the
[Creative Commons Attribution-NonCommercial 4.0 International License](https://creativecommons.org/licenses/by-nc/4.0/).

© 2026 Javier Palau Alegria
