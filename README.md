# Machine learning enhanced MHD simulations of the Interstellar Medium
Master's thesis by Javier Palau on hybrid ML-numerical simulations of the ISM, conducted at the Astro AI Laboratory at Heidelberg University.
## [Read the thesis here](Javier_Palau_Alegria_Master_Thesis.pdf)
- For ease of reading on the GitHub website, the thesis is also split into chapters within the [Chapters folder](Chapters)
## Code & Repositories

The work developed for this thesis is available across the following repositories:

- Super-resolution: [Super-resolution turbulence](https://github.com/javinukem/super_resolution_turbulence_FNO)
- Solver-in-the-loop (Available as a fork): [Astronomix SOL](https://github.com/leo1200/astronomix/tree/sol_tests)

The fork contains the modifications and extensions developed as part of this thesis within the arena/arena_tests/ solecito and solver_in_the_loop folders.


## Abstract

In this work, two hybrid machine-learning–numerical methods are studied in the context
of three-dimensional magnetohydrodynamic simulations of the interstellar medium: super-resolution
and solvers-in-the-loop. Super-resolution methods are used to recover fine
scale structures from low resolution simulations using Fourier Neural Operators. We
further introduce an additional parameter to the FNO model that shifts the spectral
region on which the model is applied. In contrast, solvers-in-the-loop introduce learned
corrections directly into the numerical simulation, allowing the core numerical methods
to be maintained while improving simulation accuracy. We test curriculum learning
and multiproblem approaches, with early signs of generalisation. Both approaches show
potential for improving the computational efficiency and accuracy of MHD simulations
while maintaining the advantages of numerical methods.

## Quick look
### Super-resolution
Super-resolution for three-dimensional turbulent hydrodynamical setups has been tested on a dataset covering a limited number of parameters, with successful results. The models used are based on Fourier Neural Operators and in this work we implement a novel parameter that modifies the spectral region on which the model acts on. The following figure shows an example of a UFNO model we trained. The first row shows the target state, the second row shows the super-resolved state, and the third row shows the input state. For a more detailed discussion, we refer the reader to the full thesis and the code repository [Super-resolution turbulence](https://github.com/javinukem/super_resolution_turbulence_FNO)

<img width="4279" height="2078" alt="final_snapshot_comparison" src="https://github.com/user-attachments/assets/356de666-7a2e-401a-a0e2-5b2fa48fc665" />

### Solver-in-the-loop
The solver-in-the-loop approach adds an extra term between successive applications of the simulation PDE. The model interacts only with the local structures not
captured by the simulator and thus acts as a residual term. Consequently, the learning
objective is reduced to a drift term in the simulation space towards the target state. This target state is established during training, and during
inference, we expect the model to have learned the discrepancies between the simulated and target dynamics.

The following figure summarizes a model trained on an MHD Blast. The model corrects the simulation as it progresses, and the error during the simulation can be seen in the fourth row. The first row shows a slice of the snapshot during training, second row shows a one-dimensional slice at train time, third row shows the model output against simulation time. For a deep dive we refer the reader to the full thesis and fork code [Astronomix SOL](https://github.com/leo1200/astronomix/tree/sol_tests).
<img width="4504" height="3948" alt="problem_analysis_mhd_blast" src="https://github.com/user-attachments/assets/bc43f7f5-f52b-494f-bbcc-03d41351a5e3" />

## Author

Javier Palau Alegria
- Contact email: javier.palau.alegria@gmail.com
- [LinkedIn](https://www.linkedin.com/in/javier-palau-alegria-215444237/)

## License

This thesis is licensed under the
[Creative Commons Attribution-NonCommercial 4.0 International License](https://creativecommons.org/licenses/by-nc/4.0/).

© 2026 Javier Palau Alegria
